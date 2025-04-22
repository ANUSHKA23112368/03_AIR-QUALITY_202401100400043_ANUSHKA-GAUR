# 03_AIR-QUALITY_202401100400043_ANUSHKA-GAUR
 🌫️ Air Quality Classification Using Rule-Based Logic

This project aims to classify air quality levels based on PM2.5, NO2, and temperature data using a simple rule-based approach. It provides a quick and interpretable way to evaluate air pollution levels and categorize them into meaningful health-based categories.

---

## 📌 Project Overview

- **Goal:** Classify air quality into five categories:  
  `Good`, `Moderate`, `Unhealthy for Sensitive Groups`, `Unhealthy`, `Very Unhealthy`.
- **Inputs:** PM2.5, NO2, and Temperature readings.
- **Method:** Rule-based classification using threshold values aligned with AQI guidelines.

---

## 🧠 Methodology

1. **Data Loading:** Import CSV dataset using Pandas.
2. **Data Processing:** Clean and inspect basic statistics.
3. **Classification:** Apply a custom function using pollutant thresholds.
4. **Results:** Label each data point with the appropriate air quality category.

---

## 🧪 Sample Classification Logic

```python
def classify_air_quality(pm25, no2, temperature):
    if pm25 <= 12 and no2 <= 53:
        return "Good"
    elif pm25 <= 35.4 and no2 <= 100:
        return "Moderate"
    elif pm25 <= 55.4 or no2 <= 360:
        return "Unhealthy for Sensitive Groups"
    elif pm25 <= 150.4 or no2 <= 649:
        return "Unhealthy"
    else:
        return "Very Unhealthy"
✅ Results Summary
Most data entries were classified as Unhealthy or Very Unhealthy.

The rule-based system performed well for basic classification.

Future work may include data visualization and machine learning enhancement.

📁 Files Included
air_quality.csv – Dataset used for classification

air_quality_classification.ipynb – Jupyter Notebook with full implementation

README.md – Project documentation

📚 References
EPA Air Quality Index (AQI)

WHO Air Pollution Guidelines

Pandas Documentation

Google Colab

🚀 How to Run
Clone this repo

Open air_quality_classification.ipynb in Google Colab or Jupyter Notebook

Run all cells to see classification results

