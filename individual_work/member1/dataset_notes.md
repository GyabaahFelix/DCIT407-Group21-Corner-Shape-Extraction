# Dataset Notes
## Corner and Shape Feature Extraction for Simple Image Analysis

---

## 1. Overview

This dataset was created for the project:

"Corner and Shape Feature Extraction for Simple Image Analysis"

It contains 15 high-resolution RGB images organized into 5 structured categories designed to evaluate classical computer vision feature extraction algorithms.

---

## 2. Dataset Structure

Total Images: 15  
Images per Category: 3  

### 1. Building
Images:
- building1.jpg
- building2.jpg
- building3.jpg

Description:
Architectural structures with strong vertical and horizontal edges. Ideal for detecting structural corners and line intersections.

---

### 2. Checker
Images:
- checker1.jpg
- checker2.jpg
- checker3.jpg

Description:
Checkerboard-style patterns with repeated high-contrast corner points.
Excellent for evaluating Harris and Shi-Tomasi corner detection.

---

### 3. Grid
Images:
- grid1.jpg
- grid2.jpg
- grid3.jpg

Description:
Structured grid-like patterns with dense corner distributions.
Useful for testing robustness of corner detection under repetition.

---

### 4. Object
Images:
- object1.jpg
- object2.jpg
- object3.jpg

Description:
Everyday objects with mixed edge structures and moderate complexity.
Used to evaluate feature extraction in semi-structured environments.

---

### 5. Shape
Images:
- shape1.jpg
- shape4.jpg
- shape5.jpg

Description:
Geometric shapes with defined contours.
Useful for contour detection and shape approximation experiments.

---

## 3. Image Specifications

- Format: JPG
- Color Space: RGB
- Resolution Range:
  - Minimum: 1536 × 2048
  - Maximum: 6720 × 4480
- Source: Locally collected structured images

---

## 4. Preprocessing Strategy

Before feature extraction, images will be:

1. Converted to grayscale
2. Resized to uniform resolution (512×512)
3. Smoothed using Gaussian Blur
4. Processed using:
   - Harris Corner Detection
   - Shi-Tomasi Corner Detection
   - Canny Edge Detection
   - Contour Detection
   - Hough Transform

---

## 5. Intended Use

This dataset is intended for:

- Educational computer vision experiments
- Corner detection validation
- Shape detection evaluation
- Structured feature extraction analysis

---

## 6. Observations

- Checker and Grid categories produce dense corner responses.
- Building category produces structural architectural corners.
- Shape category is suitable for contour-based shape classification.
- Object category provides semi-natural scene variability.
