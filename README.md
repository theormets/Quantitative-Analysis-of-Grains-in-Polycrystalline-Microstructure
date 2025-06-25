# Quantitative Analysis of Geometrical and Topological Features of Grains in Polycrystalline Microstructure

This project presents a robust and automated pipeline for the detection and quantitative analysis of grain structures in polycrystalline microstructure images. It integrates deep learning (YOLOv5) with computational geometry and graph theory to extract meaningful geometrical and topological metrics from metallographic data.

---

## 📌 Overview

Grain morphology is a critical factor influencing the mechanical and physical properties of polycrystalline materials. Manual quantification of these features is time consuming and prone to error. This tool automates the entire analysis process ,from image input to the final quantitative grain statistics  ensuring scalability, consistency, and accuracy.

---

## 🔧 How it works

- **Accurate Detection of Triple Junctions (TJs)**:
   In uploaded microstructure images uses a custom-trained YOLOv5 model to identify critical junctions where three grain boundaries converge.
- **Graph-Theoretic Modeling of Grain Boundaries**:
   Converts edge-skeletonized images into pixel-based graphs to enable path tracing and topological analysis.
- **Polygonal Grain Reconstruction**:
   Reconstructs valid, closed-loop grain geometries from TJ-to-TJ paths, ensuring non-overlapping, non-self-intersecting polygons.
- **Quantitative Feature Extraction**:
   Computes key metrics such as number of sides, area, neighboring grains, average neighbor area and  and predicts grain growth or shrinkage based on the von Neumann-Mullins relation for each grain.
- **Visual and Data-Driven Insights**:
   Generates annotated outputs for both qualitative assessment and CSV-based quantitative evaluation.


---

## 🔍 Key Features

- **Deep Learning Integration**: Uses a custom-trained YOLOv5 model to localize triple junctions.
- **Graph-Based Path Tracing**: Edge pixels are modeled as a graph for shortest path tracing between TJs.
- **Polygon Validation**: Ensures accurate, closed, non-overlapping, and non-self-intersecting grains.
- **Quantitative Metrics**: Exports detailed CSV reports of grain-wise measurements.
- **High-Quality Visual Output**: Produces annotated images of all grains, polygons, and junctions.

---

## 🧱 Prerequisites

### Dependencies
- Python ≥ 3.8
- OpenCV
- NumPy
- SciPy
- NetworkX
- scikit-image
- Ultralytics YOLOv5

### Pre-trained YOLOv5 Model: 
   A custom-trained model (best.pt) for TJ detection

---

## 🚀 Running the Colab Notebook

- This notebook allows you to upload images from your computer using Colab's upload button.
- Alternatively, you can place images in `input_samples/` and adjust the code accordingly.

---
## 📣 Credits
- **Developed by**: Meghna Dineskumar Adsule

- **Institution**: Indian Institute Of Technology (BHU) Varanasi

- **Project**: Quantitative Analysis of Geometrical and Topological Features of Grains in Polycrystalline Microstructure
