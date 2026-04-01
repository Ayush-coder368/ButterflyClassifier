# 🦋 Enchanted Wings: Butterfly Species Classification

A deep learning project that classifies butterfly species using transfer learning and computer vision.

---

## 📌 Overview

Butterflies are important indicators of ecosystem health and biodiversity. Manual identification is time-consuming and requires expertise.  

This project builds an automated butterfly species classification system using **transfer learning**, enabling fast and accurate identification.

---

## 🎯 Objectives

- Build an accurate butterfly classification model  
- Use transfer learning to improve efficiency  
- Support biodiversity monitoring and ecological research  
- Enable citizen science participation  

---

## 📂 Dataset

- **Source:** Kaggle Butterfly Image Dataset  
- **Total Images:** 6,499  
- **Classes:** 75 butterfly species  
- **Split:**
  - Training Set  
  - Validation Set  
  - Test Set  

The dataset includes variations in lighting, orientation, and backgrounds for robust training.

---

## ⚙️ Methodology

### 🔹 Data Preprocessing

- Resize images to **160x160**
- Normalize pixel values (`rescale = 1./255`)
- Data augmentation:
  - Rotation (±25°)
  - Zoom (20%)
  - Horizontal flip
  - Brightness adjustment

---

### 🔹 Transfer Learning

- Model: **MobileNetV2 (pre-trained on ImageNet)**
- `include_top=False`
- Frozen base layers for feature extraction

---

### 🔹 Model Architecture
MobileNetV2 (Base Model)
→ GlobalAveragePooling2D
→ BatchNormalization
→ Dense (128, ReLU)
→ Dropout (0.5)
→ Dense (Softmax Output)


---

### 🔹 Training Strategy

#### Phase 1: Initial Training
- Frozen base model  
- Optimizer: Adam  
- Epochs: 15  

#### Phase 2: Fine-Tuning
- Unfreeze last 30 layers  
- Learning rate: 1e-5  
- Epochs: 10  

---

### 🔹 Evaluation

- Accuracy  
- Confusion Matrix  
- Precision, Recall, F1-score  

---

### 🔹 Deployment

- Built using **Gradio**
- Features:
  - Upload butterfly image  
  - Get real-time prediction with confidence score  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Platform:** Google Colab  
- **Libraries:**
  - TensorFlow / Keras  
  - NumPy  
  - Pandas  
  - Matplotlib 
  - Gradio  

---

## 📊 Results

- High classification accuracy using transfer learning  
- Improved generalization after fine-tuning  
- No significant overfitting observed  

### 📈 Training Insights

- Training & validation accuracy increase steadily  
- Fine-tuning improves validation performance  
- Data augmentation stabilizes learning  

---

## 🌍 Applications

### 1. Biodiversity Monitoring
- Helps identify species in natural habitats  

### 2. Ecological Research
- Tracks behavior, migration, and environmental changes  

### 3. Education & Citizen Science
- Enables public participation in species identification  

---

## ✅ Advantages

- High accuracy  
- Reduced training time  
- Scalable to other classification tasks  
- Supports real-time applications  

---

## 🚀 Future Scope

- Mobile app deployment  
- Real-time camera integration  
- Expansion to other species  
- Use of advanced models (e.g., Vision Transformers)  

---

## 📌 Conclusion

This project demonstrates the effectiveness of transfer learning in image classification. It provides a fast, accurate, and scalable solution for butterfly species identification, contributing to conservation and research efforts.

---

## 📚 References

- TensorFlow Documentation  
- Keras Applications  
- ImageNet Dataset  
- Research papers on CNNs & Transfer Learning  
- Kaggle Datasets  

---
