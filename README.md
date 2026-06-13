# Project-In-Image-Processing

# Image Processing Algorithms from Scratch

## Overview

The goal of the project was to implement fundamental image processing algorithms from scratch without using built-in image processing functions from OpenCV or scikit-image.

The project focuses on understanding the mathematical foundations of image transformations and filtering operations by manually implementing and validating the algorithms.

The implementation includes binarization, gamma correction, lookup tables (LUT), convolution, correlation, image filtering, and performance analysis.

---

## Project Objectives

The project consists of two major parts:

### Part 1 – Binarization and Gamma Correction

Implementation and evaluation of:

* Binary thresholding
* Gamma correction
* Lookup Table (LUT) optimization
* Accuracy comparison with OpenCV and scikit-image
* Performance benchmarking

### Part 2 – Linear Image Filtering

Implementation of a custom image filtering engine:

* Correlation
* Convolution
* Zero padding
* Blur filtering
* Sharpen filtering
* Synthetic image analysis
* Comparison with OpenCV filtering functions

---

## Technologies Used

* Python
* NumPy
* OpenCV
* Matplotlib
* scikit-image
* Google Colab

---

## Part 1 – Binarization and Gamma Correction

### Image Preprocessing

Several real-world images were converted to grayscale format (uint8, range 0–255).

For each image, the following statistics were calculated:

* Minimum intensity
* Maximum intensity
* Mean intensity
* Median intensity

### Binarization

Two independent implementations were developed:

#### Direct Method

A manual threshold comparison was implemented using a strict threshold operation equivalent to OpenCV's THRESH_BINARY.

#### LUT Method

A Lookup Table (LUT) was generated and applied to perform thresholding efficiently.

### Gamma Correction

Two approaches were implemented:

#### Direct Computation

Gamma correction was calculated manually using the standard formula:

Output = 255 × (Input / 255)^γ

#### LUT-Based Computation

A precomputed lookup table was used to accelerate repeated transformations.

### Accuracy Evaluation

The implementations were compared against:

* OpenCV
* scikit-image

Results showed:

* Pixel-wise identical outputs
* Maximum difference = 0
* Complete numerical agreement with library implementations

### Performance Evaluation

Execution times were measured and compared.

Key findings:

* LUT methods were significantly faster than direct implementations.
* OpenCV LUT functions were the fastest overall.
* Accuracy remained identical across all methods.

---

## Part 2 – Linear Image Filtering

### Custom Filtering Engine

A custom filtering function was implemented entirely from scratch.

Features:

* Arbitrary odd-sized kernels
* Correlation mode
* Convolution mode
* Zero padding
* Input validation
* Output clipping and rounding

### Supported Filters

#### Blur Filter

3×3 averaging kernel:

* Noise reduction
* Image smoothing

#### Sharpen Filter

Edge enhancement kernel:

* Detail enhancement
* Contrast improvement

### Synthetic Image Testing

To validate the implementation, several synthetic test images were generated:

* Centered square
* Checkerboard pattern
* Horizontal gradient

These test cases allowed precise evaluation of filter behavior.

### Real Image Testing

The filters were applied to multiple real photographs and compared against OpenCV implementations.

### Validation Against OpenCV

The custom implementation was compared to:

* cv2.filter2D()

Results demonstrated:

* Pixel-perfect agreement in most cases
* Maximum difference = 0
* Minor edge differences caused only by rounding effects

Visual inspection confirmed that the outputs were indistinguishable.

---

## Performance Analysis

A detailed benchmark was performed for all implemented algorithms.

The comparison included:

* Execution time
* Numerical accuracy
* Pixel-wise differences

Results showed:

* Custom implementations are mathematically correct.
* LUT optimization substantially improves performance.
* OpenCV implementations remain significantly faster due to low-level optimization.
* Manual implementations provide educational value and algorithmic understanding.

---

## Scientific Programming Principles

The project follows scientific programming practices:

* Modular function design
* Parameter validation
* Reproducible experiments
* Numerical verification
* Performance benchmarking
* Visualization of results
* Comparison against reference implementations

---

## Skills Demonstrated

This project demonstrates practical experience in:

* Image Processing
* Computer Vision Fundamentals
* Convolution and Correlation
* Lookup Tables (LUT)
* Image Enhancement
* Algorithm Design
* Performance Optimization
* Numerical Analysis
* Scientific Programming
* Python Development

---

## Results

The custom implementations successfully reproduced the behavior of OpenCV and scikit-image algorithms.

Main achievements:

* Pixel-perfect binarization implementation
* Pixel-perfect gamma correction implementation
* Custom convolution and correlation engine
* Accurate blur and sharpen filtering
* Extensive validation and benchmarking
