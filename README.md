# Understanding Heart Disease Risk Factors through Health and Demographic Analysis

---

#### 1. Goals of the Project
**Purpose:**  
To analyze medical and demographic data of patients to identify key factors associated with heart disease. The project focuses on comparing risk across different patient groups and highlighting the most significant contributors.

**Expected Outcomes:**  
- A clear understanding of how age, gender, cholesterol, blood pressure, and chest pain type relate to heart disease prevalence.  
- Profiles of high-risk groups based on demographics and symptoms.  
- Actionable insights to support preventive healthcare strategies.  

---

#### 2. Data Sources Used
The data for this analysis was sourced from a public dataset on Kaggle:  

- **Dataset Name:** Heart Failure Prediction Dataset  
- **Source Link:** [Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)  

---

#### 3. Data Overview
The dataset contains anonymized medical and demographic details of patients. It is structured as a single table with the following columns:  

- **Age:** Age of the patient  
- **Sex:** Gender of the patient  
- **ChestPainType:** Type of chest pain experienced  
- **RestingBP:** Resting blood pressure  
- **Cholesterol:** Serum cholesterol  
- **FastingBS:** Fasting blood sugar  
- **RestingECG:** Resting electrocardiogram results  
- **MaxHR:** Maximum heart rate achieved  
- **ExerciseAngina:** Exercise-induced angina  
- **Oldpeak:** Depression induced by exercise relative to rest  
- **ST_Slope:** Slope of the peak exercise ST segment  
- **HeartDisease:** Presence of heart disease  

---

#### 4. Tools and Technologies Applied
The analysis was performed using **Python** and the following libraries:  
- **Pandas** → Data manipulation and analysis  
- **Matplotlib.pyplot** → Visualization and charts  
- **Seaborn** → Statistical plots and heatmaps  

---

#### 5. Key Insights Discovered
The analysis revealed several key findings:  

- **Age:** Prevalence of heart disease increases with age, rising from ~34% in the 30–39 age group to over 70% in those aged 60+.  
- **Gender:** Males consistently show higher prevalence. For example, in the 30–39 age group, 40% of males have heart disease vs. 16% of females.  
- **Exercise-Induced Angina:** A strong predictor — ~85% of patients with it have heart disease, compared to only 35% without.  
- **Chest Pain Type:** **Asymptomatic (ASY)** chest pain is most common among heart disease patients (~80%), indicating many patients may lack classic symptoms.  
- **Medical Indicators:**  
  - `MaxHR`: Strong negative correlation with heart disease (-0.40).  
  - `Oldpeak`: Strong positive correlation (0.40).  
  - `RestingBP` and `Cholesterol`: Very weak correlation, making them poor predictors.  

---

#### 6. Hypotheses Based on the Insights
From the insights, three hypotheses were formed:  

1. Heart disease risk increases significantly with age, especially after **50 years old**.  
2. **Males** are at consistently higher risk than females, regardless of age.  
3. **MaxHR** and **Oldpeak** are stronger predictors than traditional measures like blood pressure or cholesterol.  

---

#### 7. Recommendations Based on Analysis Results
The results suggest the following preventive healthcare strategies:  

- **Target High-Risk Groups:** Focus prevention on **males** and individuals **over 50**.  
- **Prioritize Strong Predictors:** Emphasize **MaxHR** and **Oldpeak** in screening over weaker indicators (e.g., cholesterol).  
- **Raise Awareness of Atypical Symptoms:** Educate that heart disease can occur without classic chest pain, given the high prevalence in **asymptomatic (ASY)** cases.  
- **Address Exercise-Induced Angina Promptly:** Given its ~85% prevalence among heart disease patients, this should trigger immediate preventive action.  
