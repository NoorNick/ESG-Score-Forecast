# 🌍 ESG and Financial Performance Forecasting with Machine Learning

This project analyzes and forecasts company revenue and ESG (Environmental, Social, Governance) scores using historical ESG and financial data for 1,000 synthetic global companies from 2015 to 2025. It applies exploratory data analysis, feature engineering, and machine learning to uncover insights and predict future sustainability and financial performance.

---

## 📊 Dataset Overview

- **Time span**: 2015–2025  
- **Companies**: 1,000 (synthetic)  
- **Industries**: 9 sectors  
- **Regions**: 7 global regions  
- **Features include**:
  - Financial: Revenue, Profit Margin, Market Cap, Growth Rate
  - ESG: ESG_Overall, ESG_Environmental, ESG_Social, ESG_Governance
  - Resource Usage: Carbon Emissions, Water Usage, Energy Consumption

---

## 🧪 Project Objectives

- Forecast **Revenue** and **ESG_Overall Score** for each company.
- Understand ESG and financial trends by **region**, **industry**, and **time**.
- Engineer sustainability KPIs: *Emission Intensity*, *Energy Efficiency*, and *Water Efficiency*.
- Build a machine learning pipeline using **Random Forest** with **lag features**.

---

## ⚙️ Methodology

### 🔹 Data Preprocessing
- Handled missing values (e.g., filled `GrowthRate` with mean).
- Verified 11 rows per company (1 per year).
- Created custom ESG ratios for better insight.

### 🔹 Feature Engineering
- 1-year lag features for all time-dependent variables.
- One-hot encoding of categorical fields (`Industry`, `Region`).
- Custom KPIs: `EmissionIntensity`, `EnergyEfficiency`, `WaterEfficiency`.

### 🔹 Model
- **Random Forest Regressor** in a **MultiOutputRegressor** to forecast:
  - `Revenue`
  - `ESG_Overall`
- Trained using 80% of data (chronologically split) to preserve time structure.

---

## 📈 Results

- **R² Scores**:
  - Revenue: ~0.92
  - ESG_Overall: ~0.89
- **RMSE**:
  - Revenue: Within acceptable range (millions USD)
  - ESG Score: Within 5 points of true values

### 🔮 Forecast for 2026
Predicted Revenue and ESG scores using 2025 as input. Forecasts provide insights into companies’ future performance.

---

## 📌 Key Visualizations

- ESG Score trends by region
- Carbon emissions by industry & region
- Profit and energy efficiency comparisons
- Correlation heatmap between ESG and financial indicators

---

## 📂 Repository Structure
<pre>├── data/ # Data files or links to datasets 
│ └── ESG_data.csv # Cleaned ESG and financial dataset 
│ ├── notebooks/ # Jupyter notebooks
│ ├── 1-eda.ipynb # Exploratory Data Analysis (EDA & visuals) 
│ ├── 2-preprocessing.ipynb # Data cleaning, feature engineering 
│ └── 3-modeling.ipynb # Machine learning model development & forecasting 
├── src/ # Source code (utility functions, modules if needed) 
├── docs/ # Documentation and presentation 
│ └── presentation.md # Presentation script/notes 
├── requirements.txt # Project dependencies 
└── README.md # Project overview and instructions </pre>


---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/NoorNick/ESG-Score-Prediction.git
cd ESG-Score-Prediction
```
2. Install requirements:
```
pip install -r requirements.txt
```
3.  Open Jupyter Notebook:
```
jupyter notebook
```
4.   Run the notebooks in order:
```
preprocessing.ipynb
```
```
eda.ipynb
```
```
modeling.ipynb
```
