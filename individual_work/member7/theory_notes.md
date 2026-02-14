# Corner and Shape Feature Extraction – Theory Notes

---

## 1. Introduction

Feature extraction is a fundamental step in **image processing** and **computer vision**. Instead of analyzing raw pixel values directly, we extract meaningful **features** from images to represent important structural or geometric information.  

In this project, we focus on:

- **Corner detection:** Identifying points where edges meet in an image.  
- **Shape feature extraction:** Measuring geometric properties of objects like area, perimeter, and circularity.  

These features are essential for applications such as:

- Object recognition  
- Image matching  
- Motion tracking  
- Scene understanding  

---

## 2. Corner Detection

### 2.1 What is a Corner?

A **corner** is a point in an image where intensity changes sharply in **both horizontal and vertical directions**. Corners are considered **stable and distinctive** features that are useful for tracking and object matching.  

Example: The corner of a square or rectangle in an image.

---

### 2.2 Image Representation

An image can be mathematically represented as a **2D intensity function**:

$$
I(x, y)
$$

Where:

- $x, y$ = spatial coordinates  
- $I(x, y)$ = intensity (brightness) at each point

---

### 2.3 Image Gradients

Corners are detected by analyzing **intensity changes** in the image:

$$
I_x = \frac{\partial I}{\partial x}, \quad
I_y = \frac{\partial I}{\partial y}
$$

- $I_x$ → horizontal intensity change  
- $I_y$ → vertical intensity change  

**Interpretation:**  

- A flat region → small change in both directions  
- An edge → large change in one direction  
- A corner → large change in both directions  

These gradients are usually approximated using the **Sobel operator**.

---

### 2.4 Structure Tensor (Second Moment Matrix)

To determine corner “strength” locally, we use the **structure tensor**:

$$
M =
\begin{bmatrix}
\sum I_x^2 & \sum I_x I_y \\
\sum I_x I_y & \sum I_y^2
\end{bmatrix}
$$

- Summations are over a small window around the pixel  
- Captures how intensity varies in both x and y directions  

**Eigenvalues** of $M$ provide information about the type of region:

| $\lambda_1$ | $\lambda_2$ | Region Type |
| --- | --- | --- |
| Small | Small | Flat region |
| Large | Small | Edge |
| Small | Large | Edge |
| Large | Large | Corner |

---

### 2.5 Harris Corner Response Function

The **Harris corner response** measures how likely a pixel is a corner:

$$
R = \det(M) - k \cdot (\text{trace}(M))^2
$$

Where:

- $\det(M) = \lambda_1 \lambda_2$  
- $\text{trace}(M) = \lambda_1 + \lambda_2$  
- $k$ = sensitivity constant (usually 0.04–0.06)  

**Interpretation:**

- Large positive $R$ → corner  
- Negative or small $R$ → edge or flat region  

---

## 3. Shape Feature Extraction

Shape features describe the **geometry of objects** in an image. They are global features, unlike corners which are local.

---

### 3.1 Contours

Contours are **boundaries of objects** in a binary or segmented image.  

Steps to extract contours:

1. Convert image to grayscale  
2. Apply thresholding or edge detection  
3. Use contour detection algorithms to trace object boundaries  

---

### 3.2 Area

Area is the **number of pixels inside a contour**:

$$
A = \sum_{(x,y) \in \text{region}} 1
$$

- Measures size of the object  
- Larger area → bigger object

---

### 3.3 Perimeter

Perimeter is the **length of the contour boundary**:

$$
P = \sum \sqrt{(x_i - x_{i-1})^2 + (y_i - y_{i-1})^2}
$$

- Longer perimeter → more complex or larger object boundary

---

### 3.4 Aspect Ratio

Aspect ratio describes the **proportions of a shape**:

$$
\text{Aspect Ratio} = \frac{\text{Width}}{\text{Height}}
$$

- Width = horizontal bounding box length  
- Height = vertical bounding box length  

**Usage:** Distinguish squares vs rectangles, tall vs wide shapes.

---

### 3.5 Circularity

Circularity measures how closely a shape resembles a circle:

$$
\text{Circularity} = \frac{4 \pi A}{P^2}
$$

- 1 → perfect circle  
- Smaller values → irregular shape  

**Interpretation:** Useful for classifying shapes like circles, ellipses, or polygons.

---

## 4. Strengths and Limitations

### 4.1 Strengths

**Corner Detection:**

- Computationally efficient  
- Detects stable and distinctive points  
- Useful for tracking and object recognition  

**Shape Features:**

- Easy to compute  
- Provides global geometric information  
- Helpful for classification and object comparison  

---

### 4.2 Limitations

**Corner Detection:**

- Sensitive to noise  
- Can fail under blur  
- Sensitive to illumination changes  

**Shape Features:**

- Dependent on accurate segmentation  
- Struggles with overlapping objects  
- Limited invariance to scale or deformation  

---

## 5. Conclusion

Corner and shape features complement each other in image analysis:

- **Corners:** capture local structure (e.g., edges, intersection points)  
- **Shapes:** capture global structure (e.g., size, geometry)  

Together, they provide a robust representation for **simple image analysis**, forming the foundation for advanced computer vision tasks such as object recognition, tracking, and classification.

---
