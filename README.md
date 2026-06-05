# 🖼️ Image Processing Lab — OpenCV & Python

<div align="center">
  <img src="https://github.com/user-attachments/assets/6068638e-e9d3-48bc-a4aa-b868d8512d23" width="100%" alt="Header Image" />
</div>

<br />

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-4CAF50?style=for-the-badge)

</div>

A hands-on computer vision lab implementing fundamental image processing techniques using **OpenCV**, **NumPy**, and **Matplotlib** in Google Colab. Covers RGB channel decomposition, grayscale conversion, binary thresholding, and image scaling using multiple interpolation methods.

---

## 📌 Core Features & Topics

| Topic | Description | Technical Implementation |
| :--- | :--- | :--- |
| **RGB Channel Separation** | Splitting an image into R, G, B planes individually | Array slicing & `cv2.split()` |
| **Grayscale Conversion** | Converting RGB to grayscale matrix | `cv2.COLOR_RGB2GRAY` |
| **Binary Thresholding** | Manual, Otsu's, and mean-based binarization | `cv2.THRESH_OTSU` & Custom NumPy |
| **Image Scaling (Up)** | Upscaling with mathematical precision | Linear, Cubic, & Nearest interpolation |
| **Image Scaling (Down)** | Downscaling to compress spatial dimensions | Area interpolation |
| **Error Measurement** | Quantifying reconstruction fidelity loss | Mean Squared Error ($MSE$) |

---

## 🧪 Detailed Techniques & Pipelines

### 1. RGB Plane Decomposition
* Extracted individual **Blue**, **Green**, and **Red** channels using both array slicing and `cv2.split()`.
* Visualized each channel as a grayscale plane to analyze pixel intensity distributions.

### 2. Grayscale Conversion
* Converted the original RGB image to grayscale.
* Tracked structural metadata changes by printing updated height and width shape tuples post-conversion.

### 3. Binary Thresholding (3 Methods)
* **Manual Threshold (MT):** Fixed hard thresholding applied at pixel value 128.
* **Otsu's Method:** Automatic optimal threshold calculation minimizing intra-class variance.
* **Mean-based Threshold:** Dynamically computed as $\frac{\text{min} + \text{max}}{2}$ using NumPy, applied via pixel-by-pixel iterations.

### 4. Image Scaling & Reconstruction Evaluation
* **Upscaling (1.5x):** Comparative analysis between Linear, Cubic, and Nearest Neighbor interpolation.
* **Downscaling (0.667x):** Applied Area-based interpolation on the upscaled image to return to baseline resolution.
* **Reconstruction Loss ($MSE$):** Quantified quality loss between original and downscaled image using:
  $$MSE = \frac{1}{mn}\sum_{i=0}^{m-1}\sum_{j=0}^{n-1}[I(i,j) - K(i,j)]^2$$

---

## 📊 Visual Laboratories & Pipeline Outputs

### Channel Separation & Conversions
<table border="0">
  <tr>
    <td width="50%" align="center"><b>Original & Color Spaces</b></td>
    <td width="50%" align="center"><b>Binary Thresholding Results</b></td>
  </tr>
  <tr>
    <td valign="top"><img src="https://github.com/user-attachments/assets/52aa8be9-caac-45bc-bcdc-bf7b33c654bc" alt="Original Matrix" /></td>
    <td valign="top"><img src="https://github.com/user-attachments/assets/6ae12922-18bc-430b-858f-cef88bf8894e" alt="Thresholding Comparisons" /></td>
  </tr>
</table>

### Mathematical Spatial Transformations
<table border="0">
  <tr>
    <td width="50%" align="center"><b>Upscaling Interpolation Performance</b></td>
    <td width="50%" align="center"><b>Downscaling & Structural Loss</b></td>
  </tr>
  <tr>
    <td valign="top"><img src="https://github.com/user-attachments/assets/2f381e89-f67c-48dd-a87e-2e2ba88f21fe" alt="Upscaling Matrix" /></td>
    <td valign="top"><img src="https://github.com/user-attachments/assets/08b55c3a-5e35-4b18-a249-6e39352294c5" alt="Downscaling Metrics" /></td>
  </tr>
</table>

### Numerical Matrix Data & Matrix Proofs
<p align="center">
  <img src="https://github.com/user-attachments/assets/6be455d1-97f2-4632-b32a-f7c897fe9b08" width="32%" />
  <img src="https://github.com/user-attachments/assets/cacd5a31-64cc-4236-bf43-be0cdfcbd01b" width="32%" />
  <img src="https://github.com/user-attachments/assets/25df563d-8e37-499e-bdcf-688373142050" width="32%" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/697c4bb2-3ebb-4490-8f83-9db583f85fc1" width="45%" />
  <img src="https://github.com/user-attachments/assets/5c97683c-7ecb-49d2-a73c-92bccd48e3e9" width="45%" />
</p>

---

## 🛠️ Environment Configuration & Code Architecture

```python
import cv2          # Image manipulation, transformations, and thresholding algorithms
import numpy as np  # N-dimensional matrix operations & element-wise linear algebra
import matplotlib.pyplot as plt  # High-fidelity data visualization
from google.colab import files   # Runtime local file system interfacing
```
# 📁 Repository Blueprint
```
image-processing-lab/
│
├── image_processing_lab.ipynb   # Primary Jupyter/Colab Interactive Workspace
└── README.md                    # Technical System Documentation
```
