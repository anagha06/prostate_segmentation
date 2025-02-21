# Prostate_Segmentation  

**Prostate cancer segmentation and explainability decision support system using EfficientNet.**  

## Overview  

Prostate cancer diagnosis often involves borderline classification decisions, where subtle differences in Gleason scores can significantly impact treatment. **GleasonNet** is a **four-pipeline decision support system** that enhances **prostate cancer segmentation and explainability**. Using **EfficientNet** for segmentation and an expert-driven decision support system, this approach provides clinicians with **confidence metrics and predictive insights**, addressing key gaps in automated diagnosis.  

## Features  

- **EfficientNet-Based Semantic Segmentation**: Classifies **six distinct pixel types** for precise tumor detection.  
- **Expert-Driven Decision Support**: Uses a **novel algorithm** to enhance clinical decision-making.  
- **High-Accuracy Quantification**: Converts segmentation results into actionable **ISUP/Gleason scores**.  
- **Google Cloud TPU Optimization**: Enables efficient processing of large pathology datasets.  
- **Explainability & Confidence Metrics**: Helps oncologists assess percentage involvement of tumor regions.  

## Methodology  

### **1. Dataset & Preprocessing**  
- Utilizes **pathologic data** from **Radboud & Karolinska Institutes**.  
- Downscales images for accessibility.  
- Filters dataset to **Radboud cases** for segmentation.  

### **2. Semantic Segmentation Pipeline**  
- **Trained EfficientNet** to segment six different prostate cancer tissue types.  
- Achieved **85% Jaccard Distance (IoU)** for target/predicted masks.  

### **3. Prediction Pipeline**  
- Uses segmentation masks to **quantify tumor characteristics**.  
- Trained on Google Cloud TPU for **efficient processing**.  
- Achieved **79% validation accuracy & recall** for ISUP classification.  

### **4. Decision Support System**  
- Developed with **a GU oncologist** to provide explainable metrics.  
- Computes **“percentage involvement”** for enhanced diagnostic confidence.  
- Helps distinguish **borderline cases** (e.g., Gleason **3+4 vs. 4+3**).  

## Results  

- **Semantic Segmentation Performance**: 85% **Jaccard Distance (IoU)**.  
- **Prediction Pipeline Accuracy**: 79% **validation accuracy & recall**.  
- **Explainability & Confidence Metrics**: Enables oncologists to **assess risk & treatment pathways**.  

## Installation  

### **Requirements**  
- Python 3.x  
- TensorFlow  
- EfficientNet  
- Google Cloud TPU (for training)  

### **Setup**  
```bash
git clone https://github.com/yourusername/prostate_segmentation.git
cd prostate_segmentation
pip install -r requirements.txt
