# 🛡️ DDoS Detection using Machine Learning

> A machine learning project focused on processing large-scale network data and building optimized models for DDoS attack detection and classification.

---

## 🚀 Project Overview

This project focuses on:

- Handling **large-scale network dataset (32GB+)**
- Building a **memory-efficient data processing pipeline**
- Training and improving machine learning models through **multiple iterations**
- Performing both:
  - Binary classification (Attack vs Benign)
  - Multiclass classification (12 attack types)

---

## 🎯 Key Results

- 🔥 **99.92% Accuracy** — Binary Classification
- 🧠 **~80.9% Accuracy** — Multiclass Classification
- ⚡ Reduced training and tuning time using optimized dataset pipeline
- 💾 Successfully processed **32GB+ data on limited hardware**

---

## 📂 Dataset
⚠️ Note: Due to dataset size (32GB+), only processing pipeline and models are included.
- **Dataset:** CIC-DDoS2019
- Contains multiple types of DDoS attacks such as:
  - DNS, LDAP, MSSQL, NetBIOS
  - NTP, SNMP, SSDP, TFTP
  - SYN Flood, UDP, WebDDoS, etc.

---

## 🧠 Approach

### 🔹 Iterative Model Development

Instead of training a single model, the project follows an **iterative approach**:

- **Model 0** → Initial baseline model (large dataset, slower)
- **Model 1** → Optimized version (reduced dataset, faster training)
- Future scope → Model 2 and further improvements

This approach helps balance:
- Performance
- Training time
- Resource usage

---

## ⚙️ Workflow

### 1. Data Extraction
- Processed raw dataset using **chunk-based reading (~150K rows)**
- Applied sampling across chunks to capture full attack patterns
- Prevented memory overflow

---

### 2. Data Preprocessing
- Cleaned dataset (missing values, normalization)
- Removed:
  - IP addresses
  - Ports
  - Timestamps  
- Focused on behavioral features to avoid overfitting

---

### 3. Model Training

#### 🔹 Multiclass Model
- Classifies 12 attack types
- Accuracy: ~80.9%

#### 🔹 Binary Model
- Classifies Attack vs Benign
- Accuracy: 99.92%

---

### 4. Hyperparameter Tuning
- Used **RandomizedSearchCV**
- Used **BayesSearchCV**
- Improved model performance
- Reduced tuning time significantly

---

## 📂 Project Structure

```
project_code/
│
├── dataset/                     # processed datasets
├── CSV-01-12                    # raw dataset folder
├── CSV-03-11                    # raw dataset folder
|
├── model_0_code/               # Initial baseline model (large dataset)
│   ├── A_TestDataSelection.ipynb
│   ├── A_TrainDataSelection.ipynb
│   ├── B_CleanDataSet.ipynb
│   ├── C_EDA.ipynb
│   ├── D_Model_Train.ipynb
│
├── model_1_code/               # Optimized model (current version)
│   ├── A_DataExtraction.ipynb
│   ├── B_CleanDataSet.ipynb
│   ├── C_Model_Train.ipynb
│   ├── D_hyperParametr.ipynb
│   ├── E_Binary_model.ipynb
│
├── models/                     # Saved trained models (.pkl)
├── results/                    # Output results and visualizations
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the Repository
```bash

git clone https://github.com/RajSurajR/Ddos_attack_detection_ml.git
cd Ddos_attack_detection_ml
```

---

### 2. Download Dataset

The dataset is not included in this repository due to large size (32GB+).

- Download: CIC-DDoS2019 dataset (from official source)
- Extract zip folder into the `/Ddos_attack_detection_ml/` folder 

Expected structure:
```
Ddos_attack_detection_ml/
    ├── CSV-01-12/
    └── CSV-03-11/
```

---

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

---

### 4. Run Pipeline

Navigate to:

```
model_1_code/
```

Run notebooks in order:

1. `A_DataExtraction.ipynb`
2. `B_CleanDataSet.ipynb`
3. `C_Model_Train.ipynb`
4. `D_hyperParametr.ipynb`
5. `E_Binary_model.ipynb`

---

## 📌 Skills Demonstrated

- Large-scale data processing (32GB+)
- Data preprocessing & feature engineering
- Machine learning model building
- Hyperparameter tuning
- Iterative model improvement

---

## ⚠️ Limitations

- Offline model training (no deployment)
- Multiclass accuracy affected by similar attack patterns

---

## 🔮 Future Work

- Further optimize dataset size vs accuracy
- Improve multiclass performance
- Extend to additional model versions

---

## 👤 Author

Suraj Rajak
GitHub: https://github.com/RajSurajR
LinkedIn: https://linkedin.com/in/surajrajak