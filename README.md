# 🚢 Ship Engine Anomaly Detection
---

## 📌 Overview
This project focuses on detecting anomalous ship engine behavior using statistical and machine learning techniques.

Anomalies represent unusual combinations of engine feature values that may indicate potential failures or inefficiencies.

- ⛽ Increased fuel consumption
- ⚙️ Reduced engine efficiency
- 🚢 Delivery delays
- 💰 Higher maintenance costs
- ⚠️ Operational and safety risks

---

## 🧠 Problem Statement
The goal is to detect unusual combinations of ship engine sensor readings across six key features:

- Engine RPM
- Oil pressure
- Fuel pressure
- Coolant pressure
- Oil temperature
- Coolant temperature

Anomalies represent rare or abnormal patterns that may indicate early signs of engine malfunction.

---

## 🏗️ Methodology

### 1. Exploratory Data Analysis (EDA)
- Statistical summary of engine features
- Distribution analysis using histograms and boxplots
- Identification of potential outliers

### 2. Data Preprocessing
- Feature scaling for uniform contribution
- Principal Component Analysis (PCA) for visualization

### 3. Anomaly Detection Models
Two machine learning approaches were used:

- One-Class SVM (RBF kernel)
- Isolation Forest

Both models were tuned to detect approximately **1–5% anomalies**.

---

## 📊 Key Results

### 🔹 IQR-Based Outlier Analysis
- Lubricating oil temperature: 13.4% outliers
- Fuel pressure: 5.81% outliers
- Oil pressure: 0.34% outliers
- Coolant temperature: 0.01% outliers

Threshold tuning showed that **threshold = 2** best captures meaningful anomalies.

---

### 🔹 One-Class SVM
- Nu = 0.01
- Anomaly rate ≈ 1.01%
- Detects boundary-based deviations in engine behavior

---

### 🔹 Isolation Forest
- Contamination = 0.01
- Anomaly rate ≈ 1.00%
- Strong performance in isolating extreme outliers

---

### 🔹 Model Comparison
- SVM: tighter decision boundary
- Isolation Forest: better detection of isolated extreme anomalies
- Both methods show strong agreement on core anomaly regions

---

## 📈 Key Insight
Most engine operations are stable, but anomalies occur when **multiple sensor features deviate simultaneously**.

This confirms that engine failures are driven by **multi-variable interactions**, not single-feature spikes.

---

## 📉 Visualization
- PCA used for 2D projection of high-dimensional data
- Clear separation between normal and anomalous points
- Boxplots and histograms confirm feature-level outliers

---

## 💼 Business Impact
This system enables:
- Early detection of engine issues
- Reduced maintenance costs
- Improved fuel efficiency
- Prevention of unexpected breakdowns
- Enhanced operational safety

---

📄 [View Full Report](./ship_engine_anomaly_detection.pdf)

---

## ⭐ Summary
This project demonstrates how combining statistical analysis with machine learning can effectively detect anomalies in ship engine systems and support predictive maintenance strategies.
