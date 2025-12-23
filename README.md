# Fashion-MNIST Classification and Deep Visualization Analysis

This repository contains the final project for the **SEN4107 Introduction to Neural Networks** course (Fall 2025). The project focuses on image classification using the Fashion-MNIST dataset, comparing a custom Baseline CNN with a modified ResNet-18 architecture, and analyzing internal model representations through activation maps.

## Project Overview

The project is structured into five main phases:
1. **Phase 1: Preparations:** Data exploration, statistical analysis, and visualization of the Fashion-MNIST dataset.
2. **Phase 2: Understanding Implementation:** Selection and documentation of a high-quality baseline repository.
3. **Phase 3: Implement & Compare:** Training a Baseline CNN and a modified ResNet-18 architecture under a rigorous comparison scheme.
4. **Phase 4: Document & Submit:** Comprehensive reporting and GitHub repository management.
5. **Phase 5: Technical Demonstration:** Live presentation and defense of the implementation.

## Model Architectures & Experimental Results

We implemented and compared two distinct models using **PyTorch**. To ensure a fair comparison, both models were trained for 5 epochs with a batch size of 64.

| Feature | Model 1 (Baseline CNN) | Model 2 (ResNet-18) |
| :--- | :--- | :--- |
| **Architecture** | 2-Layer CNN + Dropout | Modified Deep Residual Network |
| **Optimizer** | Adadelta (LR: 1.0) | Adam (LR: 0.0001) |
| **Loss Function** | Cross-Entropy Loss | Cross-Entropy Loss |
| **Final Accuracy** | **89.98%** | **89.18%** |
| **Training Loss** | 0.2459 | 0.1598 |

### Key Findings:
* **Efficiency:** The Baseline model achieved slightly higher test accuracy (**89.98%**) within the 5-epoch limit, proving highly efficient for low-resolution ($28 \times 28$) grayscale images.
* **Complexity vs. Performance:** While ResNet-18 achieved a lower training loss (**0.1598**), its test accuracy (**89.18%**) indicates a slight overfitting or the need for more epochs to refine its millions of parameters for this specific task.

## Deep Visualization (Phase 4)
Following the research by **Yosinski et al. (2015)**, we visualized the activation maps of the first convolutional layer (Conv1) to interpret feature extraction.
* **Feature Detection:** The filters successfully identified low-level features such as high-contrast edges, silhouettes, and mesh-like textures on items like 'Sneakers'.
* **Hierarchical Learning:** The visualization confirms that the model transitions from simple edge detection in early layers to complex conceptual representations in deeper layers.

## Repository Structure
* `/code`: PyTorch implementation scripts for both models and visualization functions.
* `SEN4107_Project_Report.pdf`: Comprehensive final report following the required structure.
* `visualizations/`: Exported activation maps and training/accuracy curves.

## Requirements
* Python 3.x
* PyTorch & Torchvision
* Matplotlib (for visualization)
* NumPy

## References
1. Xiao, H., et al. (2017). "Fashion-MNIST: A Novel Image Dataset."
2. Yosinski, J., et al. (2015). "Understanding neural networks through deep visualization."
3. He, K., et al. (2016). "Deep residual learning for image recognition."
