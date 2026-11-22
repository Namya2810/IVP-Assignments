# Image and Video Processing (IVP) — Assignments

Solutions to the 10 IVP lab assignments, written in Python as Jupyter notebooks.
Each folder contains one notebook. Every question is written in a text cell, followed directly by its code, output images and observations.

| # | Topic | Notebook |
|---|---|---|
| 1 | Grayscale to binary image (mean threshold / user threshold) | [Assignment_01.ipynb](Assignment-01/Assignment_01.ipynb) |
| 2 | RGB to grayscale (mean of planes / user weights) | [Assignment_02.ipynb](Assignment-02/Assignment_02.ipynb) |
| 3 | Image border (padding) and image complement — binary & grayscale | [Assignment_03.ipynb](Assignment-03/Assignment_03.ipynb) |
| 4 | Log transform, power-law (gamma) transform, contrast stretching / intensity slicing | [Assignment_04.ipynb](Assignment-04/Assignment_04.ipynb) |
| 5 | Smoothing: averaging, weighted max(\|x\|,\|y\|), Gaussian filters with user-chosen size, sigma and padding | [Assignment_05.ipynb](Assignment-05/Assignment_05.ipynb) |
| 6 | Histogram equalization and histogram matching | [Assignment_06.ipynb](Assignment-06/Assignment_06.ipynb) |
| 7 | Sharpening: Laplacian, Sobel, Canny, unsharp masking (Gaussian 5×5, σ = 3) | [Assignment_07.ipynb](Assignment-07/Assignment_07.ipynb) |
| 8 | Uniform, Gaussian, Erlang, exponential and Rayleigh noise from their PDFs, compared with `imnoise` | [Assignment_08.ipynb](Assignment-08/Assignment_08.ipynb) |
| 9 | Local binary pattern; Wiener, median, Gaussian and bilateral denoising | [Assignment_09.ipynb](Assignment-09/Assignment_09.ipynb) |
| 10 | Adaptive median filter vs. median filter (PSNR); Otsu thresholding | [Assignment_10.ipynb](Assignment-10/Assignment_10.ipynb) |

## Notes
- The core algorithms (thresholding, colour conversion, padding, intensity transforms, convolution, histogram equalization and matching, noise generation, LBP, Wiener filter, adaptive median filter, Otsu) are implemented from scratch with NumPy. Where possible they are checked against the OpenCV / scikit-image built-ins.
- Standard test images from scikit-image (cameraman, moon, astronaut, coins) are used. To use your own image, set `IMAGE_PATH` at the top of a notebook.
- Values the assignments ask the user to enter (threshold, gamma, filter size, padding method, window sizes, …) are read with `input()`. Pressing Enter uses the default value shown in the prompt. The saved outputs were produced with these defaults.
- MATLAB's `imnoise` corresponds to `skimage.util.random_noise` in Python.

## How to run
```bash
pip install -r requirements.txt
jupyter notebook
```
