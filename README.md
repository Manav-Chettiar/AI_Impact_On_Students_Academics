# AI Impact on Students - Power BI Dashboard

## Overview

This project explores how Generative AI (GenAI) usage affects student academic performance, burnout, and study habits. Built as a two-page interactive Power BI dashboard with a cover page, KPI cards, and a range of visuals.

**The core question the dashboard answers:**
Does higher AI usage improve or hurt student academic performance - and at what cost to wellbeing?

**Dataset:** AI Impact on Students by laveshjadon on Kaggle.

**Link:** https://www.kaggle.com/datasets/laveshjadon/ai-impact-on-students

**Note:** A synthetic dataset was used to practice full BI workflow (modeling, DAX, dashboarding) without real-world privacy or data-access constraints.

## Data adaptations made

To localize the dataset and correct a few logical inconsistencies in the raw data, the following transformations were applied in Power Query / DAX before building visuals:

1. GPA - CGPA conversion: Pre_Semester_GPA and Post_Semester_GPA (originally on a US 4.0 scale) were linearly rescaled (× 2.5) to a 10-point Indian CGPA scale, and renamed Starting_CGPA and Current_CGPA.
2. Academic year relabeling: Freshman → First Year, Sophomore → Second Year, Junior → Third Year, Senior → 4th Year (Graduate left unchanged), to match Indian academic year naming conventions.
3. Starting CGPA interpretation: For First Year students, Starting_CGPA is interpreted as their pre-college (Class 12 / high school) CGPA rather than a prior college semester, since no prior semester exists for incoming students.

## Key Insights

1. 87.5% of students improved their CGPA after AI usage; only 12.4% declined.
2. CGPA gains stay flat (~0.4–0.6) across usage levels, but exam anxiety rises steadily (3.8 → 5.6) — performance gains come with a wellbeing cost.
3. STEM shows the highest usage and strongest gains; Humanities the lowest on both.
4. Debugging/Troubleshooting with Advanced skill shows the strongest performance link (0.93 avg CGPA change).
5. Stricter AI policies correlate with slightly lower performance gains.

## Dashboard Structure

**Page 1 - Cover Title, project name, author name, background visual, and a navigation button into the dashboard.**

**Page 2 - Performance Insights**

1. 6 KPI cards: Total Students, Avg CGPA Change, Avg Weekly Hours, % High Burnout, Avg Skill Retention, Avg Anxiety Level
2. Bar chart: CGPA change by institutional AI policy
3. Combo chart: CGPA change vs. exam anxiety, by usage level
4. Scatter chart: AI usage vs. CGPA change, by major of the Students

**Page 3 - Usage Patterns**

1. Stacked column chart: CGPA change by major, by burnout risk
2. Donut chart: Burnout risk distribution
3. Pie chart: CGPA outcome distribution (Improved / Declined / No Change)
4. Stacked bar chart: CGPA change by primary AI use case, by prompt skill
5. Summary table: Performance metrics by major

## Tools Used

1. **Power BI Desktop** - data modeling, Power Query transformations, DAX measures, and report/visual design
2. **Power Query** - data cleaning, GPA-to-CGPA conversion, academic year relabeling, and binning
3. **DAX** - calculated columns and measures for CGPA change, outcome classification, usage bins, and aggregate KPIs

## Screenshots

<img width="1276" height="715" alt="page1_cover" src="https://github.com/user-attachments/assets/f7c46a5e-05ca-4abe-941d-5106ef7e6925" />

<img width="1268" height="718" alt="page2_performance" src="https://github.com/user-attachments/assets/a3b71eed-cd57-4019-8b7d-94fbd646d0e3" />

<img width="1270" height="718" alt="page3_usage" src="https://github.com/user-attachments/assets/db72e1f5-12b4-4800-aa91-397abeaeda67" />
