# Digital Restoration of Motion Blur

This repository presents a systematic study and implementation of digital image restoration techniques for mitigating **motion blur** and **atmospheric turbulence** effects. The focus is on classical deconvolution methods and their practical performance under different noise and degradation conditions.

---

## Project Overview

Image restoration is a fundamental problem in computer vision and signal processing. This project demonstrates how degraded images can be recovered using frequency-domain and spatial-domain filtering techniques.

### Goals

* **Modeling Image Degradation**
  Simulation of motion blur and atmospheric turbulence using Point Spread Functions (PSFs).

* **Restoration Techniques**
  Implementation and comparison of classical deconvolution methods:

  * Inverse filtering
  * Wiener filtering

* **Quantitative Evaluation**
  Performance assessment using standard image quality metrics:

  * Peak Signal-to-Noise Ratio (PSNR)
  * Structural Similarity Index Measure (SSIM)

---

## Repository Structure

```
.
├── filter_test_notebook.ipynb   # Main notebook with experiments and visualizations
├── README.md                    # Project documentation
├── Report.pdf                   # Report of the work (in Italian)
├── images                       # Folder with notebook output images
├── requirements.txt             # Needed libraries to execute the notebook
```

---

## Methodology

The restoration pipeline follows three main stages:

### 1. Degradation Model

A clean image is degraded using a **Point Spread Function (PSF)** to simulate:

* Motion blur
* Atmospheric turbulence

### 2. Restoration Process

The degraded image is restored using classical deconvolution techniques:

* Inverse filtering (frequency-domain reconstruction)
* Wiener filtering (regularized restoration under noise)

### 3. Evaluation

Restoration quality is analyzed both:

* **Qualitatively** (visual inspection)
* **Quantitatively** (PSNR and SSIM metrics)

---

## Results

The experiments highlight the fundamental trade-off in deconvolution methods:

* Improved detail recovery in low-noise scenarios
* Noise amplification in ill-conditioned inversions
* Strong dependence on SNR and PSF accuracy

Wiener filtering generally provides more stable and robust results compared to pure inverse filtering, especially under noisy conditions.

---

## Requirements

Install dependencies with:

```bash
pip install numpy pandas matplotlib scikit-image
```

---

## Author

**Lorenzo Pasini**

---

## Notes

This project is intended for educational and research purposes in digital image processing and inverse problems.
