# Image Preprocessing for Corner and Shape Feature Extraction

## Overview
This component of the project focuses on image preprocessing techniques
required before performing corner and shape feature extraction. Proper
preprocessing improves image quality, reduces noise, and enhances
important structural details, ensuring accurate feature detection in
subsequent stages of the project.

This work was implemented as part of the DCIT407 semester project on
*Corner and Shape Feature Extraction for Simple Image Analysis*.

---

## Responsibilities
The following preprocessing tasks were implemented:

- Grayscale conversion
- Noise reduction using Gaussian filtering
- Image thresholding
- Image normalization
- Batch preprocessing of multiple images

---

## Tools and Libraries Used
- **Python**
- **OpenCV (cv2)**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

## Preprocessing Pipeline
Each image undergoes the following steps:

1. **Grayscale Conversion**  
   Converts RGB images into a single intensity channel to simplify
   computation and reduce data complexity.

2. **Noise Reduction**  
   Gaussian blurring is applied to suppress noise that could introduce
   false corners or edges.

3. **Thresholding**  
   Otsu’s thresholding method is used to convert images into binary form,
   highlighting object boundaries for shape extraction.

4. **Normalization**  
   Pixel intensity values are scaled to a standard range to ensure
   consistency across images captured under different lighting
   conditions.

---

## Dataset
The preprocessing pipeline was applied to a set of **15 images** provided
by the project group. For clarity and readability, only a subset of
images is displayed in the notebook output, while preprocessing is
applied to all images.

---

## File Description
- `preprocessing.ipynb`  
  Jupyter Notebook containing the complete preprocessing implementation,
  visualizations, and explanations.

---

## Results
The preprocessing steps successfully enhance image quality and
structural features. Noise reduction and thresholding improve boundary
clarity, making the images suitable for reliable corner and shape
feature extraction using techniques such as Harris corner detection and
contour-based shape analysis.

---

## Conclusion
This preprocessing module provides clean, standardized image inputs for
the feature extraction stage of the project. The implemented techniques
play a critical role in improving the accuracy and robustness of corner
and shape detection algorithms.

---

## Author
**Norgbe Prince – Image Preprocessing Specialist**  
DCIT407 Group Project
