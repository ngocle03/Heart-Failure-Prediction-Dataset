# Understanding Heart Disease Risk Factors through Health and Demographic Analysis

---

## 🎯 Goals of the Project
**Purpose:**  
To analyze medical and demographic data of patients to identify key factors associated with heart disease. The project focuses on comparing risk across different patient groups and highlighting the most significant contributors.

**Expected Outcomes:**  
- 📊 A clear understanding of how age, gender, cholesterol, blood pressure, and chest pain type relate to heart disease prevalence.  
- 👥 Profiles of high-risk groups based on demographics and symptoms.  
- 💡 Actionable insights to support preventive healthcare strategies.  

---

## 📂 Data Sources Used
The data for this analysis was sourced from a public dataset on Kaggle:  

- **Dataset Name:** Heart Failure Prediction Dataset  
- **Source Link:** [Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)  

---

## 🗂️ Data Overview
The dataset contains anonymized medical and demographic details of patients. It is structured as a single table with the following columns:  

- 👵 **Age** – Age of the patient  
- 🚹 **Sex** – Gender of the patient  
- 💔 **ChestPainType** – Type of chest pain experienced  
- 🩸 **RestingBP** – Resting blood pressure  
- 🧪 **Cholesterol** – Serum cholesterol  
- 🍬 **FastingBS** – Fasting blood sugar  
- 📈 **RestingECG** – Resting electrocardiogram results  
- ❤️‍🔥 **MaxHR** – Maximum heart rate achieved  
- 😣 **ExerciseAngina** – Exercise-induced angina  
- 📉 **Oldpeak** – Depression induced by exercise relative to rest  
- 📊 **ST_Slope** – Slope of the peak exercise ST segment  
- 🩺 **HeartDisease** – Presence of heart disease  

---

## 🛠️ Tools and Technologies Applied
The analysis was performed using **Python** and the following libraries:  
- 🐼 **Pandas** → Data manipulation and analysis  
- 📊 **Matplotlib.pyplot** → Visualization and charts  
- 🌈 **Seaborn** → Statistical plots and heatmaps  


---

## 🔄 ETL Pipeline  

### 1️⃣ Extract  
Downloaded the dataset directly from Kaggle using `kagglehub`:  

```python
import kagglehub
import os
import pandas as pd

# Download dataset
path = kagglehub.dataset_download("fedesoriano/heart-failure-prediction")
csv_path = os.path.join(path, "heart.csv")
df = pd.read_csv(csv_path)
df.head()


---

## 🔑 Key Insights Discovered
The analysis revealed several key findings:  

- 👵 **Age:** Heart disease prevalence increases with age, rising from ~34% in the 30–39 age group to over 70% in those aged 60+.  
- 🚹 **Gender:** Males consistently show higher prevalence. For example, in the 30–39 age group, 40% of males have heart disease vs. 16% of females.  
- 😣 **Exercise-Induced Angina:** A strong predictor — ~85% of patients with it have heart disease, compared to only 35% without.  
- 💔 **Chest Pain Type:** **Asymptomatic (ASY)** chest pain is most common among heart disease patients (~80%), showing many patients may lack classic symptoms.  
- 🧾 **Medical Indicators:**  
  - ❤️‍🔥 **MaxHR:** Strong negative correlation with heart disease (-0.40).  
  - 📉 **Oldpeak:** Strong positive correlation (0.40).  
  - 🩸 **RestingBP** & 🧪 **Cholesterol:** Very weak correlation → poor predictors.  

---

## 🧪 Hypotheses Based on the Insights
From the insights, three hypotheses were formed:  

1. ⚡ Heart disease risk increases significantly with age, especially after **50 years old**.  
2. 🚹 **Males** are at consistently higher risk than females, regardless of age.  
3. 🔍 **MaxHR** and **Oldpeak** are stronger predictors than traditional measures like blood pressure or cholesterol.  

---

## 🩺 Recommendations Based on Analysis Results

The findings point toward both **clinical screening** 🩺 and **preventive healthcare strategies** 🛡️ to address heart disease risk.

### ⚠️ Target High-Risk Groups
- Focus preventive and diagnostic efforts on **males** and **individuals over 50**, as they consistently show the highest prevalence rates.

### 🔍 Prioritize Strong Predictors in Screening
- Emphasize **MaxHR** and **Oldpeak** during risk evaluation, as they are stronger predictors than traditional measures like cholesterol or resting blood pressure.  
- Treat **exercise-induced angina** as a red flag 🚨 — with ~85% prevalence among patients with heart disease, it should trigger early clinical screening.

### 🩺 Maintain Core Diagnostic Practices
- Continue routine tests such as **blood pressure, cholesterol, and exercise tolerance** to ensure comprehensive evaluation.  
- Prioritize screening for patients with **abnormal or asymptomatic chest pain**, since traditional symptom-based detection may miss these cases.

### ✅ Preventive Healthcare Strategies
- **Lifestyle Modifications:** Encourage dietary improvements 🥗, regular exercise 🏃, and smoking cessation 🚭, particularly for **older males**, **hypertensive patients**, and those with **high cholesterol**.  
- **Tailored Exercise Programs:** Provide supervised programs for patients with borderline angina to strengthen cardiovascular function safely.  
- **Awareness Campaigns:** Educate both the public 📢 and healthcare providers that heart disease often occurs **without classic chest pain**, reducing the risk of under-diagnosis.

> **Summary:** By targeting high-risk populations ⚡, emphasizing stronger predictors in screening 🔎, and reinforcing lifestyle-based prevention ✅, healthcare providers can reduce both the prevalence and late detection of heart disease.
