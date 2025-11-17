# Early Detection of Ovarian Cancer Using GAN-Based Data Augmentation and Transformer Models

This repository contains the complete implementation of a deep learning framework designed for early cancer detection using biomarker data. The pipeline integrates synthetic data augmentation using tabular GANs, logistic regression–based feature selection, and transformer-driven classification (SAINT) for improved diagnostic accuracy in ovarian cancer.  
The project also evaluates the model’s generalizability on breast and lung cancer biomarker datasets.

**Key components:**
- **GAN Notebooks:** CTGAN, TVAE, CopulaGAN, Gaussian methods, KDE, SMOTE  
- **Feature Extraction:** OVCD_TEXT_FEATURES  
- **Augmented Data:** OVC_TEXT_AUGMENTED_DATA  
- **Cross-Cancer Validation:** GAN models applied to breast & lung cancer biomarker datasets 
## Methodology

### 1. Data Preprocessing
- Standardization and normalization  
- Handling missing or inconsistent biomarker entries  
- Stratified train-test split  

### 2. Synthetic Data Augmentation
Four tabular GAN models were used:
- CTGAN  
- TVAE  
- CopulaGAN  
- Gaussian CopulaGAN  

These models help mitigate dataset imbalance and increase data diversity.

### 3. Feature Selection
- Logistic Regression used for feature importance ranking  
- Reduction of unnecessary biomarkers  
- Improved interpretability and classifier performance  

### 4. Classification using SAINT
SAINT (Self-Attention and Intersample Attention Transformer):
- Optimized for tabular data  
- Captures feature-level and inter-sample relationships  
- Achieved 95% accuracy for ovarian cancer  

### 5. Generalizability Testing
The same pipeline was tested on:
- Breast cancer dataset (94% accuracy)  
- Lung cancer dataset (95% accuracy)  

---

## Results

| Cancer Type | Accuracy |
|-------------|----------|
| Ovarian     | 95%      |
| Breast      | 94%      |
| Lung        | 95%      |

---

## Technologies and Libraries
- Python 3.x  
- PyTorch  
- SDV (Synthetic Data Vault)  
- Scikit-learn  
- Pandas  
- NumPy  
- Matplotlib / Seaborn  

---

## Installation

```bash
git clone https://github.com/VidyaGanes/vidya-ganesan-phd.git
cd ovarian-cancer-detection

pip install -r requirements.txt
```

