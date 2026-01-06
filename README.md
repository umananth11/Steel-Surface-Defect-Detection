# Steel-Surface-Defect-Detection
## 📌 Overview
Built an computer vision pipeline to detect, classify, and localize surface defects on steel sheets using deep learning.  
Compared segmentation, classification, and object detection approaches to balance accuracy and deployment speed.

## 🎯 Business Objective
- Automate manual steel surface inspection  
- Improve defect detection accuracy and consistency  
- Reduce inspection time and human dependency  
- Enable scalable, AI-driven quality control  

## 📂 Dataset
- High-resolution grayscale images (256 × 1600)  
- 4 defect classes with pixel-level RLE annotations  
- Challenges: class imbalance, small defects, multiple defects per image
- 
## 🧠 Modeling Approaches

### 🔹 U-Net Segmentation
- Pixel-level defect localization  
- Loss: Dice + Binary Cross Entropy  
- Metric: Dice Coefficient  
- **Best for precise defect boundaries**
- 
### 🔹 YOLOv8 Object classification & object Detection 
- Converted masks → bounding boxes  
- Metrics: mAP@50, Recall, Precision  
- **Production-friendly and real-time**

## ⚖️ Handling Class Imbalance
- Dice-based loss functions  
- Class-aware augmentation  
- Recall-focused evaluation  
- Pixel-level error analysis (FP / FN)

## 📊 Key Results
| Model | Key Strength |
|------|-------------|
| U-Net | Best localization accuracy |
| YOLOv8 | Real-time defect detection |

**Insight:** Segmentation offers precision, YOLO offers speed — detection is preferred for deployment.
## 🧪 Evaluation & Error Analysis
- Dice, Recall, Precision, mAP used appropriately  
- Focused on minimizing False Negatives  
- Visual inspection of predictions for validation  
## 🛠️ Tech Stack
Python · PyTorch · OpenCV · Albumentations ·  
segmentation-models-pytorch · Ultralytics YOLOv8 · NumPy · Pandas
