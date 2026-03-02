# 🚆 Train Delay Prediction for Operational Optimization  
### Ctrl_F_Strat_Quest | Finalist Hackathon Project - Spring Fest, 2026 (IIT Kharagpur)

---

## 📌 Overview  

This project analyzes train delay patterns in **Indian Railways** and builds a predictive, decision-support framework to improve:

- On-Time Performance (OTP)  
- Operational prioritization  
- Resource allocation  
- Passenger communication  

Instead of focusing only on prediction accuracy, this project emphasizes **interpretability, operational impact, and real-world applicability**.

---

## 🎯 Objective  

To identify key drivers of train delays and design a system that:

- Predicts arrival delays  
- Detects cascading delay risks  
- Helps prioritize high-impact operational interventions  

---

## 📊 Dataset  

- ~100,000 simulated station-arrival records  
- 30 features covering scheduling, operational, and environmental factors  

### Key Feature Groups  

### 1️⃣ Scheduling & Route
- Distance_km  
- Number_of_Stops  
- Scheduled & Actual timings  

### 2️⃣ Operational Disruptions
- Signal_Failure  
- Track_Maintenance  
- Engine_Breakdown  
- Crew_Change  

### 3️⃣ Network Effects
- Previous_Train_Delay_min  

### 4️⃣ Passenger & Weather
- Passenger_Load_pct  
- Temperature, Humidity, Visibility  
- WeatherCondition  

**Target Variable:**  
`Arrival_Delay_min`

---

## 🧹 Data Preprocessing  

- Removed unnecessary index column  
- Converted timestamp columns to datetime  
- Handled missing values  
- Normalized passenger load  
- Encoded binary operational flags  

---

## 📈 Exploratory Data Analysis  

### Key Insights  

- **32.7% of trains** experience delays exceeding 15 minutes  
- Evidence of **delay propagation** (correlation ≈ 0.26 with previous train delay)  
- Engine breakdowns cause extreme delay amplification  
- High passenger load significantly increases delay risk  

---

## 🤖 Model Used  

### Random Forest Regressor  

**Why Random Forest?**

- Robust to noise  
- Handles non-linear interactions  
- Provides interpretable feature importance  
- Suitable for operational decision support  

### 🔑 Top Predictive Features  

1. Passenger_Load_pct  
2. Distance_km  
3. Number_of_Stops  
4. Previous_Train_Delay_min  
5. Engine_Breakdown  

---

## 🧠 Strategic Impact  

### 🚦 Operational Optimization
- Prioritize trains following heavily delayed services  
- Rapid intervention for signal failures & breakdowns  

### ⚙️ Resource Allocation
- Assign reliable locomotives to high passenger-load routes  
- Minimize crew changes during congestion windows  

### 😊 Passenger Experience
- Use delay risk signals for proactive ETA updates  
- Improve transparency and trust  

---

## 🚀 Future Improvements  

- Integration with real-time railway feeds  
- Live dashboard for control rooms  
- Delay cost optimization modeling  
- Zone-specific model customization  

---

## 👥 Team - Ctrl F  

**Sagnik Das** – Data Analysis, Modeling & Technical Implementation  
**Arvik Bag** – Strategy Design, Presentation & Operational Framing  

---

## 🏆 Hackathon Note  

This solution was designed as a **decision-support framework**, not just a prediction model. We stood **8th out of 1.3K teams** across the nation

> "Prediction becomes powerful only when it leads to operational action."
