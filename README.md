# 🏥 Columbia Asia Hospitals Analysis

## 🛠️ Tools & Technologies

* **Power BI** (for dashboards and data modeling)
* **Power Query & DAX** (for cleaning, transformation, and analytics)
* **Excel** (data preparation)

---

## 🗂️ Data Overview

The dataset includes:

* **Patient Information**: Age, Gender, Race, Satisfaction Scores
* **Visit Details**: Department referrals, Doctor consulted, Appointment fees
* **Operational Metrics**: Wait times, Revenue, Visit dates

---

## 🧹 Data Cleaning & Transformation

* 🧩 Handled missing values, especially satisfaction scores (\~75% nulls retained for integrity)
* 🔄 Converted date columns to proper format for time-based analytics
* 👶🧑👵 Created **Age Brackets**: Grouped patient ages into 5 demographic bins with DAX
* 🔗 Built a robust data model by establishing relationships for multi-perspective analysis

---

## 📊 Key Insights & Dashboards

![Main Dashboard](main_tab.PNG)
![Doctor's Dashboard](Doctors_tab.PNG)
![Patient's Dashboard](Patients_tab.PNG)

### 🕒 Average Patient Wait Time

* **35.26 minutes** (calculated using DAX: `AVERAGE('Hospital ER'[patient_waittime])`)
* No significant outliers across departments

### 🏥 Departmental Visits

* **General Practice**: Most visited (\~78% of total visits)
* Identified priority departments for resource allocation and hiring

### 📈 Age Group Segmentation

* Age groups: 0-15, 15-25, 25-40, 40-60, 60+
* Helps target services based on age-specific needs

### 🧑‍🤝‍🧑 Patient Demographics

* **Gender Split**: Male (51.05%), Female (48.7%), Unspecified (24 cases)
* **Race**: Analyzed for service parity and satisfaction

### 💰 Revenue Insights

* Highest revenue: **Orthopedics** (170M)
* Lowest revenue: **Renal** (4.75M)

### 💸 Discount Recommendations

* Recommend targeting Pacific Islander, Alaska region patients, and Seniors (60+) with **25% discounts** to boost healthcare engagement

### 👨‍⚕️ Hiring Suggestions

* Renal Department: Suggest new hires to increase revenue
* General Practice: Implement a **2-shift policy** to meet demand

### 💬 Satisfaction Scores & Trends

* Satisfaction consistent across gender/race groups (no discrimination observed)
* Highest satisfaction: Age group 15-25
* Lowest satisfaction: Age group 60+

---

## 🔎 Example DAX Queries

**Age Bracket Creation:**

```DAX
Age Bracket = SWITCH(
    TRUE(),
    'Hospital ER'[patient_age] < 15, "0-15",
    'Hospital ER'[patient_age] < 25, "15-25",
    'Hospital ER'[patient_age] < 40, "25-40",
    'Hospital ER'[patient_age] < 60, "40-60",
    'Hospital ER'[patient_age] >= 60, "60+"
)
```

**Average Wait Time:**

```DAX
Average Wait Time (in mins) = AVERAGE('Hospital ER'[patient_waittime])
```

---

## 🏅 Notable Features

* Multi-tab **Power BI dashboard** (Patients, Doctors, Revenue, Visits, Satisfaction)
* Interactive visualizations (Bar, Line, Pie, Scatter, TreeMap)
* Comprehensive documentation covering approach, methodology, and DAX examples

---

## 📎 Project Files

* **Dashboard**: [Dashboard.pbix](Dashboard.pbix)
* **Presentation**: [COLUMBIA ASIA HOSPITALS ANALYSIS.pptx](COLUMBIA%20ASIA%20HOSPITALS%20ANALYSIS.pptx)
* **Project Report**: [Power BI Project Report.docx](Power%20BI%20Project%20Report.docx)
* **Dashboard Images**: See images above

---

## 🌟 Key Takeaways

* Cleaned and modeled healthcare data for comprehensive analytics
* Enabled data-driven decisions for hiring, discounts, and operational improvements
* Visualized insights effectively for clear stakeholder communication
