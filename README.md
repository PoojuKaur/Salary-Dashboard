# 📊 Excel Salary Dashboard (Data Jobs Project)

## 📌 Introduction

This project is an **Excel Salary Dashboard** that helps job seekers explore salaries in data-related jobs.

It allows users to:

* 💰 Compare salaries for different roles
* 📍 See how location affects pay
* 🛠️ Understand which skills are important

---

## 📂 Dashboard File

* 📄 `Salary_Dashboard.xlsx` → Main dashboard file, please download the raw file 
---

## 🛠️ Excel Skills Used

* 📉 Charts (Bar chart, Map chart)
* 🧮 Formulas and Functions
* ❎ Data Validation

---

## 📊 Dataset Information

The dataset contains real-world data science job data, including:

* 👨‍💼 Job titles
* 💰 Salaries
* 📍 Locations
* 🛠️ Skills

---

## 📊 Dashboard Features

### 📉 1. Salary by Job Title (Bar Chart)

* Shows median salary for different job roles
* Sorted from highest to lowest salary

💡 **Insight:**
Senior roles and engineers earn more than analyst roles

---

### 🗺️ 2. Salary by Country (Map Chart)

* Displays salaries across different countries
* Uses colors to show high and low salary regions

💡 **Insight:**
Some countries offer much higher salaries than others

---

## 🧮 Formulas Used

### 💰 Median Salary Formula

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

💡 **What it does:**

* Filters data based on:

  * Job title
  * Country
  * Job type
* Returns the **median salary**

---

### ⏰ Job Type Filter Formula

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

💡 **What it does:**

* Creates a clean list of job schedule types
* Removes incorrect or messy values

---

## ❎ Data Validation

* Dropdown filters for:

  * Job Title
  * Country
  * Job Type

💡 **Benefits:**

* Prevents wrong input
* Makes dashboard easy to use
* Improves user experience

---

## 📈 Key Insights

* Salary depends on **job role and experience**
* **Location matters a lot** for salary
* Technical roles usually pay more
* Dashboard helps compare different career options

---

## ✅ Conclusion

This dashboard helps users:

* Understand salary trends
* Compare different roles and locations
* Make better career decisions

---

## 🚀 Final Thoughts

This project improved my Excel skills and helped me learn how to:

* Build interactive dashboards
* Use formulas for real data analysis
* Present data clearly

---

## ⭐ Author

**Poojinder Kaur**
BSc Computer Science Student | Aspiring Data Analyst
