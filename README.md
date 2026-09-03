# 🏏 IPL Cricket Analysis — 2008–2024

<img width="1200" height="675" alt="IndiaTv5cce01_IPL" src="https://github.com/user-attachments/assets/5d74b7b1-335b-4e28-ac2b-913f7bbc4d84" />

## 📌 Project Overview

This project analyzes **IPL cricket data from 2008 to 2024** using SQL to uncover trends in team performance, player statistics, bowling efficiency, toss decisions, venue usage, and batting performance.

The analysis uses **match-level and ball-by-ball delivery data** to answer practical analytical questions and transform raw cricket data into meaningful insights.

### 🎯 Objectives

* Identify the most successful IPL teams
* Analyze the impact of toss decisions on match outcomes
* Identify top batsmen and bowlers
* Compare bowling efficiency using economy rates
* Analyze venue usage across IPL seasons
* Identify high-scoring innings
* Examine season-wise scoring trends
* Use SQL to generate data-driven sports insights

---

## 🛠️ Skills & SQL Techniques

* **SQL**
* Joins
* Aggregations
* `GROUP BY`
* `HAVING`
* `CASE` statements
* Common Table Expressions (**CTEs**)
* Subqueries
* Window Functions
* `COUNT()`, `SUM()`, `AVG()`
* Ranking and filtering
* Data cleaning and standardization
* Analytical storytelling

---

## 📂 Dataset

**Source:** Kaggle — IPL Complete Dataset

[IPL Complete Dataset](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020/data)

The analysis uses match-level and ball-by-ball delivery data to perform both player-level and team-level analysis.

---

# 🔍 Analysis & Key Insights

## 1️⃣ Most Successful Teams by Total Wins

Historical team names were standardized before calculating total wins. For example:

* `Kings XI Punjab` → `Punjab Kings`
* `Delhi Daredevils` → `Delhi Capitals`
* `Royal Challengers Bangalore` → `Royal Challengers Bengaluru`

### 📊 Results
<img width="238" height="285" alt="Screenshot 2026-09-03 at 7 05 27 PM" src="https://github.com/user-attachments/assets/55ab925e-89a4-4b20-a822-10eeb1fbd9b3" />


### 💡 Insight

**Mumbai Indians** and **Chennai Super Kings** have the highest number of franchise-level wins in the analyzed dataset.

---

## 2️⃣ Does Winning the Toss Help Win the Match?

This analysis compares the team that won the toss with the team that won the match.

### 📊 Results
<img width="448" height="65" alt="Screenshot 2026-09-03 at 7 06 30 PM" src="https://github.com/user-attachments/assets/a396cd9c-71bd-4780-9885-ff52f1dec55b" />

### 💡 Insight

Teams that won the toss also won the match in approximately **51% of matches**.

Since the result is close to 50%, winning the toss alone does **not appear to be a strong predictor of match success**. Team strength, player performance, venue conditions, and match strategy are likely to have a greater influence.

> **Conclusion:** Winning the toss provides only a slight observed advantage in the analyzed dataset.
---

## 3️⃣ Field First or Bat First — Which Wins More?

This analysis examines whether the toss decision is associated with a higher match win rate.

### 📊 Results
<img width="363" height="87" alt="Screenshot 2026-09-03 at 7 07 41 PM" src="https://github.com/user-attachments/assets/f2538489-ebc0-4bc5-9b00-6c0ad2d39274" />

### 💡 Insight

Teams chose to **field first** considerably more often than they chose to bat first.

Field-first decisions had a **54.05% win rate**, compared with **45.31%** for bat-first decisions — a difference of **8.74 percentage points**.

This indicates an association between fielding first and a higher observed win rate, although it does not establish causation.

---

## 4️⃣ Top 10 Run Scorers of All Time

Using ball-by-ball delivery data, batsmen were ranked based on their **total IPL runs**.

### 📊 Results
<img width="358" height="201" alt="Screenshot 2026-09-03 at 7 08 45 PM" src="https://github.com/user-attachments/assets/1a67f63b-7bf2-410c-8dcf-67f26d7039ff" />

### 💡 Insight

**Virat Kohli** leads the dataset with **8,014 runs**, while **AB de Villiers** has the highest runs-per-ball rate among the top 10.

---

## 5️⃣ Top 10 Wicket-Takers of All Time

The top IPL bowlers were identified based on **total wickets credited to the bowler**.

Run outs, retired hurt, and obstructing-the-field dismissals were excluded because they are not credited as bowler wickets.

### 📊 Results

<img width="328" height="199" alt="Screenshot 2026-09-03 at 7 09 46 PM" src="https://github.com/user-attachments/assets/f34aab4b-6d6d-477a-abec-d1bbb147f1a1" />


### 💡 Insight

**YS Chahal** leads the ranking with **205 wickets**, followed by **PP Chawla** with 192.

SL Malinga and JJ Bumrah stand out for their high wicket totals across relatively fewer matches, highlighting their strong wicket-taking impact.

---

## 6️⃣ Most Player of the Match Awards

Player of the Match awards were analyzed to identify players with the highest number of match-winning performances.

### 📊 Results

<img width="221" height="207" alt="Screenshot 2026-09-03 at 7 10 40 PM" src="https://github.com/user-attachments/assets/72e44cd3-996f-4c26-bed8-5c3c94ace1f5" />

### 💡 Insight

**AB de Villiers** leads the list with **24 Player of the Match awards**, followed by Chris Gayle with 22.

Unlike total runs or wickets, this metric captures **individual match impact**, including performances across batting, bowling, and all-round contributions.

---

## 7️⃣ Most Matches Hosted by Venue

Venue names were standardized to avoid duplicate entries caused by inconsistent naming.

For example:

`Wankhede Stadium` + `Wankhede Stadium, Mumbai` → **Wankhede Stadium**

### 📊 Results

<img width="437" height="194" alt="Screenshot 2026-09-03 at 7 11 39 PM" src="https://github.com/user-attachments/assets/53202f57-ea5a-48b1-864f-2c1fbbe90769" />


### 💡 Insight

**Wankhede Stadium** is the most frequently used venue in the dataset, having hosted **117 matches**.

The presence of Dubai and Abu Dhabi venues also highlights IPL seasons and matches hosted outside India.

---

## 8️⃣ Season-Wise Total Runs — Batting Trends

Season-level batting trends were analyzed by joining the `matches` and `deliveries` tables using `match_id`.

### 📊 Results

<img width="432" height="302" alt="Screenshot 2026-09-03 at 7 12 39 PM" src="https://github.com/user-attachments/assets/a9ae06bb-c7ee-42d0-bd46-7ac37d2f13f5" />

### 💡 Insight

**2024 recorded the highest total runs** with 25,971 runs.

Average runs per delivery increased from **1.33 in 2007/08 to 1.52 in 2024**, suggesting an increase in scoring intensity over the period.

Because total runs are influenced by the number of matches played, **runs per ball provides a more useful comparison of scoring intensity between seasons**.

---

## 9️⃣ Best Bowling Economy — Minimum 100 Overs

To identify consistently economical bowlers, only players who bowled at least **100 overs** were included.

Since one over contains six legal deliveries, the analysis uses a minimum of **600 deliveries**.

### 📊 Results

<img width="367" height="195" alt="Screenshot 2026-09-03 at 7 13 43 PM" src="https://github.com/user-attachments/assets/67b2f211-bfc2-4c56-a56f-b86cd401f230" />

### 💡 Insight

**Anil Kumble** has the lowest economy rate among qualifying bowlers at **6.65 runs per over**.

Sunil Narine and Ravichandran Ashwin demonstrate sustained efficiency across a large number of overs, while the minimum 100-over threshold prevents small-sample performances from dominating the ranking.

---

## 🔟 Highest Team Totals in a Single Innings

This analysis identifies the **highest team scores in a single IPL innings** using ball-by-ball delivery data.

The deliveries were grouped by `match_id`, `batting_team`, and `inning`, and the total runs were calculated using `SUM(runs_total)`.

### 📊 Results

<img width="337" height="194" alt="Screenshot 2026-09-03 at 7 14 40 PM" src="https://github.com/user-attachments/assets/1de897ff-7bee-40d2-a757-c14e457a36c6" />

### 💡 Insight

**Sunrisers Hyderabad** recorded the highest team total in the dataset with **287 runs** and appears three times among the top four highest-scoring innings.

The results also show multiple innings exceeding **260 runs**, highlighting the increasingly high-scoring nature of modern T20 cricket.

---

# 📈 Overall Project Insights

The analysis highlights several important trends across IPL history:

* 🏆 **Mumbai Indians** have the highest franchise-level win count in the analyzed dataset.
* 🪙 Winning the toss resulted in a match win approximately **51% of the time**.
* 🏏 Teams choosing to **field first** had a higher observed win rate than teams choosing to bat first.
* 👑 **Virat Kohli** leads the analyzed dataset in total runs.
* 🎯 **YS Chahal** leads the analyzed dataset in total wickets.
* ⭐ **AB de Villiers** has the most Player of the Match awards.
* 🏟️ **Wankhede Stadium** has hosted the most matches after venue-name standardization.
* 📈 IPL scoring intensity has increased over time, with **2024 recording the highest average runs per delivery**.
* 💥 **Sunrisers Hyderabad** recorded the highest single-innings total at **287 runs**.

---

## 🚀 Conclusion

This project demonstrates how **SQL can be used to transform granular sports data into meaningful analytical insights**.

By combining match-level and ball-by-ball data with joins, aggregations, CTEs, conditional logic, and analytical techniques, the project explores **team performance, player impact, bowling efficiency, venue trends, toss strategy, and scoring evolution across IPL history**.
