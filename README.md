# Fashion-MNIST Classification and Deep Visualization Analysis

This repository contains the final project for the **SEN4107 Introduction to Neural Networks** course. The project focuses on image classification using the Fashion-MNIST dataset, comparing a custom Baseline CNN with a modified ResNet-18 architecture, and analyzing internal model representations through activation maps.

## Project Overview

The project is structured into four main phases:
1. **Phase 1: Preparations:** Data exploration, statistical analysis, and visualization of the Fashion-MNIST dataset.
2. **Phase 2: Architecture Definition:** Implementation of a 2-layer Baseline CNN and a 1-channel adapted ResNet-18.
3. **Phase 3: Training & Comparison:** Rigorous training for 5 epochs under fixed hyperparameters to evaluate accuracy vs. complexity.
4. **Phase 4: Deep Visualization:** Interpretation of internal feature representations using activation maps.

## Model Architectures & Experimental Results

Both models were implemented using **PyTorch** and trained for 5 epochs with a batch size of 64.

| Feature | Model 1 (Baseline CNN) | Model 2 (ResNet-18) |
| :--- | :--- | :--- |
| **Architecture** | 2-Layer CNN + Dropout | Modified Deep Residual Network |
| **Optimizer** | Adadelta (LR: 1.0) | Adam (LR: 0.0001) |
| **Loss Function** | Cross-Entropy Loss | Cross-Entropy Loss |
| **Final Test Accuracy** | **91.34%** | **89.47%** |
| **Training Loss (Final)** | **0.2318** | **0.1571** |



### Key Findings:
* **Accuracy vs. Complexity:** The Baseline model achieved a superior test accuracy of **91.34%**. Its simpler architecture is highly effective for low-resolution (28x28) grayscale images.
* **Learning Capacity:** ResNet-18 achieved a significantly lower training loss (**0.1571**) compared to the Baseline (**0.2318**). This indicates superior learning capacity, though the 5-epoch limit was insufficient to fully optimize its parameters for maximum test accuracy on this specific dataset.

## Deep Visualization (Phase 4)
Following established methodologies for interpreting neural networks, we visualized the first convolutional layer to understand how the models perceive fashion items.



* **Edge Detection:** Early filters successfully captured low-level features such as high-contrast edges and structural silhouettes of items like 'Sneakers'.
* **Hierarchical Learning:** The analysis confirms that the network learns to build complex conceptual representations from these basic geometric outlines.


## Requirements
* Python 3.x
* PyTorch & Torchvision
* Matplotlib
* NumPy
