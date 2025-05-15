# 🩺 Smart Blood Test Interpreter  
**An AI-Powered Multi-Disease Diagnostic System Using Routine Blood Test Results**

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

---

## 🧠 About the Project

The **Smart Blood Test Interpreter** is a machine learning-based web application that assists in early-stage disease detection by analyzing numerical blood test data. With just standard blood test parameters as input, this system predicts multiple diseases **simultaneously** and explains which test values contributed most to the predictions.

This tool is designed to support **medical professionals, patients, and diagnostic labs**, especially in settings with limited access to specialized diagnostics. It can serve as an assistive layer to doctors for preliminary screening and health monitoring.

Developed as part of our B.Tech final-year project at **KIIT Deemed to be University**, it bridges the gap between healthcare and AI.

---

## 🔍 Problem Statement

Blood tests are one of the most common diagnostic procedures. However, interpreting them can be complex, error-prone, and time-consuming, especially when multiple diseases share overlapping symptoms.

### Goal:
> To build a smart, ML-driven diagnostic assistant that interprets standard blood test values and predicts probable diseases in real-time—**accurately, efficiently, and accessibly.**

---

## 🎯 Key Features

- **Multi-label Disease Prediction** from a single test input
- **Built with Real-World Hospital Data (~90,000 records)**
- Dual-model support: **Random Forest & XGBoost**
- **Robust Preprocessing Pipeline** with:
  - Median & KNN imputation
  - Outlier handling
  - Feature selection
- **Interactive Web Interface** via Streamlit
- Upload single entries or **CSV files for batch predictions**
- Real-time feedback with **disease probabilities & confidence scores**
- Model metrics (F1, precision, recall, etc.) displayed transparently

---

## 🩺 Diseases Predicted

The model is capable of predicting **17+ medical conditions**, including:

- Anemia types (Iron Deficiency, Hemolytic, Pernicious)
- Vitamin B12 & Folate Deficiency
- Chronic Kidney Disease (CKD)
- Sepsis, Malaria, Dengue
- Liver Disease
- Leukemia & Multiple Myeloma
- Hypothyroidism
- Autoimmune Disorders
- Thalassemia
- Myelodysplastic Syndrome
- Aplastic Anemia
- General Infections

---

## 🏗️ How It Works

### 1. Input Module  
Accepts blood test values either via form fields or CSV upload.

### 2. Preprocessing Module  
- Removes irrelevant/invalid data
- Handles missing values (median → KNN)
- Normalizes and standardizes numerical values
- Encodes disease labels for multi-label classification

### 3. ML Prediction Module  
- Applies trained **Random Forest** and **XGBoost** models
- Predicts diseases with associated probabilities
- Ranks features by importance for interpretability

### 4. Output & Evaluation  
- Shows predicted conditions
- Displays model metrics (accuracy, F1 scores, Hamming Loss)
- Graphs for condition probabilities

---

## 📊 Model Performance (XGBoost Example)

- **Training Accuracy**: 97.37%  
- **Testing Accuracy**: 94.99%  
- **F1 Score (Micro)**: 0.9779  
- **F1 Score (Macro)**: 0.9749  
- **Hamming Loss**: 0.0043  

---

## ⚙️ Tech Stack

- **Language**: Python  
- **Framework**: Streamlit (for UI)  
- **Libraries**:  
  - pandas, numpy (data handling)  
  - scikit-learn (ML framework)  
  - xgboost (model training)  
  - matplotlib, seaborn (visualization)

---

## 🖥️ Installation Guide

1. **Clone the Repository**
```bash
git clone https://github.com/your-username/smart-blood-test-interpreter.git
cd smart-blood-test-interpreter
