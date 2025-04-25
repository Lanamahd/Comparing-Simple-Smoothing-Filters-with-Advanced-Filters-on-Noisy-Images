# Comparing Simple Smoothing Filters with Advanced Filters on Noisy Images

## Overview

This project focuses on analyzing and comparing the performance of simple smoothing filters and advanced filters for image denoising. By evaluating their effectiveness on noisy images, the project highlights the trade-offs between noise reduction and detail preservation. The study uses images with various levels of complexity and detail, including natural high-detail images, low-detail images, and human-influenced high-detail images.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Filters and Techniques](#filters-and-techniques)
5. [Results and Analysis](#results-and-analysis)
6. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Steps to Run the Notebook](#steps-to-run-the-notebook)
7. [Example Output](#example-output)
8. [Conclusion](#conclusion)

---

## Introduction

Image denoising is a critical process in computer vision that aims to improve image quality by reducing noise while preserving important details. In this project, we compare simple smoothing filters, such as mean and median filters, with more advanced filters like Gaussian and bilateral filters. The comparison is conducted on images with varying levels of detail and complexity, sourced from the Berkeley Segmentation Dataset 500 (BSDS500).

---

## Features

- **Image Categories**:
  - *Natural High-Detail Images*: Images with intricate textures (e.g., animal fur, flowers, coral reefs).
  - *Natural Low-Detail Images*: Images with simpler, uniform backgrounds (e.g., open skies, grassy fields).
  - *Human-Influenced High-Detail Images*: Man-made scenes with complex textures and architectural details.

- **Filters Used**:
  - Mean Filter
  - Median Filter
  - Gaussian Filter
  - Bilateral Filter

- **Evaluation Metrics**:
  - Visual comparison of filtered images.
  - Quantitative metrics to assess noise reduction and detail preservation.

- **Visualization**:
  - Display of original, noisy, and filtered images for side-by-side comparison.

---

## Dataset

The project uses the **Berkeley Segmentation Dataset 500 (BSDS500)**, which includes 200 training images. A subset of 20 images was selected for testing, covering various categories of high and low detail. The dataset is stored in the `dataset/` directory of the repository.

---

## Filters and Techniques

1. **Simple Smoothing Filters**:
   - **Mean Filter**: Averages pixel values within a kernel to reduce noise.
   - **Median Filter**: Replaces each pixel with the median value of its neighbors to preserve edges.

2. **Advanced Filters**:
   - **Gaussian Filter**: Applies a Gaussian kernel to smooth images while maintaining structure.
   - **Bilateral Filter**: Combines spatial and intensity information for edge-preserving smoothing.

---

## Results and Analysis

- **Natural High-Detail Images**:
  - The bilateral filter outperforms others by preserving intricate textures while reducing noise.
  
- **Natural Low-Detail Images**:
  - Gaussian and mean filters perform well due to the uniform backgrounds.

- **Human-Influenced High-Detail Images**:
  - Advanced filters like bilateral filters are better at maintaining architectural details.

The results are visualized in the notebook, showcasing the differences between filters and their impact on image quality.

---

## Getting Started

### Prerequisites

- Python 3.8 or later
- Jupyter Notebook
- Required Python libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `opencv-python`
  - `Pillow`

Install the required libraries using:
    ```bash
    pip install numpy pandas matplotlib seaborn opencv-python Pillow

### Steps to Run the Notebook
1. Clone the repository:

    ```bash
    git clone https://github.com/Lanamahd/Comparing-Simple-Smoothing-Filters-with-Advanced-Filters-on-Noisy-Images.git
    cd Comparing-Simple-Smoothing-Filters-with-Advanced-Filters-on-Noisy-Images

2. Open the Jupyter Notebook:

    ```bash
    jupyter notebook assignment1.ipynb

3. Follow the cells in the notebook to execute the analysis.

---

## Example Output

### Example Visualization

#### Natural High-Detail Image
  - **Original Image**: Displays intricate textures (e.g., red flower petals).
  - **Noisy Image**: Introduced Gaussian noise.
  - **Filtered Images**:
    - Mean Filter: Blurs the image, losing fine details.
    - Median Filter: Preserves edges but reduces texture sharpness.
    - Gaussian Filter: Smooths noise while maintaining structure.
    - Bilateral Filter: Best performance, preserving edges and textures.

---

## Conclusion
This project demonstrates the strengths and weaknesses of various filters in image denoising. While simple smoothing filters are computationally efficient, advanced filters like the bilateral filter excel in preserving details in complex images. The comparison serves as a valuable reference for selecting appropriate filters based on image characteristics and application requirements.
