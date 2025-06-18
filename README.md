# 🌦️ Weather Image Classification using Transfer Learning

This project builds an image classification model to predict weather conditions from images using transfer learning with MobileNet. The classifier predicts four categories:

- Shine
- Cloudy
- Sunrise
- Rain

## 📂 Project Overview

- **Model:** MobileNet (pre-trained on ImageNet)  
- **Dataset:** Multi-class Weather Dataset (provided via CSV files)  
- **Task:** Multi-class image classification (4 classes)  
- **Approach:** Transfer Learning with frozen MobileNet layers and a custom classifier head  

## 🛠️ Workflow

**Data Preparation:**  
- Read image paths and labels from `training.csv`, `validation.csv`, and `test.csv`.  
- Preprocess images (resize to 230x230, normalize).  

**Model Building:**  
- Load MobileNet without top layers.  
- Freeze pre-trained layers.  
- Add a Dense layer with softmax activation for classification.  

**Training:**  
- Optimizer: Adam with exponential decay learning rate.  
- Loss: Sparse categorical crossentropy.  
- Trained for 5 epochs.  

**Evaluation:**  
- Calculate overall test accuracy.  
- Measure per-class accuracy.  
- Visualize per-class performance using bar charts.  

## ✅ Results

- **Test Accuracy:** 95.11%  

- **Per-Class Accuracy:**  
  - Shine: 89.29%  
  - Cloudy: 94.55%  
  - Sunrise: 97.22%  
  - Rain: 100%  

## 📊 Visualizations

- Bar chart of per-class accuracy to analyze model performance across categories.  
- Class distribution bar chart to visualize dataset balance.  

## 💻 Requirements

```bash
pip install tensorflow numpy matplotlib
