# AcciSense – Intelligent Road Accident Risk Prediction System

AcciSense is a machine learning-based web application system  designed to predict road accident risk using real-time driving conditions.
The system analyzes multiple factors such as speed, braking, steering, road condition, traffic, visibility, and tyre condition to estimate accident probability and identify key risk contributors.

The project combines data generation, model training, backend APIs, and a real-time simulation dashboard.

---

## Project Overview

The system works in three main stages:

1. Synthetic driving data is generated to simulate real-world conditions
2. A machine learning model is trained on engineered features
3. A web-based interface provides real-time prediction and visualization

The application also highlights the top contributing factors responsible for accident risk.

---

## Key Features

* Real-time accident risk prediction using machine learning
* Feature engineering for improved model accuracy
* Dynamic risk scoring mapped to SAFE, MEDIUM, and HIGH levels
* Identification of top risk contributing factors
* Interactive dashboard with live simulation
* Route visualization and vehicle movement simulation
* REST API for prediction and route generation

---

## Feature Importance Insight

The trained model identifies the most influential factors affecting accident risk.

* Traffic condition has the highest impact
* Road condition and tyre condition also contribute significantly
* Derived features such as speed-brake ratio and visibility risk enhance prediction quality

This analysis is generated using feature importance from the trained model

---

## Tech Stack

Backend:

* Python
* Flask (API development)
* Scikit-learn (Random Forest model)
* XGBoost (model comparison)
* Joblib (model persistence)

Frontend:

* HTML, CSS, JavaScript
* Leaflet.js (map visualization)
* Gauge.js (risk meter UI)

Libraries:

* NumPy
* Pandas
* Matplotlib
* Requests

Dependencies listed in: 

---

## Project Structure

```
AcciSense/
│── app.py                 # Flask backend (prediction + routing)
│── index.html            # Frontend dashboard
│── accisense_model.pkl   # Trained ML model
│── label_encoder.pkl     # Label encoder
│── accisense_dataset.csv # Generated dataset
│── requirements.txt
│
├── training/
│   ├── train_accisense_model.py
│   ├── rf_model_train.py
│   ├── model_compare.py
│
├── preprocessing/
│   ├── data_generation.py
│   ├── detect_outliers.py
│   ├── feature_importance.py
```

---

## How the System Works

### Data Generation

Synthetic driving data is generated using statistical distributions to simulate real-world driving patterns

### Feature Engineering

Additional features are created to improve prediction:

* Speed to brake ratio
* Steering intensity
* Visibility risk

### Model Training

A Random Forest model is trained and evaluated using classification metrics

### Prediction Logic

The system calculates a risk score and maps it to:

* SAFE
* MEDIUM
* HIGH

Real-time predictions are served through Flask APIs

---

## Running the Project

### 1. Clone Repository

```
git clone https://github.com/shaily27/AcciSense.git
cd AcciSense
```

### 2. Install Dependencies

```
pip install -r requirements.txt
```

### 3. Run Application

```
python app.py
```

Open in browser:

```
http://127.0.0.1:5000/
```

---

## Output

The system provides:

* Risk level (SAFE / MEDIUM / HIGH)
* Risk probability percentage
* Top 3 contributing conditions
* Real-time vehicle simulation with map

---

## Future Improvements

* Integration with real-world traffic and weather APIs
* Deep learning-based risk prediction
* Mobile application support
* Real-time IoT sensor integration
* Advanced analytics dashboard

---

## Author

Shaily Gupta
GitHub: https://github.com/shaily27

---

## License

This project is for academic and learning purposes.
