# SF-Salaries
**SF Salaries Analysis** — Python &amp; Power BI project analyzing 148K+ San Francisco city employee salary records (2011–2014), uncovering a base pay reversal in 2014 and structural overtime concentration in the Transportation sector.


# SF Salaries Analysis
 
## Overview
An end-to-end data analysis project examining San Francisco city employee salaries from 2011 to 2014 (148,654 records, 13 columns), covering data cleaning, exploratory analysis, and dashboard visualization to surface trends and cost drivers in the city's payroll.
 
## Business Problem
The city needed visibility into how payroll costs were evolving year over year, and whether certain job categories were creating disproportionate overtime costs that could signal staffing or budget issues.
 
## Data Cleaning
- Removed two non-informative columns: `Notes` (entirely empty) and `Agency` (constant value across all rows).
- Replaced invalid `"Not Provided"` text values with `0.0` across `Base Pay`, `Overtime Pay`, `Other Pay`, and `Benefits`, then converted these columns from Object to Float for numerical analysis.
- Filled missing `Benefits` values with `0.0`, after identifying that benefits data was only recorded starting in 2012 (0% availability in 2011 vs. 100% from 2012–2014) — a finding that directly shaped how later year-over-year comparisons were interpreted.
- Removed records with null or zero `Total Pay & Benefits`, as these did not represent valid salary data.
- Standardized `Job Title` casing and removed resulting duplicate records.
## Key Insights
- **Base Pay grew steadily from 2011 to 2013** (year-over-year growth rising from 2.89% to 6.41%), then **reversed sharply in 2014 with a 4.40% decline** — despite a continued increase in headcount, suggesting new hires skewed toward lower-paid, entry-level roles.
- **Overtime Pay totaled ~$752.8M against ~$9.8B in Base Pay** across the four years, or **~7.67% of total Base Pay citywide** — but this average masked heavy concentration in specific job categories.
- **The Transportation sector was the leading driver of overtime costs**, with roles such as Switch Repairer, Electrical Transit System Mechanic, Transit Power Line Worker, Train Controller, and Transit Supervisor repeatedly appearing among the highest overtime-to-base-pay ratios — a pattern consistent with structural staffing shortages rather than isolated cases.
## Tools Used
- **Python (Pandas, NumPy, Matplotlib):** Data cleaning and exploratory analysis in Jupyter Notebook
- **Excel:** Parallel analysis pass for cross-validation
- **Power BI:** Interactive dashboard for salary trends and overtime breakdown
## Workflow
Followed a 4-stage methodology — **Define → Clean → Analyze → Decide**. Data understanding and cleaning were performed in Jupyter Notebook, followed by time-series analysis of pay trends and a dedicated overtime analysis (citywide overtime ratio, top jobs by overtime, and overtime-to-base-pay ratio by role). Findings were then visualized in a Power BI dashboard to support the final recommendations.
 
## Recommendations
- Review 2014 hiring strategy and experience levels of new employees, given the base pay decline despite rising headcount.
- Exclude 2011 from any Benefits-related comparisons, since benefits data was not recorded that year.
- Investigate structural staffing shortages in the Transportation sector, where overtime costs are heavily concentrated.
- Run a cost-benefit analysis comparing the cost of hiring additional full-time staff against sustained overtime costs in high-overtime roles.
- Address the operational risk of burnout and error rates tied to consistently high overtime hours.
## Demo
Watch the full project presentation on LinkedIn: [https://www.linkedin.com/posts/hozaifa-alzohare_dataanalysis-python-pandas-ugcPost-7491839559245152257-Ftrf/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAD0S7hMB18CJGuqXP0XkHByzUPj7CuoJdTM]
