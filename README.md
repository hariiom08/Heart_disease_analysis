# ❤️ Heart Health Analysis Dashboard (Power BI)

This repository contains a **Heart Disease Analysis Dashboard** built in **Power BI**.  
The dashboard provides key insights about patient survival, risk factors, and the influence of medical conditions like **cancer, diabetes, and serum sodium levels** on heart health.  

The project aims to make heart health insights **simple, interactive, and easy-to-understand** for both medical professionals and general users.

---

## 📂 Folder Structure

📁 Heart-Health-Analysis  
│── Heart_Disease_Analysis_Report.pbix   # Power BI dashboard file  
│── Heart_Disease_Dataset.xlsx           # Dataset used for analysis  
│── heart image.png                      # Dashboard theme/logo  
│── README.md                            # Documentation file  
│── Screenshot 2025-09-16 200709.png     # Dashboard preview 1  
│── Screenshot 2025-09-16 200754.png     # Dashboard preview 2  
│── Screenshot 2025-09-16 200818.png     # Dashboard preview 3  

---

---

## 📊 Dashboard Overview

The dashboard provides:
- ✅ **Survival Rate (Alive %)**  
- ✅ **Average Age of Survivors**  
- ✅ **Total Alive Patients**  
- ✅ **Total Deaths**  
- 📊 **Survivors by Age Group**  
- 📊 **Survivors with Cancer**  
- 📊 **Survivors with and without Diabetes**  
- 📊 **Average Serum Sodium Levels**  
- 👩‍⚕️ **Gender-based Filtering (Male/Female)**  

---

## 🖼️ Dashboard Previews

![Dashboard Screenshot 1](Screenshot%202025-09-16%20200709.png)  
![Dashboard Screenshot 2](Screenshot%202025-09-16%20200754.png)  
![Dashboard Screenshot 3](Screenshot%202025-09-16%20200818.png)  

---

## 🗂️ Dataset

The dataset contains patient records with the following parameters:

- `Age`
- `Sex` (Male/Female)
- `Status` (Alive/Dead)
- `Diabetes` (Yes/No)
- `Cancer` (Yes/No)
- `Serum_Sodium` (numeric values)
- `Ejection_Fraction` (optional – heart pumping efficiency)

---

## 🧮 Key Metrics & DAX Measures

### KPIs
```DAX
Total Alive = CALCULATE(COUNTROWS(Heart), Heart[Status] = "Alive")

Total Death = CALCULATE(COUNTROWS(Heart), Heart[Status] = "Dead")

Survival Rate = DIVIDE([Total Alive], [Total Alive] + [Total Death], 0)

Avg Age Alive = AVERAGEX(FILTER(Heart, Heart[Status] = "Alive"), Heart[Age])


---

## 🎯 Insights

- **68% of patients are alive** → most survive, but 32% deaths still significant.  
- **51–60 years age group** has the highest survival count.  
- **Serum sodium levels** are stable (~136–138) across groups.  
- **Diabetes & Cancer** increase health risk, reducing survival chances.  
- **Older patients (71+)** show the lowest survival rate.  

---

## 🚀 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/hariiom08/heart-health-analysis.git

---

