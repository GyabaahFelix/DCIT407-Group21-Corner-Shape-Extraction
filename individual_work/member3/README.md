
# Corner Detection Module — DCIT407 Semester Project

## Overview

This module focuses on detecting and analyzing corner features in images using two classical computer vision algorithms: **Harris Corner Detection** and **Shi–Tomasi Corner Detection**. The notebook demonstrates how preprocessing and parameter tuning affect corner detection performance and stability.

The notebook forms part of the **DCIT407 Semester Project** on corner and shape feature extraction and represents Awuah Jim Isaac's assigned task in the group project.

---

## Features Implemented

1. **Preprocessing Integration**
   - Conversion of images to **grayscale**.
   - **Gaussian smoothing** to reduce noise and stabilize corner detection.
   - Ensures all subsequent corner detection algorithms operate on clean and consistent image data.

2. **Harris Corner Detection**
   - Implements Harris corner detection using OpenCV’s `cornerHarris` function.
   - Calculates the **corner response function**:  
     $$
     R = \det(M) - k (\mathrm{trace}(M))^2
     $$
   - Includes **parameter sensitivity analysis** by varying `k` to demonstrate how corner counts change.
   - Highlights both weak and strong corners in processed images.

3. **Shi–Tomasi Corner Detection**
   - Implements Shi–Tomasi detection using OpenCV’s `goodFeaturesToTrack()` function.
   - Uses the eigenvalues of the structure tensor to select strong corners:  
     $$
     R = \min(\lambda_1, \lambda_2)
     $$
   - Performs **parameter sensitivity analysis** for `qualityLevel` and `max_corners` to observe algorithm behavior.
   - Produces fewer but stronger and more stable corners compared to Harris.

4. **Comparison of Both Methods**
   - Processes all images in the `images/` directory.
   - Computes **Harris corner count**, **Shi–Tomasi corner count**, and the **difference between them**.
   - Provides quantitative comparison and discussion on algorithm behavior.

5. **Parameter Sensitivity Analysis**
   - Demonstrates how changing parameters (`k` for Harris, `qualityLevel` for Shi–Tomasi) affects the number and quality of detected corners.
   - Helps identify optimal parameter values for stable and meaningful feature detection.

6. **Observations and Conclusions**
   - Harris detects more corners, including weak points, making it sensitive to noise.
   - Shi–Tomasi selects fewer but stronger corners, making it more robust for practical applications.
   - Preprocessing and careful parameter tuning significantly improve detection stability.


