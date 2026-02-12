# Dataset Description: Corner and Shape Feature Extraction

## 1. Overview
This dataset was created for the project:
**"Corner and Shape Feature Extraction for Simple Image Analysis."**

The dataset contains images categorized to evaluate corner detection and shape analysis algorithms such as:
- Harris Corner Detection
- Shi-Tomasi Corner Detection
- Canny Edge Detection
- Contour Detection
- Hough Transform

---

## 2. Dataset Structure

The dataset is divided into three main categories:

### 1. Geometric Shapes
Images containing simple shapes on clean backgrounds:
- Squares
- Rectangles
- Triangles
- Circles
- Polygons

Purpose: To validate corner detection precision under controlled conditions.

---

### 2. Real-World Structured Objects
Images of objects with strong edges and corners:
- Buildings
- Windows
- Street signs
- Boxes
- Doors

Purpose: To evaluate algorithm performance in real-world scenarios.

---

### 3. Complex Scenes
Images with multiple overlapping objects and varying lighting conditions.

Purpose: To test robustness and generalization capability.

---

## 3. Image Specifications

- Format: JPG / PNG
- Resolution: ≥ 512×512
- Color format: RGB
- Source: Unsplash, Pexels, Pixabay (royalty-free images)

---

## 4. Preprocessing Plan

Images will be:
- Resized for uniformity
- Smoothed using Gaussian blur
- Processed using edge and corner detection algorithms

---

## 5. Intended Use

This dataset is intended for:
- Educational purposes
- Feature extraction experiments
- Computer vision algorithm testing
