# BingePlay Streaming Analytics 🎬📊

## Project Overview
This project simulates the role of the first Data Analyst at **BingePlay**, a fictional Indian OTT streaming service. Using a production-style relational database containing data on users, subscriptions, shows, watch sessions, and ratings, I solved 12 real-world business questions. 

The questions ranged from foundational revenue reporting to advanced product intelligence, including user retention, content performance, and early churn detection.

## 🛠️ Tools & Technologies Used
*   **Database:** MySQL
*   **Programming:** Python
*   **Libraries:** SQLAlchemy, PyMySQL, Pandas
*   **Environment:** Jupyter Notebook

## 🧠 Key SQL Skills Demonstrated
*   **Advanced Querying:** Window Functions (e.g., `ROW_NUMBER()`, `LAG()`), Common Table Expressions (CTEs).
*   **Problem Solving:** The "Gaps-and-Islands" problem (finding consecutive week streaks).
*   **Data Quality Handling:** Navigating the classic `NOT IN` vs. `NULL` trap, self-joins, and anti-existence checks (`NOT EXISTS`).
*   **Data Aggregation:** Multi-level grouping, date/time extraction, and conditional aggregation (`CASE WHEN`).

## 📈 Business Questions Solved

### Tier 1: Foundations
*   Calculated total **Active Monthly Recurring Revenue (MRR)** as of mid-2024.
*   Analyzed **Signup Momentum** month-over-month to identify peak acquisition periods.
*   Evaluated **Device Analytics** (sessions, watch time, completion rates) while filtering out NULL user logs.
*   Assessed **Rating Distributions** to find the percentage of highly-rated (4-5 star) content.
*   Compared the average IMDb ratings of **BingePlay Originals vs. Acquired Content**.

### Tier 2: Joins & Subqueries
*   Detected **Binge Days** (identifying users watching the same show 5+ times in one day).
*   Identified Q1 signups who **never watched a single session** (using `LEFT JOIN` / `NOT EXISTS` to bypass the NULL trap).
*   Found **Over-paying Users** (Premium/Family users whose watch history consists *only* of Basic-tier content).
*   Tracked **Upgrade Success Cohorts** (users who upgraded from Basic to Premium/Family and remained active).
*   Analyzed **Cliffhanger Comebacks** (users returning to watch the same show within 1–7 days after an incomplete session).

### Tier 3: Advanced Analytics
*   Measured **Consecutive-Week Engagement** by finding users with 4+ week streaks using the Gaps-and-Islands technique.
*   Built a **Churn Signal Detection** model to flag users whose June watch time dropped by 50% or more compared to May.

## 📂 Repository Contents
*   `bingeplay_Srushti.ipynb` - The main Jupyter Notebook containing all SQL queries, Python execution, and business interpretations.
*   `bingeplay_setup.sql` - The SQL script used to generate the database and insert the mock data.

---
*Created as part of the Data Analytics & Data Science Track at The Unlox Academy.*
