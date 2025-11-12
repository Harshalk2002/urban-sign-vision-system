# 🛣️ Urban Sign Vision System
A computer vision project that detects and classifies urban traffic signs using classical ML and deep learning pipelines.

## 📘 Overview
This project was developed as part of the **MSA 8395 — Computer Vision** course at Georgia State University.  
The system analyzes real-world street imagery from the **Mapillary Traffic Sign Dataset**, building a complete end-to-end pipeline from data preparation to model evaluation.

## 🧩 Project Structure
```
urban-sign-vision-system/
│
├── notebooks/
│   ├── 01_data_preparation.ipynb         
│   ├── 02_preprocessing_region_proposal.ipynb 
│   ├── 03_classical_ml.ipynb             
│   ├── 04_deep_learning.ipynb            
│   └── 05_analysis.ipynb                 
│
├── results/
│   ├── figures/                          
│   ├── metrics/                          
│   └── subset/                           
│
├── models/
│   ├── rf_model.pkl                      
│   └── svm_model.pkl                     
│
└── README.md
```

## ⚙️ Workflow
### **Phase 1: Data Preparation**
- Extracted a balanced subset of 5 major sign categories  
- Created bounding box CSVs (`annotations_master.csv`, `subset_split.csv`)  
- Split into **train/val/test**

### **Phase 2: Region Proposal**
- Implemented IoU-based region proposal evaluation  
- Generated precision-recall metrics at IoU thresholds (0.3, 0.5, 0.7)  
- Visualized GT vs proposal bounding boxes  

### **Phase 3: Classical ML**
- Feature extraction: HOG + PCA  
- Models: SVM and Random Forest  
- Achieved ~90% test accuracy  

### **Phase 4: Deep Learning**
- Built CNN classifier with PyTorch  
- Visualized misclassified samples  
- Compared CNN vs ML baselines  

### **Phase 5: Final Analysis**
- Aggregated metrics across models  
- Created summary plots and CSV tables  
- Final model comparison figure saved as `phase5_model_comparison.png`

## 📊 Results Summary
| Model | Test Accuracy | CV Mean | CV Std |
|-------|----------------|---------|--------|
| SVM | 0.899 | 0.906 | 0.024 |
| Random Forest | 0.899 | 0.874 | 0.015 |
| CNN | 0.300 | 0.500 | 0.000 |

> **Insight:** Classical models performed better due to limited data and heavy image variance in the dataset subset.

## 🧠 Key Learnings
- Importance of region proposal tuning for detection accuracy  
- Trade-offs between HOG-based vs CNN-based recognition pipelines  
- Practical understanding of model evaluation metrics (IoU, precision, recall)  

## 🛠️ Environment Setup
```bash
git clone git@github.com:Harshalk2002/urban-sign-vision-system.git
cd urban-sign-vision-system
python -m venv .venv
source .venv/bin/activate  # (Linux/Mac)
pip install -r requirements.txt
```

## 📁 Key Outputs
- **Metrics:** Stored in `/results/metrics`
- **Visuals:** All plots under `/results/figures`
- **Models:** Serialized pickle files under `/notebooks/models`

## 👨‍💻 Authors
**Harshal Prashant Kamble**  
📧 harshalkamble2511@gmail.com  
🎓 Georgia State University, J. Mack Robinson College of Business  
