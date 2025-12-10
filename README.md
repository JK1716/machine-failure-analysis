# 📊 Machine Failure Analysis
**Dataset:** AI4I 2020 Predictive Maintenance Dataset  
**Tools Used:** Microsoft Excel (Power Query, PivotTables, Charts), Basic Engineering Metrics

---

## 📌 Project Overview
This project analyzes **10,000 manufacturing records** to understand the conditions leading to machine failures.  
Failures are categorized into:

- **TWF** — Tool Wear Failure  
- **HDF** — Heat Dissipation Failure  
- **PWF** — Power Failure  
- **OSF** — Overstrain Failure  
- **RNF** — Random Failure

The goal is to identify which product types (L, M, H) and operating conditions contribute most to these failures.

---

## 🎯 Key Findings

### 🔥 Heat Dissipation Failure (HDF)
- Temperature difference (≈10 K) is similar across all types.
- **Type L** shows the highest HDF rate (**1.27%**).
- Suggests thermal load accumulates more during L-type cycles.

### ⚙️ Overstrain Failure (OSF)
- ToolWear × Torque is used as a mechanical load indicator.
- **Type L** has the highest mechanical load and the highest OSF rate (**1.45%**).

### ⚡ Power Failure (PWF)
- Power (Torque × RPM) is nearly identical across types.
- **Type M** exhibits the highest PWF rate (**1.03%**).

### 🛠️ Tool Wear Failure (TWF)
- All types have similar tool wear (~107–108 min).
- **Type H** shows the highest TWF rate (**0.70%**), consistent with faster wear (Type H adds +5 min per cycle).

### 🎲 Random Failure (RNF)
- Very low overall (<0.5%).
- Slightly higher in **Type H**.

---

## 📈 Dashboard Design (Excel)

### 🔹 **KPIs**

#### 1️⃣ Clustered Bar Chart — Count of Products by Product Type

<p align="left">
  <img src="Visuals/Product_count.png" width="300">
   <img src="Visuals/Product_count_KPI.png" width="250">
</p>

#### 2️⃣ Combo Chart (Clustered Column + Stacked Line) — Machine Failure Analysis by Product Type

<p align="left">
  <img src="Visuals/Failure_count.png" width="300">
   <img src="Visuals/Failure_count_KPI.png" width="250">
</p>  

### 3️⃣ Pie Chart — Machine Failure Types Breakdown

<p align="left">
  <img src="Visuals/Failure_breakdown.png" width="300">
</p>  

| <img src="Visuals/HDF.png" width="300"/> | <img src="Visuals/OSF.png" width="250"/> |<img src="Visuals/PWF.png" width="250"/> |<img src="Visuals/TWF.png" width="250"/> |<img src="Visuals/RNF.png" width="250"/> |
|--------------|--------------------|--------------------|--------------------|--------------------|

### 🔻 **Cause–Effect Analysis**
 
#### 🔥 HDF — Heat Dissipation Failure

<p align="left">
  <img src="Visuals/HDF_Failure_distribution.png" width="400">
</p>

#### ⚙️ OSF — Overstrain Failure

<p align="left">
  <img src="Visuals/OSF_load_imapct.png" width="400">
</p>

#### ⚡ PWF — Power Failure

<p align="left">
  <img src="Visuals/PWF_Power_load_effect.png" width="400">
</p>

#### 🛠️ TWF — Tool Wear Failure

<p align="left">
  <img src="Visuals/TWF_wear_level.png" width="400">
</p>

#### 🎲 RNF — Random Failure

<p align="left">
  <img src="Visuals/RNF_Failure_distribution.png" width="400">
</p>

## 🧪 Engineering Interpretation

### **HDF — Heat Dissipation Failure**
- Caused by thermal imbalance.  
- Even small ∆T variations create hotspots.  
- Type L’s higher frequency of cycles increases cumulative heat exposure.

### **OSF — Overstrain Failure**
- Higher mechanical load (Torque × ToolWear) leads to structural stress.  
- Type L operations show the greatest strain → highest OSF.

### **PWF — Power Failure**
- Caused by electrical overload or unstable torque–speed combinations.  
- Type M has the highest PWF despite similar power levels → suggests load sensitivity.

### **TWF — Tool Wear Failure**
- Tool failure occurs at 200–240 min wear threshold.  
- Type H adds the most wear per cycle → reaches threshold faster.

### **RNF — Random Failure**
- Stochastic events that don’t correlate with metrics.  
- Slightly higher in Type H due to elevated operational intensity.

---

## 🚀 Suggested Improvements & Next Steps

### ✔ 1. Predictive Modeling (Excel or Python)
- Logistic Regression to predict failure probability  
- Random Forest for identifying key drivers  

### ✔ 2. Control Chart / SPC Integration
- Monitor torque, rpm, temperature, and tool wear  
- Identify abnormal process behavior  

### ✔ 3. Preventive Maintenance Rules
Examples:
- Replace tool at **180 min** instead of near 200–240 min  
- Limit torque spikes to reduce OSF  
- Introduce cooling cycles for Type L production  

### ✔ 4. Develop a Live Excel Dashboard  
Refreshable via Power Query.

---

## 🧾 Files Included
### 📂 Data/
- `ai4i2020_raw.csv` – Original dataset  
- `Machine_Failure_Cleaned.csv` – Cleaned dataset  

### 📂 Excel/
- `Machine_Failure_Analysis.xlsx` – Full Excel dashboard & analysis  

### 📂 Visuals/
- KPI cards  
- Charts for each failure mode  

### 📄 README.md
Project overview. 

---

## 📧 Contact
**Kalkidan Tsegaye — Electromechanical & Data Analyst**  
📍 Addis Ababa, Ethiopia  
📧 kalkidantsegaye171@gmail.com  
LinkedIn: www.linkedin.com/in/kalkidan-tsegaye  
