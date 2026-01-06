# Predicting Diabetes Risk Using Health and Lifestyle Indicators

## Project Overview

Diabetes is one of the most prevalent chronic diseases in the United States, affecting millions of individuals and placing a substantial burden on public health systems and the economy. Early identification of individuals at risk is critical, as lifestyle interventions and timely medical care can significantly reduce disease progression and long-term complications.

This project applies machine learning classification techniques to health and lifestyle survey data to evaluate whether diabetes risk can be accurately predicted using commonly collected indicators such as body mass index (BMI), physical activity, diet, and existing health conditions. In addition to predictive performance, this project seeks to understand which risk factors contribute most strongly to diabetes risk.

---

## Research Question

**Can we accurately predict an individual’s diabetes risk using health and lifestyle indicators—such as BMI, physical activity, diet, and existing health conditions—through machine learning classification models?**

---

## Project Motivation

This project is motivated by both public health importance and personal experience. Diabetes has affected multiple generations within my family: my grandparents experienced diabetes-related complications, my parents have lived with diabetes for decades, and more recently, my older brother was diagnosed with prediabetes.

Witnessing the long-term health and lifestyle impacts of diabetes firsthand reinforced the importance of early risk identification—particularly at the prediabetes stage, where intervention can prevent or delay disease progression. This personal context directly informed the focus of this project on modifiable lifestyle factors and existing health conditions that are commonly available through public health surveys.

By applying machine learning to these indicators, this project aims to explore how effectively diabetes risk can be identified early and which factors may be most informative for prevention-focused screening strategies.

---

## Dataset Description

This project uses data from the **Behavioral Risk Factor Surveillance System (BRFSS) 2015**, a large-scale health-related telephone survey conducted annually by the Centers for Disease Control and Prevention (CDC). The BRFSS collects information on health behaviors, chronic conditions, and preventive service usage from U.S. adults.

The dataset used here was obtained from Kaggle and represents a cleaned and consolidated subset of the original BRFSS 2015 data.

- **Source:** Kaggle – *Diabetes Health Indicators Dataset*  
- **Year:** 2015  
- **Population:** U.S. adults  
- **Survey Type:** Self-reported health survey  

---

## Dataset Used

Only the following dataset file is used in this project:

**`diabetes_012_health_indicators_BRFSS2015.csv`**

- **Number of observations:** 253,680  
- **Number of features:** 21  
- **Target variable:** `Diabetes_012`  
- **Classification type:** Multiclass (3 classes)  
- **Class imbalance:** Present  

### Target Variable: Diabetes_012

- `0` = No diabetes (or diabetes only during pregnancy)  
- `1` = Prediabetes  
- `2` = Diabetes  

This structure enables multiclass classification to distinguish between individuals with no diabetes, prediabetes, and diabetes.

---

## Feature Selection Rationale

The selected features represent health behaviors, lifestyle choices, and medical conditions that are well-established in the clinical and public health literature as risk factors for type 2 diabetes. These variables were chosen specifically because they are:

- Commonly collected in public health surveys  
- Largely non-invasive and low-cost to obtain  
- Actionable through lifestyle or medical intervention  

Key feature groups include:

- **Anthropometric factors:** Body Mass Index (BMI)  
- **Lifestyle behaviors:** Physical activity, diet (fruit and vegetable consumption), smoking, alcohol use  
- **Existing health conditions:** High blood pressure, high cholesterol, heart disease, stroke  
- **Self-reported health status:** Physical and mental health indicators  
- **Demographic and socioeconomic factors:** Age, sex, education, income, healthcare access  

A full data dictionary describing each feature and its encoding is provided below.

---

## Data Dictionary

### Diabetes_012
Diabetes status  
- 0 = No diabetes  
- 1 = Prediabetes  
- 2 = Diabetes  

### HighBP
High blood pressure  
- 0 = No  
- 1 = Yes  

### HighChol
High cholesterol  
- 0 = No  
- 1 = Yes  

### CholCheck
Cholesterol checked in past 5 years  
- 0 = No  
- 1 = Yes  

### BMI
Body Mass Index (continuous)

### Smoker
Smoked at least 100 cigarettes in lifetime  
- 0 = No  
- 1 = Yes  

### Stroke
History of stroke  
- 0 = No  
- 1 = Yes  

### HeartDiseaseorAttack
History of coronary heart disease or heart attack  
- 0 = No  
- 1 = Yes  

### PhysActivity
Physical activity in past 30 days (excluding work)  
- 0 = No  
- 1 = Yes  

### Fruits
Consumes fruit daily  
- 0 = No  
- 1 = Yes  

### Veggies
Consumes vegetables daily  
- 0 = No  
- 1 = Yes  

### HvyAlcoholConsump
Heavy alcohol consumption  
- 0 = No  
- 1 = Yes  

### AnyHealthcare
Has health care coverage  
- 0 = No  
- 1 = Yes  

### NoDocbcCost
Unable to see a doctor due to cost (past 12 months)  
- 0 = No  
- 1 = Yes  

### GenHlth
Self-reported general health  
- 1 = Excellent  
- 5 = Poor  

### MentHlth
Days mental health not good (0–30)

### PhysHlth
Days physical health not good (0–30)

### DiffWalk
Difficulty walking or climbing stairs  
- 0 = No  
- 1 = Yes  

### Sex
Sex  
- 0 = Female  
- 1 = Male  

### Age
Age group category  
- 1 = 18–24 years  
- 13 = 80 years or older  

### Education
Highest level of education completed  
- 1 = Lowest  
- 6 = College graduate  

### Income
Household income category  
- 1 = Less than $10,000  
- 8 = $75,000 or more  

---

## Modeling Approach

This project treats diabetes risk prediction as a **multiclass classification problem**. Multiple machine learning models are evaluated to compare performance and interpretability. Special attention is given to class imbalance, particularly for the prediabetes class, which represents an important target for early intervention.

Model performance is evaluated using appropriate classification metrics beyond accuracy, including precision, recall, and F1-score.

---

## Ethical Considerations and Limitations

This dataset is based on self-reported survey data and may be subject to recall bias and reporting inaccuracies. Additionally, predictive models developed in this project are not intended to replace clinical diagnosis, but rather to explore population-level risk patterns and potential screening approaches.

Care is taken to interpret results responsibly, particularly given the sensitive nature of health-related predictions.

---

## References

- Centers for Disease Control and Prevention (CDC). Behavioral Risk Factor Surveillance System (BRFSS).  
- Kaggle: Diabetes Health Indicators Dataset  
- Xie, Z. et al. *Building Risk Prediction Models for Type 2 Diabetes Using Machine Learning Techniques*