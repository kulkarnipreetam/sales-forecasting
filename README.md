# 📈 Forecasting Sales — Kaggle Store Sales Time Series Competition

The goal of this Kaggle competition was to **forecast daily sales** of 33 product families across 54 stores in Ecuador for the period **August 16–30, 2017**.  
The training dataset consisted of ~**3 million rows of sales transactions** covering **January 1, 2013 to August 15, 2017**.  
Additional data on **holidays 🏖️**, **oil prices ⛽**, and **store transactions 🏬** were also provided.  

---

## 🔍 Exploratory Data Analysis (EDA)

- 📊 Identified product families with strong **seasonal spikes**, particularly around New Year 🎉.  
- 📈 Examined **trend and seasonality** in sales using deterministic process features.  
- 🔁 Explored **autocorrelation and partial autocorrelation** to assess temporal dependencies.  

---

## 🧠 Modeling Approaches

Three models were developed and submitted:  

### 1. **Multivariate Linear Regression**
- Built using **Deterministic Process** with:
  - Trend and seasonal Fourier features 📅  
  - Holiday 🏖️ and New Year 🎉 indicators  
- Fitted across all stores and families simultaneously (multivariate setup).  
- Submission clipped negative predictions to zero for RMSLE compatibility.  

📌 **Kaggle Public Score:** `0.64608 RMSLE`  

---

### 2. **Neural Network 🤖**
- Features included:
  - Day of week 📅  
  - Week number  
  - Oil prices ⛽  
  - Holiday 🏖️ / New Year 🎉 indicators  
  - Store 🏬 and family 🛍️ identifiers  
  - Number of products on promotion 🏷️  
- Trained on data from **Jan 2016 – Aug 2017**.  

📌 **Kaggle Public Score:** `0.89728 RMSLE`  

---

### 3. **XGBoost 🌲**
- Used the same feature set as the neural network.  
- Despite strong performance in many forecasting tasks, it performed worse here due to difficulty modeling strong seasonality and trend.  

📌 **Kaggle Public Score:** `1.23260 RMSLE`  

---

## ✅ Results & Insights

- **Best model:** Multivariate Linear Regression (`0.64608 RMSLE`)  
- Neural network performed reasonably (`0.89728 RMSLE`)  
- XGBoost underperformed (`1.23260 RMSLE`)  
- While R² was used for instructional evaluation in class (regression fit), **RMSLE was the true Kaggle competition metric**  
- Incorporating **lag features** or **store/family-specific models** could further improve accuracy  

---

## Important Notice

The code in this repository is proprietary and protected by copyright law. Unauthorized copying, distribution, or use of this code is strictly prohibited. By accessing this repository, you agree to the following terms:

- **Do Not Copy:** You are not permitted to copy any part of this code for any purpose.
- **Do Not Distribute:** You are not permitted to distribute this code, in whole or in part, to any third party.
- **Do Not Use:** You are not permitted to use this code, in whole or in part, for any purpose without explicit permission from the owner.

If you have any questions or require permission, please contact the repository owner.

Thank you for your cooperation.
