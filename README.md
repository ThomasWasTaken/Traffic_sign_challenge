# Traffic Sign Recognition Challenge

This repository contains a high-performance deep learning solution for the **German Traffic Sign Recognition Benchmark (GTSRB)**. The goal of this project is to develop a single, elegant neural network that achieves state-of-the-art accuracy without the use of ensembles or transfer learning.

## 🏆 Project Objectives
The primary goal is to exceed an accuracy threshold of **99.47%** on the GTSRB test set under strict constraints:
* **Framework**: Built entirely using **PyTorch**.
* **Architecture**: A single network (no ensembles).
* **Training**: Trained from scratch using only the provided GTSRB training data.
* **Reproducibility**: Optimized for execution in a free Google Colab environment.

## 🛠️ Key Features
* **Custom Mini-ResNet**: An optimized architecture designed specifically for traffic sign classification.
* **Advanced Scheduling**: Implements a `SequentialLR` strategy combining `LinearLR` (warmup) and `CosineAnnealingLR` for optimal convergence.
* **Robust Data Splitting**: Uses a specific index-based split saved to `gtsrb_split.json` to ensure identical training/validation sets across runs.
* **Automated Pipeline**: Includes automated data extraction, preprocessing, and checkpointing.

## 📁 Repository Structure
* `Traffic_signs_submission_final.ipynb`: The main Jupyter notebook containing the full pipeline from data loading to evaluation.
* `gtsrb_split.json`: Metadata file storing the training and validation indices for reproducibility.
* `mini_resnet_checkpoint.pth`: The saved weights of the best-performing model.

## 🚀 Getting Started

### Prerequisites
* A Google account to access Google Colab.
* The `GTSRB.zip` dataset file (standard benchmark format).

### Installation & Usage
1.  **Upload the Notebook**: Open the `.ipynb` file in Google Colab.
2.  **Upload Dataset**: Ensure `GTSRB.zip` is available in your Google Drive root or local Colab storage.
3.  **Run All Cells**: The notebook will:
    * Unzip and organize the data.
    * Initialize the specialized ResNet architecture.
    * Train using the `AdamW` optimizer and the custom learning rate schedule.
    * Save the best model state based on validation accuracy.

## 📊 Results
the model Acheiwed an accuracy of 99.63%, thereby ahceiwing the goal presented in the challenge.
## 📜 License
This project was developed as part of a Machine Learning competition focused on model elegance and performance.
