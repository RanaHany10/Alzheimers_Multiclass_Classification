
# Alzheimer's Multi-class Classification

The project leverages deep learning models, specifically transfer learning with pre-trained models, to aid in the early diagnosis of Alzheimer's disease.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training and Evaluation](#training-and-evaluation)
- [Results](#results)

## Project Overview

Alzheimer's disease is a major neurodegenerative disorder that requires early diagnosis for effective management. This project aims to classify Alzheimer's disease stages (Normal, Mild Cognitive Impairment, Very Mild Dementia) using MRI images. By applying transfer learning techniques, the project achieves multi-class classification with a focus on leveraging pre-trained models.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/alzheimers-multiclass-classification.git
   cd alzheimers-multiclass-classification
   ```

2. **Install dependencies:**
   
   Create a `requirements.txt` file with the following contents:
   ```bash
   tensorflow==2.13.0
   keras-tuner==1.3.5
   numpy==1.23.5
   pandas==2.0.3
   scikit-image==0.21.0
   scikit-learn==1.3.0
   matplotlib==3.7.3
   split-folders==0.5.1
   ```
   Then, install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Dataset

The dataset used for this project is the Alzheimer's Disease Neuroimaging Initiative (ADNI) dataset. It contains MRI scans labeled as Normal (ND), Mild Cognitive Impairment (MID), and Very Mild Dementia (VMD). Preprocessing steps include scaling, resizing, and splitting the dataset into training and testing sets.

## Model Architecture

The project explores several models, including:

- **Base Model (Inception):** A pre-trained Inception model fine-tuned for multi-class classification.
- **Model 1:** Inception with additional layers for increased capacity.
- **Model 2:** Inception with optimized parameters and data augmentation.
- **Model 3:** Xception model pre-trained on ImageNet.
- **Model 4:** VGG19 model, which performed the best with an accuracy of 67%.

## Training and Evaluation

The models were trained using the ADNI dataset, with a typical training/testing split of 80/20. Key metrics, including accuracy and AUC, were used to evaluate model performance. The best model, VGG19, achieved a 67% accuracy.

## Results

- **Best Model:** VGG19
- **Accuracy:** 67%
- **Confusion Matrix:** Available in the results directory.