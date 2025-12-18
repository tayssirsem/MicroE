# Micro-Expressions Recognition: CNN vs RNN
---

## Project Overview
This project focuses on **automatic recognition of facial micro-expressions** using deep learning. Facial micro-expressions are subtle, involuntary expressions that reveal genuine emotions. The study compares two deep learning architectures:

- **Convolutional Neural Network (CNN)** – specialized in capturing spatial patterns in images.
- **Recurrent Neural Network (RNN)** – processes images as sequences of pixel rows to capture sequential dependencies.

The models classify facial images into **six emotion classes**: Anger, Disgust, Fear, Sadness, Surprise, and Happiness.

---

## Dataset
- **Source:** [Kaggle Micro-Expressions Dataset](https://www.kaggle.com/datasets)  
- **Classes:**  6
- **Number of images:** varies per class  
- **Preprocessing steps:**
  - Resize all images to 224×224 pixels
  - Normalize pixel values to range [0, 1]
  - Data augmentation: horizontal flip, random rotation, zoom, and contrast
  - Dataset split: 80% training / 20% validation

---

## Evaluation Metrics
- **Accuracy** – overall classification accuracy  
- **Precision** – how accurate positive predictions are  
- **Recall** – model’s ability to find all positive samples  
- **F1-score** – harmonic mean of precision and recall  
- **Confusion matrix** – detailed performance per class  
- **Training & Validation curves** – monitor overfitting  

---

## Results Summary

| Model |  Accuracy  | Precision |  Recall   | F1-score |
|-------|------------|-----------|-----------|----------|
| CNN   | 0.963333   | 0.964323  |0.963333   | 0.963154 |
| RNN   | 0.811942   | 0.825955  | 0.811942  | 0.814567 |

- CNN consistently outperforms RNN on all metrics.  
- CNN better captures spatial features; RNN loses spatial relationships when processing images as sequences.  
- Data augmentation and convolutional feature extraction help CNN generalize and reduce overfitting.  

