# 2026worldcup_prediction
Predicting the FIFA 2026 World Cup Qualification and Winner

## Project Overview
This project aims to predict which teams will qualify for the FIFA 2026 World Cup and determine the potential tournament winner by analyzing historical international football match data.

## Research Question
To what extent can historical performance, FIFA rankings, and squad market value predict the qualification and potential winner of the FIFA 2026 World Cup?


## Motivation  
Football has always been a passion of mine, and the FIFA World Cup has been one of my favorite sporting events since childhood. The excitement, unpredictability, and high-level competition make it a unique tournament where data-driven insights can help uncover hidden patterns and trends. As someone who aims to build a career at the intersection of **football and data science**, I wanted to use this project as an opportunity to gain hands-on experience in football analytics. By applying **data science techniques to real-world football data**, I hope to develop practical skills that will be useful in my future career.


## Methodology

This project follows a structured data science workflow consisting of four main phases:

### 1. Data Collection & Preprocessing  
The datasets will be sourced from multiple platforms and structured to ensure consistency in analysis.

- **Data Sources:**  
  - **Historical Match Results (1994-2024):** Collected from Kaggle and FIFA.com.  
  - **FIFA Rankings (1992-2024):** Extracted from FIFA’s official site.  
  - **2026 FIFA World Cup Qualification Groups:** Manually compiled from FIFA’s records.  
  - **Squad Market Values (2006-2026):** Gathered from Transfermarkt to assess financial strength.  

- **Preprocessing Steps:**  
  - **Handling Missing Data:** Imputing missing values where necessary and removing inconsistencies.  
  - **Feature Normalization:** Scaling numerical values such as FIFA rankings and squad market values for uniformity.  
  - **Filtering Match Data:** Only including **official FIFA-sanctioned** matches (World Cup, qualifiers, and major tournaments).  

---

### 2. Exploratory Data Analysis (EDA)  
This phase focuses on uncovering trends and insights in international football performance.

- **Historical Trends Analysis:**  
  - Examining past **World Cup performance trends** across teams.  
  - Analyzing changes in **FIFA rankings over time**.  

- **Key Performance Indicators:**  
  - Identifying **win rates, goal differences, and home advantage** effects.  
  - Evaluating how **market value correlates with team performance**.  

- **Data Visualization Techniques:**  
  - Heatmaps for correlation analysis.  
  - Time-series plots for performance evolution.  
  - Bar charts comparing successful vs. underperforming teams.  

---

### 3. Statistical Analysis & Machine Learning  
This phase applies advanced techniques to predict **qualification and tournament success**.

- **Statistical Analysis:**
  
  - Identifying **key performance factors** that influence match outcomes.  
  - Examining **historical trends** to detect patterns in team success.  
  - Identifying statistically significant relationships between **FIFA rankings, squad strength, and World Cup performance**.  

- **Machine Learning Models:**  
  - Predicting **2026 World Cup qualification probabilities**.  
  - Identifying **potential winners** using past tournament performance and squad strength.  
  - Comparing predictions with historical outcomes to evaluate model effectiveness.  

---

### 4. Results & Interpretation  
The final phase interprets the findings and presents them through **data-driven insights**.

- **Probability Rankings:**  
  - Assigning qualification likelihoods to each team.  
  - Identifying high-probability contenders and potential underdogs.  

- **Tournament Winner Predictions:**  
  - Highlighting teams most likely to reach the knockout rounds and finals.  

- **Final Presentation:**  
  - Visualizing results through **tables, rankings, and charts**.  
  - Comparing **actual vs. predicted performance** for validation.  



## How the Data Will Be Used

Each dataset will be processed and analyzed through different statistical and machine learning techniques to predict World Cup qualification and the tournament winner. Below are the key steps for data utilization:

### 1. Match Results (1994-2024)
   - **Data Preprocessing:**  
     - Filtering only official FIFA-sanctioned matches (World Cup, Qualifiers, and Continental Tournaments).  
     - Standardizing team names for consistency.  
   - **Analysis Approach:**  
     - Calculating **win percentages, average goals per game, and home/away performance**.  
     - Examining trends in **goal differentials** and their impact on success.  
     - Checking correlations between **previous match results and later tournament performance**.  

### 2. Goals Scored & Team Performance
   - **Data Preprocessing:**  
     - Merging goal statistics with match results.  
     - Handling missing data by interpolating values where necessary.  
   - **Analysis Approach:**  
     - Computing **goal averages per team per tournament**.  
     - Measuring the consistency of teams in **scoring goals across different World Cups**.  
     - Identifying **offensive vs. defensive team profiles** (e.g., high-scoring vs. defensive teams).  

### 3. FIFA Rankings (1992-2024)
   - **Data Preprocessing:**  
     - Mapping **historical FIFA rankings** to match results.  
     - Normalizing ranking scores to compare across different years.  
   - **Analysis Approach:**  
     - Checking whether higher-ranked teams perform better in tournaments.  
     - Applying **regression models** to measure the relationship between ranking changes and performance.  

### 4. Squad Market Value (2006-2026)
   - **Data Preprocessing:**  
     - Extracting **team-level total market value** from Transfermarkt.  
     - Normalizing values to adjust for market inflation.  
   - **Analysis Approach:**  
     - Checking whether **higher market value correlates with tournament success**.  
     - Clustering teams based on **financial strength vs. actual performance**.  

### 5. 2026 FIFA World Cup Qualification Groups
   - **Data Preprocessing:**  
     - Extracting qualification results from official FIFA sources.  
     - Merging with previous World Cup performance data.  
   - **Analysis Approach:**  
     - Using **classification models** to predict whether a team will qualify.  
     - Comparing **historical qualification patterns** with current standings.  
     - Evaluating which **teams are over/underperforming** relative to past tournaments.  


## Data Collection Plan  

The datasets will be sourced from **Kaggle, FIFA and Transfermarkt**. The key steps are:  

- **Historical match results (1872-2024)** and **FIFA rankings (1992-2024)** will be downloaded from Kaggle and FIFA.com.  
- **2026 World Cup qualifier groups** will be manually compiled from FIFA.  
- **Goalscorers, team performance, and shootout data** will be obtained from Kaggle.  
- **Squad market values (2006-2026)** will be collected from Transfermarkt.  

 



  

