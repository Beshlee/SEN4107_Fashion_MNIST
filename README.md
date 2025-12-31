# Fashion-MNIST Classification and Deep Visualization Analysis

This repository contains the final project for the **SEN4107 Introduction to Neural Networks** course. [cite_start]The project focuses on image classification using the Fashion-MNIST dataset, comparing a custom Baseline CNN with a modified ResNet-18 architecture, and analyzing internal model representations through activation maps. [cite: 1, 2, 74]

## Project Overview

The project is structured into four main phases:
1. [cite_start]**Phase 1: Preparations:** Data exploration, statistical analysis, and visualization of the Fashion-MNIST dataset. [cite: 15, 80, 94]
2. [cite_start]**Phase 2: Architecture Definition:** Implementation of a 2-layer Baseline CNN and a 1-channel adapted ResNet-18. [cite: 119, 128]
3. [cite_start]**Phase 3: Training & Comparison:** Rigorous training for 5 epochs under fixed hyperparameters to evaluate accuracy vs. complexity. [cite: 25, 141]
4. [cite_start]**Phase 4: Deep Visualization:** Interpretation of internal feature representations using activation maps. [cite: 153, 160]

## Model Architectures & Experimental Results

[cite_start]Both models were implemented using **PyTorch** and trained for 5 epochs with a batch size of 64. [cite: 137, 201]



| Feature | Model 1 (Baseline CNN) | Model 2 (ResNet-18) |
| :--- | :--- | :--- |
| **Architecture** | [cite_start]2-Layer CNN + Dropout [cite: 122, 125] | [cite_start]Modified Deep Residual Network [cite: 129] |
| **Optimizer** | [cite_start]Adadelta (LR: 1.0) [cite: 137] | [cite_start]Adam (LR: 0.0001) [cite: 135] |
| **Loss Function** | [cite_start]Cross-Entropy Loss [cite: 137] | [cite_start]Cross-Entropy Loss [cite: 134] |
| **Final Test Accuracy** | [cite_start]**91.34%** [cite: 144, 151] | [cite_start]**89.47%** [cite: 146, 152] |
| **Training Loss (Final)** | [cite_start]**0.2318** [cite: 151] | [cite_start]**0.1571** [cite: 152, 179] |

### Key Findings:
* [cite_start]**Accuracy vs. Complexity:** The Baseline model achieved a superior test accuracy of **91.34%**. [cite: 144, 174] [cite_start]Its simpler architecture is highly effective for low-resolution (28x28) grayscale images. [cite: 120, 184]
* [cite_start]**Learning Capacity:** ResNet-18 achieved a significantly lower training loss (**0.1571**) compared to the Baseline (**0.2318**). [cite: 179] [cite_start]This indicates superior learning capacity, though the 5-epoch limit was insufficient to fully optimize its parameters for maximum test accuracy on this specific dataset. [cite: 181, 192]

## Deep Visualization (Phase 4)
[cite_start]Following established methodologies for interpreting neural networks, we visualized the first convolutional layer to understand how the models perceive fashion items. [cite: 111, 153, 155]



* [cite_start]**Edge Detection:** Early filters successfully captured low-level features such as high-contrast edges and structural silhouettes of items like 'Sneakers'. [cite: 162, 167]
* [cite_start]**Hierarchical Learning:** The analysis confirms that the network learns to build complex conceptual representations from these basic geometric outlines. [cite: 165, 166, 195]

## Repository Structure
* `Baseline_Model.ipynb`: Implementation and training of the Baseline CNN.
* [cite_start]`ResNet18_Model.ipynb`: Modified ResNet-18 implementation for grayscale input. [cite: 131, 132]
* [cite_start]`PROJECT_REPORT.pdf`: Comprehensive final report detailing the experimental rigor and results. [cite: 37, 59]
* [cite_start]`visualizations/`: Exported activation maps and training curves. [cite: 159, 182]

## Requirements
* Python 3.x
* [cite_start]PyTorch & Torchvision [cite: 201]
* Matplotlib
* NumPy
