# 🚗 AcciSense – Intelligent Road Accident Risk Prediction System

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-Backend-green)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-RandomForest-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

# 📌 Overview

AcciSense is an AI-powered road accident risk prediction system designed to estimate accident probability using vehicle dynamics, road conditions, traffic density, visibility, and tyre health.

The system analyzes real-time driving inputs and predicts whether the driving situation is:

- 🟢 SAFE
- 🟡 MEDIUM RISK
- 🔴 HIGH RISK

Along with risk prediction, the system explains the most influential factors contributing to accident risk, making the model more interpretable and useful for safety analysis.

---

# 🎯 Problem Statement

Road accidents occur due to a combination of factors such as:

- Overspeeding
- Sudden braking
- Poor road conditions
- High traffic congestion
- Low visibility
- Worn tyre conditions

Traditional monitoring systems often fail to provide proactive risk assessment.

AcciSense addresses this problem by using Machine Learning to evaluate multiple driving conditions simultaneously and estimate accident risk before an accident occurs.

---

# ✨ Key Features

### Intelligent Risk Prediction

Predicts accident probability in real time.

### Explainable AI

Displays the top contributing risk factors.

### Feature Engineering

Generates advanced driving indicators:

- Speed-Brake Ratio
- Steering Intensity
- Visibility Risk

### REST API Support

Prediction APIs built using Flask.

### Route Visualization

Uses routing services for path generation.

### Interactive Dashboard

Visual representation of:

- Risk Meter
- Prediction Results
- Vehicle Movement
- Risk Contributors

---

# 📊 Dataset Information

## Dataset Type

Synthetic Driving Dataset

## Dataset Source

Self-generated using custom Python simulation scripts.

## Dataset Cost

₹0

## Total Records

15,000

## Features

| Feature | Description |
|----------|-------------|
| Speed | Vehicle speed |
| Brake | Braking intensity |
| Steering | Steering angle |
| Road | Dry / Wet road |
| Traffic | Traffic density |
| Visibility | Driver visibility |
| Tyre | Tyre condition |

---

# ⚙ Feature Engineering

Three additional engineered features were created:

### Speed-Brake Ratio

Measures aggressive driving behavior.

### Steering Intensity

Captures sharp steering movements.

### Visibility Risk

Represents weather-related visibility danger.

Total Features Used By Model:

10 Features

---

# 🧠 Machine Learning Pipeline

Data Generation
↓
Data Cleaning
↓
Feature Engineering
↓
Label Encoding
↓
Train-Test Split
↓
Random Forest Training
↓
Performance Evaluation
↓
Model Deployment
↓
Flask API
↓
Interactive Dashboard

---

# 🤖 Model Used

## Random Forest Classifier

Parameters:

- n_estimators = 200
- max_depth = 10
- class_weight = balanced
- random_state = 42

Why Random Forest?

✔ Handles nonlinear relationships

✔ Reduces overfitting

✔ Works well with mixed feature types

✔ Provides feature importance scores

---

# 📈 Model Performance

| Metric | Score |
|----------|----------|
| Accuracy | 86.10% |
| Precision | 89.54% |
| Recall | 86.10% |
| F1 Score | 86.14% |

---

# 📊 Class Distribution

| Risk Level | Samples |
|------------|---------|
| SAFE | 1,585 |
| MEDIUM | 8,843 |
| HIGH | 4,572 |

---

# 🔍 Feature Importance Analysis

The trained model identified the following factors as most influential:

1. Traffic Condition
2. Road Condition
3. Tyre Condition
4. Brake Intensity
5. Steering Intensity

These results indicate that environmental and vehicle-condition factors contribute significantly to accident risk prediction.

---

# 📸 Feature Importance Visualization

Add your uploaded image:

```md
![Feature Importance](images/accident_top_features.png)
```

---

# 🚀 REST API Endpoints

## Prediction API

POST

```http
/predict
```

### Sample Request

```json
{
  "speed": 90,
  "brake": 60,
  "steering": 20,
  "road": 1,
  "traffic": 2,
  "visibility": 40,
  "tyre": 1
}
```

### Sample Response

```json
{
  "risk": "HIGH",
  "risk_probability": 87.4
}
```

---

## Route Generation API

POST

```http
/get-route
```

Generates routes between source and destination coordinates.

---

# 🛠 Tech Stack

## Backend

- Python
- Flask
- Scikit-Learn
- Joblib

## Machine Learning

- Random Forest
- XGBoost

## Frontend

- HTML
- CSS
- JavaScript

## Visualization

- Matplotlib
- Leaflet.js
- Gauge.js

## Data Processing

- NumPy
- Pandas

---

# 📂 Project Structure

AcciSense/
│
├── app.py
├── accisense_model.pkl
├── label_encoder.pkl
├── accisense_dataset.csv
├── requirements.txt
│
├── training/
│ ├── train_accisense_model.py
│ ├── rf_model_train.py
│ └── model_compare.py
│
├── preprocessing/
│ ├── data_generation.py
│ ├── detect_outliers.py
│ └── feature_importance.py
│
├── images/
│ └── accident_top_features.png
│
└── demo/
└── demo_video.mp4

---

# 🎥 Demo

## Dashboard Preview

Add screenshots here:

```md
![Dashboard](images/dashboard.png)
<img width="1599" height="899" alt="Accisense Screenshot 2" src="https://github.com/user-attachments/assets/79588440-4050-458e-81b5-3cd363ebc901" />

```

```md
![Prediction](images/prediction.png)
```<img width="1599" height="899" alt="Accisense Screenshot 1" src="https://github.com/user-attachments/assets/5f2aab1f-53a4-4db3-87d4-434cb2a5d611" />


---

## Video Demonstration

```md
[Watch Demo Video](demo/demo_video.mp4)
```

or

```md
[YouTube Demo](YOUR_YOUTUBE_LINK)
```

---

# 🔮 Future Enhancements

- Real-world traffic integration
- Weather API integration
- Deep Learning models
- Mobile Application
- IoT Sensor Support
- Driver Behavior Analytics
- Real-time Vehicle Monitoring

---

# 💼 Resume Highlights

- Developed an end-to-end Machine Learning system for accident risk prediction.
- Generated and engineered driving-risk datasets with 15,000 records.
- Built REST APIs using Flask for real-time inference.
- Implemented Explainable AI using feature importance analysis.
- Created an interactive dashboard with visualization support.
- Integrated route-generation services for driving simulation.

---

# 👩‍💻 Author

Shaily Gupta

GitHub:
https://github.com/shaily27

---

⭐ If you found this project useful, consider giving it a star.
