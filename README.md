---

## 🚀 Project Overview

**Columbia Asia Hospitals Analysis** is a comprehensive healthcare data analytics project aimed at delivering actionable insights for hospital management. Using Power BI, this project evaluates patient demographics, satisfaction, departmental performance, and helps strategize for better revenue, staffing, and patient service.

---

## 📝 Objectives

* 📈 Assess the hospital's **revenue generation**
* 🏥 Recommend **departments for new hires**
* 💸 Suggest **patient discount strategies**
* 📊 Uncover patient satisfaction and operational trends

---

## 🛠️ Tools & Technologies

* **Power BI** (for dashboards and data modeling)
* **Power Query & DAX** (for cleaning, transformation, and analytics)
* Excel (data preparation)

---

## 🗂️ Data Overview

The dataset includes:

* **Patient Information:** Age, Gender, Race, Satisfaction Scores
* **Visit Details:** Department referrals, Doctor consulted, Appointment fees
* **Operational Metrics:** Wait times, Revenue, Visit dates

---

## 🧹 Data Cleaning & Transformation

* 🧩 **Handled missing values** (especially satisfaction scores, \~75% nulls retained for integrity)
* 🔄 **Converted date columns** to proper format for time-based analytics
* 👶🧑👵 **Created Age Brackets:** Grouped patient ages into 5 demographic bins with DAX
* 🔗 **Built data model:** Established relationships for robust, multi-perspective analysis

---

## 📊 Key Insights & Dashboards

!\[Main Dashboard]\(main tab.PNG)
!\[Doctor's Tab]\(Doctor's tab.PNG)
!\[Patient's Tab]\(Patient's tab.PNG)

### 🕒 **Average Patient Wait Time**

* **35.26 minutes** (calculated using DAX: `AVERAGE('Hospital ER'[patient_waittime])`)
* *No significant outliers across departments!*

---

### 🏥 **Departmental Visits**

* **General Practice** is the most visited (\~78% of total visits)
* *Helps in identifying priority departments for resource allocation and hiring*

---

### 📈 **Age Group Segmentation**

* Patients grouped into: **0-15**, **15-25**, **25-40**, **40-60**, **60+**
* *Aids in understanding which age groups require more attention/services*

---

### 🧑‍🤝‍🧑 **Patient Demographics**

* **Gender Split:** Male (51.05%), Female (48.7%), Unspecified (24)
* **Race:** Visualized and analyzed for service parity and satisfaction

---

### 💰 **Revenue Insights**

* **Orthopedics** generated the highest revenue (170M)
* **Renal** generated the least (4.75M)

---

### 💸 **Discount Recommendations**

* Target **Pacific Islander**, **Alaska region** patients and **Seniors (60+)** for 25% discounts—encouraging increased healthcare engagement

---

### 👨‍⚕️ **Hiring Suggestions**

* **Renal Department** has the least doctors and revenue—suggest new hires here
* **General Practice** can benefit from a **2-shift policy** to meet demand

---

### 💬 **Satisfaction Scores & Trends**

* **No evidence of gender/racial discrimination**: Satisfaction rates are equal across all groups
* *Highest satisfaction:* Age 15-25
* *Lowest satisfaction:* Age 60+

---

## 🔎 Example DAX Queries

```DAX
-- Age Bracket Creation
Age Bracket = SWITCH(
    TRUE(),
    'Hospital ER'[patient_age] < 15, "0-15",
    'Hospital ER'[patient_age] < 25, "15-25",
    'Hospital ER'[patient_age] < 40, "25-40",
    'Hospital ER'[patient_age] < 60, "40-60",
    'Hospital ER'[patient_age] >= 60, "60+"
)
```

```DAX
-- Average Wait Time
Average Wait time (in mins) = AVERAGE('Hospital ER'[patient_waittime])
```

---

## 🏅 Notable Features

* **Multi-tab Power BI dashboard** (Patients, Doctors, Revenue, Visits, Satisfaction)
* **Interactive visualizations:** Bar, Line, Pie, Scatter, TreeMap, and more
* **Comprehensive documentation:** Approach, methodology, and DAX code samples


---

## 📎 Project Files

* **Power BI Dashboard:** `Dashboard.pbix`
* **Presentation:** `COLUMBIA ASIA HOSPITALS ANALYSIS.pptx`
* **Project Report:** `Power BI Project Report.docx`
* **Dashboard Images:** *(see images above)*
---

## 🌟 Key Takeaways

* Clean and model healthcare data for end-to-end analytics
* Drive decisions on **hiring**, **discounts**, and **operational improvements**
* Present insights visually to support business stakeholders

---

