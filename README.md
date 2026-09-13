# Employee Attrition & Workforce Analytics Dashboard

An interactive **Power BI dashboard** built to analyze employee attrition and workforce patterns across departments, job roles, age groups, and overtime status.

## 📊 Dashboard Overview

The dashboard provides a high-level view of workforce composition and employee attrition using interactive KPIs, charts, and slicers.

### Key KPIs

- **Total Employees:** 1,470
- **Active Employees:** 1,233
- **Attrition Employees:** 237
- **Attrition Rate:** 16.12%

### Visualizations

- Employee Attrition by Job Role
- Employee Attrition by Department
- Employee Attrition by Age Group
- Employee Attrition by Overtime
- Interactive filters for:
  - Department
  - Job Role
  - Overtime

## 🛠️ Tools & Technologies

- **Power BI Desktop**
- **DAX**
- Data Visualization
- Data Analysis
- Interactive Slicers
- Calculated Columns & Measures

## 📐 DAX Measures

The dashboard uses DAX measures to calculate key workforce metrics.

```DAX
TotalEmployees =
COUNTROWS(HR_Employee_Data)
```

```DAX
ActiveEmployees =
CALCULATE(
    [TotalEmployees],
    HR_Employee_Data[Attrition] = "No"
)
```

```DAX
AttritionEmployees =
CALCULATE(
    [TotalEmployees],
    HR_Employee_Data[Attrition] = "Yes"
)
```

```DAX
AttritionRate =
DIVIDE(
    [AttritionEmployees],
    [TotalEmployees],
    0
)
```

## 📌 Age Grouping

Employees are grouped into the following age categories:

- Under 25
- 25–34
- 35–44
- 45–54
- 55+

A separate sort column is used to display the age groups in the correct chronological order.

## 📂 Dataset

The dashboard uses the **IBM HR Analytics Employee Attrition & Performance** dataset.

The dataset contains employee-level HR information such as:

- Attrition
- Department
- Job Role
- Age
- Monthly Income
- Job Satisfaction
- Overtime
- and other workforce attributes

Dataset source: [Kaggle – IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-Dataset)

## 🖼️ Dashboard Preview

Add your dashboard screenshot here:

```text
![Employee Attrition & Workforce Analytics Dashboard](dashboard.png)
```

Place the screenshot file in the root of this repository and name it:

`dashboard.png`

## 🎯 Project Objectives

- Analyze employee attrition patterns
- Compare attrition across departments and job roles
- Examine workforce distribution by age group
- Understand the relationship between overtime and attrition
- Build an interactive dashboard for HR workforce analysis
- Demonstrate practical Power BI and DAX skills

## 📈 Key Insights

The dashboard can be used to explore:

- Which departments have higher employee attrition
- Which job roles experience greater attrition
- How attrition varies across age groups
- How overtime status relates to employee attrition
- Workforce composition across different organizational segments

## 📁 Repository Contents

```text
Employee-Attrition-Workforce-Analytics/
│
├── README.md
├── dashboard.png
└── Employee Attrition & Workforce Analytics.pbix
```

> **Note:** The `.pbix` file may require Power BI Desktop to open.

## 👩‍💻 Author

**Anusha Palaparthi**

- GitHub: [Anusha-2005](https://github.com/Anusha-2005)
