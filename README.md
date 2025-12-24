# Fashion-MNIST Classification and Deep Visualization Analysis

This repository contains the final project for the **SEN4107 Introduction to Neural Networks** course. The project focuses on image classification using the Fashion-MNIST dataset, comparing a custom Baseline CNN with a modified ResNet-18 architecture, and analyzing internal model representations through activation maps.

## Project Overview

The project is structured into four main phases:
1. [cite_start]**Phase 1: Preparations:** Data exploration, statistical analysis, and visualization of the Fashion-MNIST dataset. [cite: 21]
2. [cite_start]**Phase 2: Architecture Definition:** Implementation of a 2-layer Baseline CNN and a 1-channel adapted ResNet-18. [cite: 43, 52]
3. [cite_start]**Phase 3: Training & Comparison:** Rigorous training for 5 epochs under fixed hyperparameters to evaluate accuracy vs. complexity. [cite: 65, 72]
4. [cite_start]**Phase 4: Deep Visualization:** Interpretation of internal feature representations using activation maps. [cite: 78, 84]

## Model Architectures & Experimental Results

[cite_start]Both models were implemented using **PyTorch** and trained for 5 epochs with a batch size of 64. [cite: 61, 65, 130]

| Feature | Model 1 (Baseline CNN) | Model 2 (ResNet-18) |
| :--- | :--- | :--- |
| **Architecture** | [cite_start]2-Layer CNN + Dropout [cite: 45] | [cite_start]Modified Deep Residual Network [cite: 53] |
| **Optimizer** | [cite_start]Adadelta (LR: 1.0) [cite: 61] | [cite_start]Adam (LR: 0.0001) [cite: 59] |
| **Loss Function** | [cite_start]Cross-Entropy Loss [cite: 61] | [cite_start]Cross-Entropy Loss [cite: 58] |
| **Final Test Accuracy** | [cite_start]**91.34%** [cite: 68, 75] | [cite_start]**89.47%** [cite: 70, 76] |
| **Training Loss (Final)** | [cite_start]**0.2318** [cite: 75, 103] | [cite_start]**0.1571** [cite: 76, 103] |



### Key Findings:
* [cite_start]**Accuracy vs. Complexity:** The Baseline model achieved a superior test accuracy of **91.34%**. [cite: 68, 98] [cite_start]Its simpler architecture is highly effective for low-resolution (28x28) grayscale images. [cite: 100, 108]
* [cite_start]**Learning Capacity:** ResNet-18 achieved a significantly lower training loss (**0.1571**) compared to the Baseline (**0.2318**). [cite: 76, 103] [cite_start]This indicates superior learning capacity, though the 5-epoch limit was insufficient to fully optimize its 11 million parameters for maximum test accuracy. [cite: 104, 105, 116]

## Deep Visualization (Phase 4)
Following the methodologies of **Yosinski et al. (2015)[cite_start]**, we visualized the first convolutional layer to interpret feature extraction. [cite: 35, 78]



* [cite_start]**Edge Detection:** Early filters successfully captured low-level features such as high-contrast edges and structural silhouettes of items like 'Sneakers'. [cite: 85, 86, 89]
* [cite_start]**Hierarchical Learning:** The analysis confirms that the network learns to build complex conceptual representations from these basic geometric outlines. [cite: 90, 119]

## Repository Structure
* [cite_start]`Baseline_Model.ipynb`: Implementation and training of the Baseline CNN. [cite: 43]
* [cite_start]`ResNet18_Model.ipynb`: Modified ResNet-18 implementation for grayscale input. [cite: 52, 56]
* [cite_start]`PROJECT_REPORT.pdf`: Comprehensive final report detailing the experimental rigor and results. [cite: 1, 63]
* [cite_start]`visualizations/`: Exported activation maps and training curves. [cite: 83, 106]

## Requirements
* [cite_start]Python 3.x [cite: 130]
* [cite_start]PyTorch & Torchvision [cite: 130]
* [cite_start]Matplotlib [cite: 131]
* [cite_start]NumPy [cite: 131]

## References
1. Xiao, H., et al. (2017). [cite_start]"Fashion-MNIST: A Novel Image Dataset." [cite: 121]
2. Yosinski, J., et al. (2015). [cite_start]"Understanding neural networks through deep visualization." [cite: 123]
3. He, K., et al. (2016). [cite_start]"Deep residual learning for image recognition." [cite: 125]
