# Computer Vision Course – Day 1 Lab

Image processing fundamentals and data augmentation with OpenCV, completed in Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JanaHAlharbi/Computer-Vision-Course---Day1-CoLab/blob/main/CV_Day1_Lab_Student.ipynb)

## Overview

This lab takes a single image and walks through the basic steps used to prepare images for a computer vision model. It is split into two parts: core image processing techniques, and nine data augmentation techniques that create new training examples from one original image.

## Part 1: Image Processing

| Technique | What it does |
|---|---|
| Grayscale conversion | Reduces the image from 3 colour channels to 1, using 3x fewer numbers |
| Canny edge detection | Blurs the image with a 5 x 5 Gaussian window, then finds edges using thresholds 80 and 180 |
| Preprocessing for a CNN | Resizes to 224 x 224, scales pixels to 0..1, and standardizes with the ImageNet mean and standard deviation |

## Part 2: Data Augmentation

| # | Technique | Description |
|---|---|---|
| 1 | Horizontal flip | Mirrors the image left to right |
| 2 | Rotation | Rotates by a small angle (15 degrees) around the centre |
| 3 | Crop and zoom | Keeps 70% of the image and resizes it back to full size |
| 4 | Brightness | Adds 60 to every pixel, clipped to 0..255 |
| 5 | Contrast | Stretches pixel values away from the mean by a factor of 1.6 |
| 6 | Saturation | Multiplies the saturation channel in HSV by 1.8 |
| 7 | Gaussian noise | Adds random noise with a standard deviation of 25 |
| 8 | Gaussian blur | Applies a strong 11 x 11 blur |
| 9 | Cutout | Hides a random box covering 25% of the height and width |

The final cell shows the original image next to all nine variations in one gallery.

## Tools

- Python 3
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Google Colab

## How to Run

1. Click the **Open in Colab** badge above.
2. Choose **Runtime > Run all**.
3. Scroll through the notebook to see the output of each technique.

## What I Learned

- An image is an array of numbers, so slicing and arithmetic work on it directly.
- Pixel values must be converted to a wider type before arithmetic, then clipped to 0..255 to avoid overflow.
- Blurring before edge detection stops noise from being detected as edges.
- Models trained on ImageNet expect a fixed input size and standardized pixel values.
- Augmentation creates varied training examples without collecting new images.

## Author

[@JanaHAlharbi](https://github.com/JanaHAlharbi)
