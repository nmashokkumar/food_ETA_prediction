# 🚚 Delivery ETA Prediction using Machine Learning  
**Predicting delivery time using real-world food-delivery signals**

This project builds a machine learning model that predicts the **Estimated Time of Arrival (ETA)** for food-delivery orders.  
The dataset contains realistic operational features like distance, weather, traffic, restaurant load, courier experience, and vehicle type.

This project aligns with real logistics ML systems used by companies like **Swiggy, Zomato, Uber Eats**.

---

## 🧠 Problem Statement  
Given order, courier, restaurant, and environmental features, **predict the total delivery time (in minutes)**.

This helps improve:
- Customer experience (accurate ETA)
- Courier assignment
- Route optimization
- Restaurant load balancing

---

## 📌 Dataset Description  
Each row represents a delivery order with the following key features:

### **Input Features**
- `Distance_km`
- `Weather`
- `Traffic_Level`
- `Time_of_Day`
- `Vehicle_Type`
- `Preparation_Time_min`
- `Courier_Experience_yrs`
- `Restaurant_Load`
- `Restaurant_lat`, `Restaurant_lon`
- `Delivery_lat`, `Delivery_lon`
- `Is_Peak_Evening`

### **Target**
- `Delivery_Time_min` (regression)

Dataset size: **20,000 rows** (synthetic but highly realistic)

---

## 🛠️ ML Workflow

### **1. Data Cleaning & Preprocessing**
- Handle missing values  
- Handle categorical encoding  
- Outlier removal  
- Feature scaling (optional for tree models)

### **2. Feature Engineering**
- Peak-hour indicator  
- Traffic × Distance  
- PrepTime ÷ Courier Experience  
- Weather multiplier  
- Geo-distance approximation  

### **3. Model Training**
Models used:
- **RandomForestRegressor**
- **XGBoost Regressor**
- Linear Regression (baseline)

Random Forest & XGBoost performed best.

---

## 📊 Model Performance (example)
| Model | R² Score |
|-------|----------|
| Linear Regression | 0.55 |
| RandomForestRegressor | **0.75+** |
| XGBoostRegressor | **0.70+** |

---

## 📈 Key Insights
- Distance + Traffic + Prep Time are the most important features  
- Experienced couriers reduce ETA significantly  
- Evening is peak delay period  
- Rainy weather increases ETA by 10–20%

---

## 📦 Installation
```bash
pip install pandas numpy scikit-learn xgboost matplotlib
```


👨‍💻 Author

Ashok Kumar N
Aspiring Data Scientist
