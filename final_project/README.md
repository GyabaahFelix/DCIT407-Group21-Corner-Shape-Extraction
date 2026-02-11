# DCIT407 – Corner and Shape Feature Extraction for Simple Image Analysis

## Project Overview

This project implements **corner and shape feature extraction techniques** for simple image analysis using Python. The goal is to demonstrate how fundamental image processing methods can be used to detect important visual features such as edges, corners, and geometric shapes in real-world images.

The project is developed as part of the **DCIT407 Semester Project** and is implemented using **OpenCV, NumPy, and Matplotlib** in a Jupyter/Google Colab notebook.

This notebook presents a complete pipeline that includes:

* Image loading and preprocessing
* Corner detection
* Edge detection
* Shape detection and classification
* Visualization and comparison of results
* Discussion and analysis

---

## Objectives

The main objectives of this project are to:

* Understand the theory behind corner and shape feature extraction
* Implement feature detection algorithms in Python
* Apply the algorithms to real images
* Analyze and interpret the results
* Demonstrate practical applications of image feature extraction

---

## Technologies Used

* **Python 3**
* **OpenCV** – image processing and feature detection
* **NumPy** – numerical computations
* **Matplotlib** – visualization
* **Google Colab / Jupyter Notebook** – development environment

---

## Project Structure

```
DCIT407-Group21/
│
├── final_project/
│   └── DCIT407_Group21_Corner_Shape_Feature_Extraction.ipynb
│
├── individual_work/
│   └── (member contributions)
│
└── images/
    └── sample images used for testing
```

The main notebook integrates all modules into a unified workflow.

---

## Methodology

The notebook follows a structured image processing pipeline:

### 1. Image Acquisition

Real or publicly available images are loaded and prepared for analysis.

### 2. Image Preprocessing

Images are converted to grayscale and filtered to reduce noise and improve detection accuracy.

### 3. Corner Detection

Corner detection algorithms such as:

* Harris Corner Detection
* Shi-Tomasi Corner Detection

are used to identify significant feature points.

### 4. Edge Detection

Canny edge detection is applied to highlight boundaries and structural details.

### 5. Shape Detection

Contours are extracted and analyzed to classify simple geometric shapes such as:

* Triangles
* Rectangles/Squares
* Circles

### 6. Visualization

Original and processed images are displayed side-by-side for comparison.

---

## How to Run the Notebook

### Option 1: Google Colab

1. Upload the notebook to Google Colab
2. Upload the sample images to the Colab environment
3. Run all cells sequentially

### Option 2: Local Jupyter Environment

1. Install required libraries:

```
pip install opencv-python numpy matplotlib
```

2. Place images inside the `images/` folder
3. Open and run the notebook in Jupyter

---

## Results

The notebook produces:

* Visual overlays of detected corners
* Edge maps of input images
* Detected shapes with labels
* Comparative visualizations

These outputs demonstrate how feature extraction techniques can identify structural information in images.

---

## Applications

Corner and shape feature extraction has many real-world uses, including:

* Object recognition
* Robotics and navigation
* Computer vision systems
* Medical image analysis
* Surveillance and security
* Industrial inspection

---

## Strengths and Limitations

### Strengths

* Efficient and interpretable feature detection
* Works well on clear geometric structures
* Simple and computationally fast

### Limitations

* Sensitive to noise and lighting variations
* Performance decreases on complex or cluttered images
* Requires parameter tuning

---

## Conclusion

This project demonstrates how corner and shape feature extraction techniques can be implemented and applied to simple image analysis tasks. The notebook provides a clear and modular pipeline that highlights both the theoretical and practical aspects of image feature detection.

The project reinforces key concepts in image processing and shows how they can be used in real-world applications.

---

## Contributors

DCIT407 – Group 21

All group members contributed to the development, implementation, and documentation of this project.

---

## License

This project is developed for academic purposes as part of the DCIT407 course.
