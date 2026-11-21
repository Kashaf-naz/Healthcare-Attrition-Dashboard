
# 📊 Healthcare Employee Attrition Dashboard (Power BI)

An end-to-end HR analytics project that looks at why employees leave a healthcare organisation and which groups HR should focus on first.

## Business Question

Why are employees leaving, and which groups should HR prioritise to reduce attrition?

## Key Findings

- Overall attrition is **11.87%** (199 leavers out of 1,676 employees).
- Overtime employees leave at **29.2%**, versus **5.0%** for non-overtime staff.
- Employees in their first 2 years leave at **44.68%**, and the rate falls steadily with tenure (16.82% at 3-5 years, 10.40% at 6-10, 6.16% at 11-15, 3.40% at 15+).
- Employees aged 18-24 leave at **41%**, and entry-level staff at **22.87%**.
- "Other" (16.29%) and Nurse (13.02%) are the job roles with the highest attrition.
- Cardiology (13.94%) and Maternity (12.31%) have the highest department rates; Neurology is lowest (7.74%).

## Recommendations

1. **Limit overtime:** cap overtime hours, share it fairly, review schedules.
2. **Support new joiners and early-career staff:** buddy program, 30-60-90 day check-ins, clear training and career path.
3. **Focus on Nurse and Other roles:** stay interviews with nurses; ask HR to break "Other" into specific roles.
4. **Keep tracking:** record exit-interview reasons and review attrition by tenure each month.

## Dashboard Pages

1. **Executive Overview:** headline KPIs, attrition by department, gender, job role, age band and shift, education field and job level.
2. **Workforce Demographics:** workforce make-up, leavers who worked overtime, and attrition by tenure band and income band.
3. **Department & Role Insights:** attrition counts, a department x job role heatmap, overtime share by job role, and satisfaction by department.
4. **Drill-through page:** employee-level detail, reached by right-clicking a department or job role.
5. **Rating scale reference:** explains the 1-4 satisfaction and performance scales.
6. **Recommendations:** actions linked to each finding.

![Executive Overview](images/Executive%20Overview.jpg)
![Workforce Demographics](images/Workforce%20Demographics.jpg)
![Department and Role Insights](images/Department%20%26%20role%20insights.jpg)
![Drill-through Details](images/Drill%20Through%20Details.jpg)
![Rating Scale Reference](images/Rating%20scale%20Bookmark.PNG)
![Recommendations](images/Recommendation%20page.jpg)

## Data Modeling

- The source data was a single flat file. I restructured it into a star schema: a fact table (`Fact_EmployeeAttrition`) and dimension tables (`Dim_Employee`, `Dim_Education`, `Dim_Satisfaction`) related through `EmployeeID`, plus a `Tenure Band Table` for tenure grouping.
- Created DAX measures such as `Total Employees`, `Attrition Count`, `Attrition Rate`, `Attrition % Overtime`, `Attrition % Non-Overtime`, `Average Age`, `Average Tenure Years`, `Average Monthly Income`, `Avg Job Satisfaction`, `Avg Environment Satisfaction`, `Avg Work Life Balance` and `Avg Performance Rating`.
- Created calculated columns for grouping, such as age band, tenure band and income band.

## Data Preparation

- Checked for duplicate records, null values and incorrect data types in Power Query. No duplicates or nulls were found.
- Standardised an inconsistent job role label ("Admin" and "Administrative") so the roles are counted correctly.

## Features

- Interactive slicers (gender, department, job role, job level, shift, overtime)
- Drill-through to employee-level detail
- Key Insights pop-up on the Executive Overview page
- Consistent theme and navigation across pages

## Limitations

- "Other" is a role category in the source data and is not broken down further.
- Some groups (for example the lowest income band) are small, so their rates should be treated as signals to investigate, not firm conclusions.
- Findings show associations in this dataset, not proven causes.

## Data Source

Kaggle dataset: [Employee Attrition for Healthcare](https://www.kaggle.com/datasets/jpmiller/employee-attrition-for-healthcare). Used for portfolio purposes. 
The dataset contains employee and company data for analytics and machine learning, with Attrition as the target variable. It was supplied as a single flat file, which I restructured into a star schema. Used for portfolio purposes.

## Tools

Power BI, Power Query, DAX, data modeling, bookmarks and drill-through.


## 👩‍💻 Author
**Kashaf Naz**  
- 📧 kashafnaz225@gmail.com 
- 💼 www.linkedin.com/in/kashaf-naz



⭐ *If you find this project useful, consider giving it a star on GitHub!*
