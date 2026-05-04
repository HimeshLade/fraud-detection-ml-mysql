# Fraud Detection ML System 🚀

[![Streamlit App](https://img.shields.io/badge/Streamlit-Running-green)](http://localhost:8501)

## Overview

Complete ML-based fraud detection using synthetic financial transactions (1M+ records). LogisticRegression model achieves **95% accuracy**. Interactive Streamlit app for predictions.

## 📸 Live Demo Screenshots
## Fraud Example :-
![Fraud Example](visuals/Fraud%20Example.png)

## Safe Example :-
![Safe Example](visuals/Safe%20Example.png)
## Quick Start 🏃‍♂️

```bash
pip install -r requirements.txt
python fraud_data_generator.py  # Generate Fraud.csv
python train_model.py           # Train → fraud_detection_model.pkl
streamlit run fraud_detection.py  # App at http://localhost:8501
```

## Key Features

- **Data**: 1M synthetic txns, realistic fraud rate (~0.13%)
- **Model**: Pipeline (OneHot + Scale + LogisticReg), 95% acc
- **App**: Predict fraud from type/amount/balances
- **Params for Fraud Demo**:
  | Type | Amount | OldOrg | NewOrg | OldDest | NewDest | Result |
  |-----------|--------|--------|--------|---------|---------|--------|
  | TRANSFER | 10000 | 10000 | 0 | 0 | 0 | ❌ Fraud |
  | DEPOSIT | 5000 | 10000 | 15000 | 20000 | 25000 | ✅ Safe |

## Files

- `fraud_data_generator.py`: Synthetic data
- `train_model.py`: Train & save model
- `fraud_detection.py`: Streamlit UI
- `requirements.txt`: Dependencies

Model performance:

```
Accuracy: 0.9467
Confusion Matrix: [[1804823 101499] [151 2313]]
```
