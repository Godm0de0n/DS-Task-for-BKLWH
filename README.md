This is an Assignment for Junior Data Scientist position at B.K.L Walawalkar Hospital

Submitted by Abhisek Nag

# 🩺 Maternal Health Data Analysis

This project performs an end-to-end exploratory data analysis (EDA) on maternal health data collected from three sources: basic demographics, delivery details, and postnatal follow-up. The goal is to uncover patterns, trends, and critical health insights using visualizations and statistics.

---

## 📁 Dataset Overview

The data is derived from three Excel sheets:

### 1. **Basic Information**
Contains demographic and health background of patients.
- `patient_id`, `ht`, `wt`
- `education`, `income`
- `ageatmenarche`, `ageatmarriage`, `ageatfirstpregnancy`
- `district`, `village`, `occupation`, `diet`, `condition`

### 2. **Delivery Information**
Captures data at the time of delivery.
- `patient_id`
- `dateofdelivery`, `ageatdelivery`, `weightatdelivery`
- `haemoglobinatdelivery`, `placentalweight`
- `termofdelivery`, `typeofdelivery` (e.g., Normal or Cesarean)

### 3. **Follow-up Information**
Follow-up health records across 4 visits post-delivery.
- BP and weight at each visit: `VisitX_bpdis`, `VisitX_bpsys`, `VisitX_wt`, `VisitX_date` (X = 1 to 4)

---

## 🔍 Analysis Workflow

1. **Data Merging & Cleaning**
   - Merged datasets on `patient_id`
   - Converted date columns to datetime
   - Handled missing values with proper imputation or filtering
   - Calculated derived metrics:
     - BMI = wt / (ht^2)
     - Avg systolic BP and diastolic BP
     - Weight change from Visit 1 to Visit 4

2. **Exploratory Data Analysis (EDA)**
   - Distribution of delivery types (Normal vs. Cesarean)
   - Cesarean delivery percentage by maternal condition
   - Haemoglobin levels by diet type
   - Top 5 villages by average systolic blood pressure
   - Weight and BP changes over follow-up visits

---

## 📊 Visualizations

- 🥧 **Delivery Type Distribution** – Pie chart showing Cesarean vs. Normal rates
- 📈 **Cesarean Rate by Condition** – Bar chart of Cesarean delivery % grouped by condition
- 🩸 **Haemoglobin by Diet** – Bar chart showing average haemoglobin levels by diet type
- 🧠 **BP by Village** – Top 5 villages with highest average systolic BP
- 📉 **BP and Weight Trends** – Line charts showing patient trends across 4 visits
- 🏋️ **Weight Change by Delivery Type** – Comparison of average weight gain/loss

---

## 💡 Key Insights

- ⚠️ **High BMI (>30)** in certain groups — recommend dietary counseling.
- 🩸 **Haemoglobin < 9 g/dL** indicates potential anemia — suggest iron supplements.
- 💓 **Avg Systolic BP > 140 mmHg** in some villages — risk of hypertension.
- 🍽️ **Diet and Haemoglobin**: Non-vegetarians showed lower average haemoglobin.
- 🚼 **Cesarean Delivery Rates** were significantly higher for patients with hypertension or anemia.

---

## 🛠️ Requirements

Run this project in **Google Colab** or your local environment.
or check this - https://colab.research.google.com/drive/1bzQoYMVtS-HGsXgumiLUhBZ7DK6KoxuW?usp=sharing (upload 3 files separately)

**Libraries Required:**
- pandas
- numpy
- matplotlib
- seaborn
- openpyxl

```bash
pip install pandas numpy matplotlib seaborn openpyxl
