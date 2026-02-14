
# Corner and Shape Feature Extraction for Simple Image Analysis

## Project Overview

This project explores fundamental feature extraction techniques in image processing and computer vision.  

The goal is to extract meaningful structural and geometric features from simple images using:

- Harris Corner Detection
- Contour-Based Shape Feature Extraction

These techniques allow us to analyze both **local features** (corners) and **global features** (shape properties).

---

## Objectives

- Detect corners using the Harris Corner Detector  
- Extract object contours from binary images  
- Compute geometric shape features:
  - Area
  - Perimeter
  - Aspect Ratio
  - Circularity  
- Analyze strengths and limitations of these methods  

---

## Theoretical Background

The project is based on two core concepts:

### Corner Detection

The Harris Corner Response is defined as:

$$
R = \det(M) - k(\text{trace}(M))^2
$$

Where:

- $M$ is the structure tensor  
- $\det(M) = \lambda_1 \lambda_2$  
- $\text{trace}(M) = \lambda_1 + \lambda_2$  

A large positive value of $R$ indicates a corner.

---

### Shape Feature Extraction

Key geometric formulas used:

- **Area:** Number of pixels inside contour  
- **Perimeter:** Boundary length of contour  
- **Aspect Ratio:** Width / Height  
- **Circularity:**  

$$
\frac{4\pi A}{P^2}
$$

Circularity close to 1 indicates a shape close to a perfect circle.

---

## Project Structure

```
Corner-Shape-Feature-Extraction/
│
├── theory_notes.md
├── documentation.ipynb
├── sample_images/
└── README.md
```

### File Descriptions

- **theory_notes.md**  
  Contains detailed mathematical explanations and theoretical background.

- **documentation.ipynb**  
  Jupyter Notebook containing:
  - Implementation of algorithms  
  - Visualizations  
  - Feature computations  
  - Observations and analysis  

- **sample_images/**  
  Folder containing input images used for experiments.

---

## Technologies Used

- Python  
- OpenCV  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/GyabaahFelix/DCIT407-Group21-Corner-Shape-Extraction.git
```

2. Navigate to the project directory:

```bash
cd Corner-Shape-Feature-Extraction
```

3. Install required libraries:

```bash
pip install opencv-python numpy matplotlib
```

4. Open Jupyter Notebook:

Open `documentation.ipynb` and run all cells.

---

## Extracted Features

The system extracts:

- Corner points (local features)
- Object contours
- Area
- Perimeter
- Aspect Ratio
- Circularity

These features can be used for object recognition and classification.

---

## Strengths

- Computationally efficient  
- Easy to interpret  
- Works well for simple structured images  
- Provides both local and global feature representation  

---

## Limitations

- Sensitive to noise and illumination changes  
- Dependent on accurate segmentation  
- Not inherently scale-invariant  
- Limited robustness to overlapping objects  

---

## Applications

- Object recognition  
- Shape classification  
- Motion tracking  
- Basic computer vision systems  

---

## Conclusion

This project demonstrates how corner detection and shape feature extraction provide meaningful structural information from images. These foundational techniques form the basis for more advanced computer vision systems.
