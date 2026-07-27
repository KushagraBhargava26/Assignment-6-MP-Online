# Weather Classification using SVM and Open-Meteo API

**Author:** Kushagra Bhargava

**Registration Number:** 23BAI10987

**Application Number:** IN26011651

**Batch Number:** 1A

**Email ID:** kushagra.23bai10987@vitbhopal.ac.in

---

# Objective

The objective of this assignment is to develop a Support Vector Machine (SVM) classification model that predicts whether the weather is **Warm** or **Cool** using meteorological data collected from the Open-Meteo Weather API. The project demonstrates the complete machine learning workflow including data collection, preprocessing, model development, and performance evaluation.

---

# API Documentation

**Open-Meteo Weather API (Free)**

https://open-meteo.com/

**Sample API Request**

```
https://api.open-meteo.com/v1/forecast?latitude=28.6139&longitude=77.2090&hourly=temperature_2m,relative_humidity_2m,surface_pressure,wind_speed_10m&forecast_days=7
```

---

# Libraries Used

- requests
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

# Dataset Description

The dataset is collected directly from the **Open-Meteo Weather API** and contains hourly weather observations.

### Input Features

- Temperature (°C)
- Relative Humidity (%)
- Surface Pressure (hPa)
- Wind Speed (km/h)

### Target Variable

**Weather_Class**

- Warm → Temperature ≥ 25°C
- Cool → Temperature < 25°C

> **Note:** If the fetched weather data contains only one class using the 25°C threshold, an adaptive median-temperature threshold is applied to generate both classes for demonstration purposes and to enable SVM training.

---

# Methodology

### 1. Data Collection

- Retrieved hourly weather data from the Open-Meteo API.
- Converted the JSON response into a Pandas DataFrame.

### 2. Data Preprocessing

- Checked for missing values.
- Removed unnecessary columns (Time).
- Created the `Weather_Class` target variable.
- Encoded the target labels using LabelEncoder.
- Split the dataset into 80% training and 20% testing sets.
- Standardized feature values using StandardScaler.

### 3. Model Development

- Built an SVM Classifier using the **RBF kernel**.
- Trained the model on the training dataset.
- Predicted weather classes for the testing dataset.

### 4. Model Evaluation

The model was evaluated using:

- Accuracy Score
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

# Results

The Support Vector Machine successfully classified weather observations into **Warm** and **Cool** categories using meteorological features.

Evaluation metrics generated include:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

The confusion matrix provides a visual representation of correctly and incorrectly classified weather instances.

---

# Observations

1. The SVM classifier effectively learned the relationship between meteorological features and weather categories.

2. Feature scaling significantly improved model performance because SVM relies on distance-based calculations.

3. The RBF kernel successfully handled the nonlinear relationship between weather parameters.

---

# Conclusion

This project demonstrated how real-time weather data from the Open-Meteo API can be used to build an SVM-based weather classification model. Meteorological features such as temperature, humidity, surface pressure, and wind speed were used to classify weather conditions into Warm and Cool categories. Data preprocessing, including label encoding and feature scaling, played a crucial role in improving model performance. The SVM classifier achieved reliable classification performance when evaluated using accuracy, precision, recall, F1-score, and confusion matrix.

### Advantages of SVM

- Performs well on high-dimensional datasets.
- Effectively models nonlinear decision boundaries using kernel functions.

### Limitations of SVM

- Computationally expensive for very large datasets.
- Requires careful selection of kernel parameters and hyperparameter tuning.

---

# Repository Structure

```
Assignment-6/
│
├── Assignment-6.ipynb
├── README.md
└── requirements.txt
```

---

# Requirements

```
requests
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

# Output

- Weather data fetched from Open-Meteo API
- Data preprocessing completed
- SVM model trained successfully
- Weather classification predictions generated
- Model evaluated using standard classification metrics
- Confusion Matrix visualized"# Assignment-6-MP-Online" 
