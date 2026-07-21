# Retinal Vessel Segmentation using Mathematical Morphology

> **A research-oriented implementation of retinal blood vessel segmentation using mathematical morphology, custom grayscale morphological operators, multi-scale vessel enhancement, and morphological reconstruction for biomedical image analysis.**

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-orange.svg)
![Medical Imaging](https://img.shields.io/badge/Application-Medical%20Imaging-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

# Overview

This repository presents a **research-oriented implementation** of retinal blood vessel segmentation based entirely on **classical mathematical morphology** and low-level image processing techniques.

Unlike many retinal vessel segmentation approaches that rely on deep neural networks, this project demonstrates that carefully designed morphological operators can produce highly interpretable and reliable vessel segmentation while preserving complete algorithmic transparency.

The implementation emphasizes **algorithmic understanding**, **reproducibility**, and **from-scratch implementation** of fundamental image processing techniques instead of relying on high-level morphology libraries.

The complete segmentation pipeline was developed in **Spring 2025** during the **Advanced Digital Image Processing** course at **Shiraz University** and has subsequently been refactored into a modular research repository following modern software engineering and reproducible research practices.

---

# Motivation

Retinal vascular analysis plays an essential role in the diagnosis of numerous systemic and ophthalmic diseases, including

* Diabetic Retinopathy
* Hypertensive Retinopathy
* Glaucoma
* Cardiovascular Disease
* Stroke Risk Assessment

Reliable vessel segmentation is a fundamental preprocessing step for quantitative retinal image analysis, enabling the extraction of vascular biomarkers such as

* Vessel caliber
* Vessel density
* Vessel tortuosity
* Branching patterns
* Arteriolar-to-venular ratio

This project demonstrates how **classical mathematical morphology** remains an effective and interpretable solution for biomedical image segmentation.

---

# Key Features

* Research-oriented biomedical image processing pipeline
* From-scratch grayscale morphology implementation
* Manual structuring element generation
* Custom grayscale erosion and dilation
* Custom grayscale opening and closing
* Manual binary morphology
* Background estimation via morphological opening
* Flat-field illumination correction
* Multi-scale white top-hat enhancement
* Manual contrast normalization
* Custom Otsu thresholding implementation
* Marker-based morphological reconstruction
* Connected component area opening
* Retina field-of-view masking
* Publication-quality visualizations
* Fully implemented in Python without high-level morphology libraries

---

# Repository Structure

```text
retinal-vessel-segmentation-using-mathematical-morphology

│
├── data/
│   └── sample-image.jpg
│
├── docs/
│   └── Report.pdf
│
├── notebooks/
│   └── Retinal_Vessel_Segmentation.ipynb
│
├── results/
│
├── README.md
├── requirements.txt
├── LICENSE
└── CITATION.cff
```

---

# Dataset

## Retinal Fundus Image

The project uses a color retinal fundus image for vessel segmentation.

Image characteristics include

* RGB retinal fundus photograph
* Green channel enhancement
* High-resolution vascular structures
* Biomedical imaging application
* Binary vessel mask generation

---

# Methodology

## Vessel Segmentation Pipeline

```text
Input Fundus Image
        │
        ▼
Green Channel Extraction
        │
        ▼
Large-Scale Morphological Opening
        │
        ▼
Background Estimation
        │
        ▼
Flat-Field Correction
        │
        ▼
Manual Contrast Normalization
        │
        ▼
Image Inversion
        │
        ▼
Multi-Scale White Top-Hat Enhancement
        │
        ▼
Merged Vessel Enhancement
        │
        ▼
Custom Otsu Thresholding
        │
        ▼
Binary Vessel Mask
        │
        ▼
Marker Generation
        │
        ▼
Morphological Reconstruction
        │
        ▼
Morphological Closing
        │
        ▼
Morphological Opening
        │
        ▼
Connected Component Area Opening
        │
        ▼
Retina ROI Extraction
        │
        ▼
Final Vessel Segmentation
```

---

# Implemented Algorithms

## Mathematical Morphology

The following grayscale morphological operators were implemented **from scratch**:

* Disk structuring element generation
* Grayscale erosion
* Grayscale dilation
* Grayscale opening
* Grayscale closing

---

## Binary Morphology

* Binary erosion
* Binary dilation
* Binary opening
* Binary closing

---

## Vessel Enhancement

* Background estimation
* Flat-field correction
* Contrast normalization
* Multi-scale white top-hat transformation
* Image inversion
* Multi-scale enhancement fusion

---

## Segmentation

* Custom Otsu thresholding
* Binary vessel segmentation

---

## Morphological Reconstruction

* Marker generation
* Binary reconstruction
* Hysteresis propagation

---

## Post-processing

* Area opening using connected components
* Retina field-of-view masking
* Noise removal
* Vessel refinement

---

# Experimental Results

## Vessel Enhancement

The multi-scale white top-hat strategy effectively enhances vessels with different diameters while suppressing slowly varying retinal background illumination.

Visualization includes

* Green channel
* Background corrected image
* Multi-scale Top-Hat responses
* Combined enhancement

---

## Binary Segmentation

Global thresholding using a manually implemented Otsu algorithm successfully separates vessel structures from retinal background.

Outputs include

* Otsu threshold
* Binary vessel mask
* Final cleaned segmentation

---

## Morphological Refinement

The reconstruction and cleanup stages significantly improve segmentation quality by

* reconnecting fragmented vessels,
* removing isolated false positives,
* preserving thin vascular branches,
* refining vessel continuity.

---

# Design Highlights

Compared with conventional morphology-based implementations, this repository introduces several engineering improvements:

* Complete grayscale morphology implemented from scratch
* No reliance on OpenCV morphology functions
* Multi-scale vessel enhancement strategy
* Manual histogram-based Otsu optimization
* Morphological reconstruction implementation
* Connected-component area filtering
* Research-quality modular pipeline
* Fully interpretable segmentation workflow

---

# Technologies

* Python
* OpenCV
* NumPy
* Matplotlib

---

# Installation

```bash
git clone https://github.com/hannah-fathi/retinal-vessel-segmentation-using-mathematical-morphology.git

cd retinal-vessel-segmentation-using-mathematical-morphology

pip install -r requirements.txt
```

---

# Quick Start

Launch the notebook

```bash
notebooks/Retinal_Vessel_Segmentation.ipynb
```

Execute each processing stage sequentially to reproduce the complete vessel segmentation pipeline.

---

# Repository Highlights

* Research-oriented implementation
* Biomedical computer vision application
* Classical mathematical morphology
* Fully interpretable segmentation pipeline
* From-scratch grayscale morphology
* Multi-scale vessel enhancement
* Custom Otsu thresholding
* Morphological reconstruction
* Reproducible experiments
* Publication-quality visualization

---

# Current Limitations

The current implementation assumes

* Single retinal fundus image
* Healthy image acquisition conditions
* Fixed imaging protocol
* Morphology-based segmentation only
* No supervised learning

---

# Future Work

Potential extensions include

* DRIVE dataset evaluation
* STARE dataset evaluation
* CHASE_DB1 dataset evaluation
* Quantitative segmentation metrics (Dice, IoU, Sensitivity, Specificity)
* Skeleton extraction
* Vessel width estimation
* Artery–vein classification
* Graph-based vascular analysis
* Deep learning comparison (U-Net, Attention U-Net)
* Hybrid morphology–deep learning framework

---

# Citation

If you use this repository for research or education, please consider citing:

```bibtex
@software{fathi2026retinal,
  author  = {Hannah Fathi},
  title   = {Retinal Vessel Segmentation using Mathematical Morphology},
  year    = {2026},
  url     = {https://github.com/hannah-fathi/retinal-vessel-segmentation-using-mathematical-morphology}
}
```

---

# Acknowledgements

This project was originally developed during **Spring 2025** as part of the **Advanced Digital Image Processing** course at **Shiraz University**.

The original coursework has been substantially refactored into a research-oriented implementation emphasizing reproducibility, modular software architecture, and interpretable biomedical image analysis.

---

# Research Areas

* Biomedical Computer Vision
* Medical Image Processing
* Retinal Image Analysis
* Mathematical Morphology
* Vessel Segmentation
* Image Enhancement
* Feature Extraction
* Classical Computer Vision
* Explainable Image Processing
* Computer-Aided Diagnosis (CAD)

---

# License

This project is released under the **MIT License**.

---

# Author

**Hannah Fathi**

** M.Sc. Student in Artificial Intelligence and Robotics**

**Spring 2025** 

### Research Interests

* Computer Vision
* Medical AI
* Medical Image Analysis
* Biomedical Computer Vision
* Remote Sensing
* Explainable AI
* Deep Learning
* Image Processing
