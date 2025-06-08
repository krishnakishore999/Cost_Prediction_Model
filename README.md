# Steel Production Cost Prediction Model
This project estimates the **cost of producing steel per ton (in USD)** by analyzing the relationship between raw material usage and total production cost. The primary objective is to predict the **conversion cost**, which is not directly dependent on raw material inputs but inferred using machine learning.

**I have built this project using realtime data from ERP Systems as a part of my job at Jindal. Hence the dataset is not shared.**
---

## 📌 Project Description

Steel production cost is traditionally split into two major components:

- **Raw Material Cost**: Directly proportional to the quantity and price of materials such as scrap, DRI, HBI, Pig Iron, etc.
- **Conversion Cost**: Includes energy consumption, flux required, water consumption, NG consumption, etc. This part is **not directly observable** from raw material inputs and is the main target of this predictive model.

This model aims to accurately estimate the **conversion cost** using historical data of steel heats and raw material consumption.

---

### Columns

 1   Grade
 2   Ext. Scrap (Ton)                      
 3   Rate of ext scrap ($/Ton)             
 4   DRI TOTAL (T)                         
 5   Rate of DRI ($/Ton)                   
 6   HBI TOTAL (T)                         
 7   Rate of HBI ($/Ton)                   
 8   T/d skull / Slag Metallics TOTAL (T)  
 9   Rate of Skull ($/Ton)                 
 10  Pig Iron TOTAL (T)                    
 11  Rate of Pig Iron ($/Ton)              
 12  Int scrap (T)                         
 13  Rate of Int. Scrap ($/Ton)             
 14  Yeild(charge to billet)               
 15  RM Cost                               
 16  Conv Cost                             
 17  Total Cost 

---

## ⚙️ Modeling Process

1. **Data Loading and Cleaning**  
   - Loaded Excel data
   - Handled missing or inconsistent entries

2. **Exploratory Data Analysis (EDA)**
   - Descriptive stats 
   - Plotted distributions with **skewness** and **kurtosis**
   - Identified heavily skewed and heavy-tailed variables
   - Performed correlation analysis

4. **Feature Engineering**  
   - Derived (Material x Cost) columns to capture the effect of cost and material.
   - Transformation of variables.

5. **Modeling**  
   - Trained multiple regression models (Linear Regression, Polynomial Reg, XGBoost)

---

## 📈 Results

The final model (XgBoost) performance on the test set:

- **R-squared (R2)**: 0.88

> These results show a strong predictive power, helping optimize operational decisions and control conversion cost more effectively.

---
