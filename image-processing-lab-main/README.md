# 🖼️ Image Processing Lab — OpenCV & Python
<img width="655" height="510" alt="image" src="https://github.com/user-attachments/assets/52aa8be9-caac-45bc-bcdc-bf7b33c654bc" />
<img width="1142" height="354" alt="image" src="https://github.com/user-attachments/assets/6068638e-e9d3-48bc-a4aa-b868d8512d23" />
<img width="663" height="609" alt="image" src="https://github.com/user-attachments/assets/6ae12922-18bc-430b-858f-cef88bf8894e" />
<img width="656" height="595" alt="image" src="https://github.com/user-attachments/assets/2f381e89-f67c-48dd-a87e-2e2ba88f21fe" />
<img width="656" height="595" alt="image" src="https://github.com/user-attachments/assets/08b55c3a-5e35-4b18-a249-6e39352294c5" />
<img width="478" height="435" alt="download (1)" src="https://github.com/user-attachments/assets/6be455d1-97f2-4632-b32a-f7c897fe9b08" />
<img width="831" height="269" alt="download (2)" src="https://github.com/user-attachments/assets/cacd5a31-64cc-4236-bf43-be0cdfcbd01b" />
<img width="831" height="269" alt="download (3)" src="https://github.com/user-attachments/assets/25df563d-8e37-499e-bdcf-688373142050" />
<img width="557" height="269" alt="download (4)" src="https://github.com/user-attachments/assets/697c4bb2-3ebb-4490-8f83-9db583f85fc1" />
<img width="763" height="374" alt="sd" src="https://github.com/user-attachments/assets/5c97683c-7ecb-49d2-a73c-92bccd48e3e9" />

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange?logo=googlecolab&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A hands-on computer vision lab implementing fundamental image processing techniques using **OpenCV**, **NumPy**, and **Matplotlib** in Google Colab. Covers RGB channel decomposition, grayscale conversion, binary thresholding, and image scaling using multiple interpolation methods.

---

## 📌 Topics Covered

| Topic | Description |
|-------|-------------|
| RGB Channel Separation | Splitting an image into R, G, B planes individually |
| Grayscale Conversion | Converting RGB to grayscale using `cv2.COLOR_RGB2GRAY` |
| Binary Thresholding | Manual threshold, Otsu's method, and mean-based thresholding |
| Image Scaling (Up) | Upscaling using Linear, Cubic, and Nearest interpolation |
| Image Scaling (Down) | Downscaling using Area interpolation |
| Error Measurement | Mean Square Error (MSE) between original and scaled images |

---

## 🧪 Techniques Implemented

### 1. RGB Plane Decomposition
- Extracted individual **Blue**, **Green**, and **Red** channels using both array slicing and `cv2.split()`
- Visualized each channel as a grayscale plane

### 2. Grayscale Conversion
- Converted the original RGB image to grayscale
- Printed updated height and width after conversion

### 3. Binary Thresholding (3 Methods)
- **Manual Threshold (MT):** Fixed threshold at pixel value 128
- **Otsu's Method:** Automatic optimal threshold using `cv2.THRESH_OTSU`
- **Mean-based Threshold:** Computed as `(min + max) / 2` using NumPy, applied pixel-by-pixel

### 4. Image Scaling
- **Upscaling (1.5x):** Linear, Cubic, and Nearest Neighbor interpolation
- **Downscaling (0.667x):** Area interpolation on the upscaled image
- **MSE Calculation:** Quantified quality loss between original and downscaled image

---

## 🛠️ Libraries Used

```python
import cv2          # Image reading, conversion, thresholding, resizing
import numpy as np  # Array operations, pixel-level processing
import matplotlib.pyplot as plt  # Visualization
from google.colab import files   # File upload in Colab
```

---

## 🚀 How to Run

1. Open the notebook in Google Colab using the badge at the top
2. Run all cells in order (`Runtime → Run all`)
3. When prompted, upload any RGB image from your device
4. All outputs — channel planes, thresholded images, scaled images — will display inline

---

## 📊 Sample Outputs

The notebook generates the following visualizations:
- Original RGB image
- Blue, Green, Red channel planes (grayscale)
- Grayscale version of the image
- Binary images using MT, Otsu, and Mean threshold — side by side
- Upscaled images using Linear, Cubic, Nearest — side by side
- Original vs Downscaled comparison
- Printed MSE value for quality comparison

---

## 📐 Key Observations

- **Otsu's thresholding** automatically finds the optimal threshold and generally outperforms a fixed value like 128 for natural images
- **Cubic interpolation** produces the smoothest upscaled result but is computationally heavier
- **Nearest Neighbor** is the fastest but produces blocky/pixelated edges
- **MSE** increases when downscaling due to information loss during compression

---

## 📁 File Structure

```
image-processing-lab/
│
├── image_processing_lab.ipynb   # Main Colab notebook
└── README.md                    # Project documentation
```

---

## 🙋 Author

**Aldrin Johny**  
B.Tech Student | Aspiring AI/ML Engineer  
[![GitHub](https://img.shields.io/badge/GitHub-aldrinjohny--ai-black?logo=github)](https://github.com/aldrinjohny-ai)

---

## 📚 References

- [OpenCV Documentation](https://docs.opencv.org/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Otsu's Thresholding — OpenCV Tutorial](https://docs.opencv.org/4.x/d7/d4d/tutorial_py_thresholding.html)

---

> 💡 *This lab is part of my Computer Vision learning journey. More CV projects coming soon!*
