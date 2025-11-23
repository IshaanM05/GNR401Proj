# GNR401Proj
# Hyperspectral Image Processing: Core Algorithms from Scratch

### Project Overview
This project implements fundamental image processing and enhancement algorithms applied to the **Indian Pines hyperspectral remote sensing dataset**.

The primary objective was to understand the mathematical foundations of these algorithms by implementing them **entirely from scratch using Python and NumPy**, without relying on high-level image processing libraries (such as OpenCV or Scikit-Image) for the core logic.

### Dataset
**Indian Pines** (AVIRIS sensor): A 145x145 pixel hyperspectral data cube with 220 spectral bands.
* **Processing approach:** The spectral bands were averaged to create a high-SNR grayscale representation for spatial processing.
* **Ground Truth:** Used to validate edge detection results against actual land-cover class boundaries.

### Implemented Algorithms
All algorithms were implemented using raw matrix manipulation and manual convolution loops:

1.  **Intensity Transformations:**
    * **Log Transform:** Enhances details in darker regions of the spectral image.
    * **Gamma Correction:** Non-linear brightness adjustment.
    * **Contrast Stretching:** Linear normalization to utilize the full dynamic range (0-255).
    * **Histogram Equalization:** Flattens the density of pixel intensities to maximize global contrast.

2.  **Spatial Filtering (Convolution):**
    * **Average (Mean) Filter:** Reduces noise via spatial smoothing.
    * **Sobel Edge Detection:** Calculates gradient magnitude using manually convolved Gx and Gy kernels.
