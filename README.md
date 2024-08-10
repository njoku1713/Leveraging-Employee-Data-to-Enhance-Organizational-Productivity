# Leveraging-Employee-Data-to-Enhance-Organizational-Productivity

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendations)

### Project Overview
In today’s competitive business environment, optimizing employee management processes is crucial for enhancing overall productivity. This project aims to analyze key employee-related data to identify trends and develop strategies that can improve organizational outcomes. By examining hiring trends, training effectiveness, turnover rates, and employee engagement, this project will provide actionable insights to inform data-driven decisions that bolster the company’s productivity and employee satisfaction.

![image](https://github.com/user-attachments/assets/78325765-1607-4abe-81bc-3509074cff2a)

### Data Source
The data used in this project was sourced from Kaggle [Download here](https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset). The dataset consists of the following four distinct CSV files:
1. employee_data.csv: This dataset contains detailed information about employees, including demographics, job roles, and performance metrics.
2. employee_engagement_survey_data.csv: This dataset captures the results of employee engagement surveys conducted within the company. It provides insights into how employees feel about their work environment, job satisfaction, and overall engagement with the organization.
3. recruitment_data.csv: This dataset includes information related to the company’s recruitment process, covering various stages from application to hiring. It helps analyze the efficiency and effectiveness of recruitment strategies.
4. training_and_development_data.csv: This dataset tracks the training and development activities within the company, including internal and external training programs. It provides data on the allocation of training resources and the participation of employees in these programs.

### Tools
 - Excel - Data Cleaning, Analyses, and Creating reports [Download here](https://microsoft.com)

### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Handled missing values.
3. Data cleaning and formating.

### Exploratory Data Analysis (EDA)
EDA involved exploring the call data to answer questions such as:
- What is the impact of training hours on employee performance?
- How does the effectiveness of internal training compare to external training?
- What are the key factors contributing to employee turnover?
- How does employee engagement vary across different departments or job roles?
- Which demographic factors influence employee productivity the most?
- What strategies can be implemented to improve areas with lower productivity or higher turnover?

### Data Analysis
1. As is common in businesses and organizations, we evaluated how the company spent money on internal and external training. To do this, we used a SUMX function in Excel Power Query to calculate the total training cost, which allowed for a thorough analysis of training expenses.
```DAX Calculations
= SUM(training_and_development_data [Training Day]*[Training Cost per Day]
```
2. To gain a deeper understanding of the workforce dynamics, the Calculate function was employed to determine Employee Status by 'Employment Type' and the 'Gender Distribution across the Company’s Departments.
```
= CALCULATE(employee_data[Count of EmpID],employee_data[EmpStatAnalysis]="Active")
= CALCULATE(employee_data[Count of GenderCode],employee_data[GenderCode]="Male")

```

### Results/Findings
The analysis results are summarized as follows:
1. Balanced Training Investment: The company allocates its training resources almost equally between internal (50.31%) and external (49.69%) programs, reflecting a balanced approach to employee development.
2. Sales Dominates Workforce: A substantial portion of the workforce (67.33%) is concentrated in the Sales department, suggesting it is a key focus area for the organization.
3. Involuntary Turnover Concern: Involuntary terminations are the highest among all types of turnover, potentially signaling issues related to performance management or organizational changes.
4. Recruitment Funnel Insights: The recruitment process shows a high number of offers being made, but also a significant number of rejections, indicating a potentially rigorous selection process or a mismatch between applicants and job requirements.

### Recommendations
Based on the analysis, we recommend the following actions:
1. Tailor and Enhance Training Programs: Assess the effectiveness of current training programs and tailor them to meet specific departmental needs, particularly focusing on areas like Sales and Production to maximize their impact on performance.
2. Improve Retention Strategies: Strengthen retention by enhancing performance management, providing clear career progression, and aligning roles with employees' skills and aspirations to reduce involuntary turnover.
3. Refine the Recruitment Process: Optimize the recruitment funnel by refining job descriptions, improving selection criteria, and ensuring a better match between candidates and job roles to reduce rejection rates and improve hiring efficiency.
4. Promote Workforce Diversity: Use gender distribution insights to develop diversity and inclusion initiatives, ensuring equal opportunities across departments, which can lead to improved employee engagement and retention.
