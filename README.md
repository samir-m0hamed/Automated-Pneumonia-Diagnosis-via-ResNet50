# Pneumonia Detection via ResNet50 (Transfer Learning & Fine-Tuning)

Deep learning system for automated pneumonia classification from chest X-ray images using a pretrained ResNet50 architecture.  
The pipeline follows a two-stage training strategy: feature extraction and full network fine-tuning to maximize diagnostic performance.

---

## 📌 Project Overview

This project implements a complete medical image classification workflow:

1. Data preprocessing and normalization  
2. Transfer learning using pretrained ResNet50  
3. Feature extraction phase (frozen backbone)  
4. Fine-tuning phase (partial unfreezing)  
5. Performance monitoring across training stages  
6. ROC analysis and threshold evaluation  
7. Clinical-style evaluation using confusion matrix metrics  

---

## 🧠 Model Architecture

| Component | Description |
|---|---|
| Backbone | ResNet50 pretrained on ImageNet |
| Strategy | Transfer Learning + Fine-Tuning |
| Input Type | Chest X-Ray Images |
| Task | Binary Classification (Normal vs Pneumonia) |
| Evaluation | Accuracy, Precision, Recall, F1, ROC-AUC |

---

## 📊 Training Performance

### Phase 1 — Feature Extraction
![Feature Extraction Results](Pneumonia%20Detection%20via%20ResNet/Feature%20Extraction%20Results.png)

| Metric | Observation |
|---|---|
| Training Loss | Decreased steadily |
| Validation Loss | Slight fluctuations |
| Training Accuracy | Continuous improvement |
| Validation Accuracy | Stable around ~0.90 |
| Training AUC | Approached ~0.994 |
| Validation AUC | ~0.975–0.982 |

---

### Phase 2 — Fine-Tuning
![Fine Tuning Results](Pneumonia%20Detection%20via%20ResNet/fine%20tuning%20results.png)

| Metric | Observation |
|---|---|
| Training Loss | Further reduction |
| Validation Loss | Moderate fluctuation |
| Training Accuracy | Reached ~0.97 |
| Validation Accuracy | ~0.91–0.92 |
| Training AUC | ~0.996 |
| Validation AUC | ~0.981–0.987 |

---

## 📉 ROC Curve

![ROC Curve](Pneumonia%20Detection%20via%20ResNet/ROC%20Curve.png)

| Metric | Value |
|---|---|
| ROC-AUC | **0.995** |
| Interpretation | Excellent class separability |

---

## 🔬 Confusion Matrix

![Confusion Matrix](Pneumonia%20Detection%20via%20ResNet/confusion%20matrix.png)

| Actual \ Predicted | Normal | Pneumonia |
|---|---|---|
| Normal | 80 | 1 |
| Pneumonia | 20 | 206 |

---

## 📈 Final Evaluation Metrics

| Metric | Value |
|---|---|
| Accuracy | 93.16% |
| Precision (Pneumonia) | 99.52% |
| Recall / Sensitivity | 91.15% |
| Specificity | 98.77% |
| F1 Score | 95.20% |
| ROC-AUC | 0.995 |

---

## 🏥 Clinical Interpretation

- Very high precision → minimal false pneumonia alarms  
- Strong sensitivity → effective disease detection  
- Excellent specificity → reliable normal classification  
- Near-perfect ROC-AUC → robust probability separation  

Model demonstrates strong potential for AI-assisted radiological screening.

---

## ⚙️ Technologies Used

| Category | Tools |
|---|---|
| Deep Learning | TensorFlow / Keras |
| Model | ResNet50 |
| Evaluation | Scikit-learn |
| Visualization | Matplotlib / Seaborn |
| Environment | Jupyter Notebook |

---

## 🚀 How to Run

```bash
git clone <repo-url>
cd pneumonia-resnet50
pip install -r requirements.txt
jupyter notebook Pneumonia_Detection_via_ResNet50.ipynb
```

---

## 📁 Repository Structure

```
pneumonia-resnet50/
│
├── Pneumonia_Detection_via_ResNet50.ipynb
│
├── Pneumonia Detection via ResNet/
│   ├── confusion matrix.png
│   ├── Feature Extraction Results.png
│   ├── fine tuning results.png
│   └── ROC Curve.png
│
└── README.md
```

---

## 📜 License

This project is for research and educational purposes

---

## 👩‍💻 Author

**Samir Mohamed : AI & Computer Vision Engineer**
