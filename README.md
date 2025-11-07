Employee Attrition Dashboard (Power BI)

## Overview
This Power BI project analyzes employee attrition data to uncover trends and insights that help HR teams understand and address workforce turnover. The dashboard provides a visual breakdown of attrition by key HR metrics such as job satisfaction, work-life balance, overtime, training, and years with manager.

---

## Key Insights
- **Attrition Drivers:** Identify factors that most contribute to employee attrition.  
- **Employee Engagement:** Examine how satisfaction and work-life balance impact retention.  
- **Performance Correlation:** Understand how ratings, training frequency, and management years relate to attrition.  
- **Departmental Comparison:** See which departments face the highest turnover rates.

---

## Tools & Technologies
- **Power BI Desktop** – Data visualization & dashboard creation    
- **DAX** – Calculated measures and KPIs  

---

## Dashboard Pages
1. **Overview Page:** KPIs and overall attrition summary  
2. **Attrition Analysis Page:**  
   - Attrition by Job Satisfaction  
   - Attrition by Work-Life Balance  
   - Overtime Donut Chart  
   - Attrition by Performance Rating  
   - Attrition by Training Times  
   - Attrition by Years with Manager  

---

## Features
- Interactive slicers and filters for dynamic exploration  
- KPI cards highlighting critical HR metrics  
- Clean, HR-analytics-friendly layout  

---

## How to Use
1. Download the `.pbix` file from this repository.  A copy of the original dataset (before cleaning) is also attached.
2. Open it in **Power BI Desktop**. Interact with it and discover insights.

---

## DAX Measures

| Measure | Formula | Purpose |
|----------|----------|----------|
| **Attrition Rate** | `Attrition Rate = DIVIDE(CALCULATE(COUNT(Employee[EmployeeID]), Employee[Attrition] = "Yes"), COUNT(Employee[EmployeeID]))` | Calculates overall employee attrition as a percentage of total employees. |
| **Average Satisfaction** | `Average Satisfaction = AVERAGE(Employee[JobSatisfaction])` | Evaluates general job satisfaction levels across the workforce. |
| **Average Training Times** | `Avg Training Times = AVERAGE(Employee[TrainingTimesLastYear])` | Helps visualize the link between training frequency and attrition. |
| **Years With Manager (Avg)** | `Avg Years With Manager = AVERAGE(Employee[YearsWithCurrManager])` | Shows how relationship duration with managers correlates with retention. |
| **Active Employees** | `Active Employees = CALCULATE(COUNT(Employee[EmployeeID]), Employee[Attrition] = "No")` | Tracks the current active workforce. |

_and a host of others, all included under a Measures table._

These measures were created to:
- Quantify attrition patterns and HR engagement indicators.  
- Enable drill-downs and comparisons across departments, satisfaction levels, and job roles.  
- Support KPI cards and visuals for executive decision-making.

---

## Preview
![PBI Overview](https://github.com/user-attachments/assets/10c3d65f-6521-4f06-8789-c1d5f53cd735)
