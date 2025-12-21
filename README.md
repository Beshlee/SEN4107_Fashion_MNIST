# Fashion-MNIST Classification and Deep Visualization Analysis

This repository contains the final project for the **SEN4107 Deep Learning** course. The project explores image classification on the Fashion-MNIST dataset using two distinct Convolutional Neural Network (CNN) architectures and provides a deep visualization of internal model representations.

## Project Overview

The project is structured into four main phases:
1. **Phase 1: Preparation:** Data exploration and statistical analysis of the Fashion-MNIST dataset.
2. **Phase 2: Implementation:** Setting up a high-quality Baseline CNN model.
3. **Phase 3: Experimental Evaluation:** Comparing the Baseline model with a deeper ResNet-18 architecture.
4. **Phase 4: Deep Visualization:** Analyzing internal activation maps to understand feature extraction.

## Model Architectures & Results

We implemented and compared two models using PyTorch:

| Metric | Model 1 (Baseline CNN) | Model 2 (ResNet-18) |
| :--- | :--- | :--- |
| **Architecture** | Simple 2-Layer CNN | Deep Residual Network |
| **Final Accuracy** | **~91.39%** | **~89.10%** |
| **Optimization** | Adadelta | Adam |
| **Loss Function** | NLL Loss | Cross Entropy Loss |

**Analysis:** The Baseline model achieved higher accuracy due to the low resolution ($28 \times 28$) of the dataset, allowing for faster convergence. ResNet-18 showed a more stable learning curve but requires more epochs to fully utilize its depth.

## Deep Visualization (Phase 4)
Following the research by **Yosinski et al.**, we visualized the activation maps of the first convolutional layer.
* **Observation:** The filters successfully identified low-level features such as edges, silhouettes, and sole patterns of the 'Sneaker' input.
* **Conclusion:** This confirms the model learns structural features rather than random noise.

## Repository Structure
* `/notebooks`: Contains `Baseline_Model.ipynb` and `ResNet18_Model.ipynb`.
* `Final_Project_Report.pdf`: Comprehensive report covering all project phases.
* `dataset_preview.png`: Sample images from each class.
* `dataset_statistics.png`: Class distribution bar chart.
* `cnn_activation_maps.png`: Visualization of convolutional layer activations.

## Requirements
* Python 3.x
* PyTorch & Torchvision
* Matplotlib
* NumPy

## References
1. Yosinski, J., et al. (2015). "Understanding neural networks through deep visualization."
2. He, K., et al. (2016). "Deep residual learning for image recognition."
3. Fashion-MNIST Dataset: https://github.com/zalandoresearch/fashion-mnist
