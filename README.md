## Project Overview

This project explores how national team success in the FIFA World Cup can be systematically measured and compared using historical performance data from 1930 to 2022. It aims to measure success using stage progression and compare long-term performance across confederations.

A stage-based scoring system is used to quantify how far teams advance in each tournament. Additionally, secondary indicators such as win rate and goal difference per game provide supporting context.

The analysis includes a specific comparison between UEFA and CONMEBOL, two of the most successful football confederations. Through exploratory data analysis and hypothesis testing, the project investigates whether one has historically outperformed the other in terms of World Cup success.

## **Research Question**

**Can national team success in the FIFA World Cup be systematically measured and compared using historical tournament data?**  
- Are UEFA teams statistically more successful than CONMEBOL teams in the World Cup?  
- Does FIFA Ranking correlate with tournament performance?


## Motivation  
Football has always been a personal passion, and the FIFA World Cup stands out as the most prestigious and exciting tournament in the sport. This project offers an opportunity to combine that enthusiasm with an academic interest in data science. By analyzing historical World Cup data, the goal is to gain deeper insights into how national team success can be quantified and compared over time. This work also reflects a broader interest in football analytics—a growing field where statistical reasoning and data-driven methods are increasingly shaping how the game is understood and strategized. The project serves as a practical step toward building a career at the intersection of football and data science, offering valuable experience in working with real-world sports data and applying exploratory analysis and hypothesis testing in a structured and meaningful way.
Methodology

## Methodology

### Data Collection & Preprocessing

The datasets were collected from multiple public sources and harmonized to create a clean master dataset.

**Data Sources:**
- Historical FIFA World Cup results (1930–2022)
- FIFA Rankings (1994–2024)
- Confederation membership data
- Country mapping files for standardization

**Preprocessing Steps:**
- Standardized country names using mapping dictionaries
- Assigned a stage score (1 to 6) to reflect how far a team advanced in each World Cup
- Created key variables per team:
  - `sum_stage_score_full`: Total stage score across all tournaments
  - `win_rate`: Win ratio across all matches
  - `gd_per_game`: Goal difference per game
- Calculated `avg_rank` for each team using FIFA Rankings (only from 1994 onward)
- Filtered out teams with fewer than 2 tournament appearances

---

## Statistical Analysis

The third stage of the project focuses on examining long-term patterns in World Cup performance using statistical methods. The goal is to evaluate whether measurable indicators of success—such as **stage progression**, **win rate**, and **goal difference per game**—reveal systematic advantages between confederations, particularly between **UEFA** and **CONMEBOL**. In addition, statistical tests are used to explore the relationship between team success and **FIFA rankings**.

---

## How the Data Will Be Used

Each dataset contributes to answering a specific research question by being transformed into indicators of performance. The following is a breakdown of how the data is used:

### 1. Historical World Cup Data (1930–2022)

- **Purpose**: Build the primary measure of success (stage score), and compute win rate and goal difference per game.  
- **Usage**:
  - Assign scores from 1 (Group Stage) to 6 (Champion) for each team’s performance per tournament.
  - Aggregate results by team and confederation.
  - Use match outcomes to calculate win rate and goal difference per game.

### 2. FIFA Rankings (1994–2022)

- **Purpose**: Evaluate how pre-tournament expectations (rankings) align with actual success.  
- **Usage**:
  - Compute each team’s average FIFA ranking across the years they participated post-1994.
  - Correlate these values with post-1994 stage scores using Spearman correlation.

### 3. Confederation Info

- **Purpose**: Compare performance between different global football regions.  
- **Usage**:
  - Group and analyze results by confederation.
  - Visualize and test performance trends (e.g., UEFA vs. CONMEBOL).

These steps enable the use of data not just descriptively, but also to conduct rigorous, testable comparisons that support meaningful insights into long-term patterns of team success at the FIFA World Cup.


## Exploratory Data Analysis (EDA)

To understand the data before testing hypotheses, some basic exploratory analysis was conducted. This included checking for missing values, identifying outliers, and examining the distribution of stage scores.

---

### 1. Missing Value Analysis

![Figure 1: Heatmap of Missing Values](output/Missing%20Value%20Analysis.png)

A heatmap was used to detect missing values in the dataset.  
While the majority of the data is complete, a few columns — including FIFA rankings and post-1994 stage scores — contain missing entries. These are mostly due to data being unavailable for certain teams or tournaments.  
Rows with missing values were handled appropriately depending on the analysis.

---

### 2. Outlier Detection

![Figure 2: Outlier Detection for Total Stage Score](output/Outlier%20Detection.png)

A boxplot was generated to visually inspect potential outliers in total stage scores.  
A few exceptionally high-performing teams stand out as statistical outliers, especially from UEFA. These include teams like Germany and Brazil.  
These values were kept in the dataset, as they represent meaningful historical achievements.

---

### 3. Skewness of the Distribution

The skewness of the total stage score distribution was calculated to assess its symmetry.  
A strong right-skew was observed (**skewness ≈ 1.99**), meaning that most teams have relatively low scores, while a small number have achieved very high totals.  
This reflects the dominance of a few elite teams in World Cup history.

---

### 4. Summary

The dataset is mostly complete and includes some meaningful outliers.  
The distribution of total stage scores is right-skewed, with a few teams consistently performing at a much higher level than the rest.  
These findings helped shape the next steps in visualization and hypothesis testing.


## Findings

### ![Stage Score Distribution by Confederation](output/Stage%20Score%20Distribution%20by%20Confederation.png)  

**Figure 1: Stage Score Distribution by Confederation**

This box plot displays the distribution of stage scores (1 = Group Stage, ..., 6 = Champion) by confederation.

- **CONMEBOL** shows the highest median (~2.5) and the widest spread, indicating frequent deep tournament runs and multiple championships.
- **UEFA** follows with a median around 3 and several high stage scores as outliers, reflecting consistent semifinal and final appearances.
- **CAF**, **AFC**, **CONCACAF**, and **OFC** mostly cluster near the bottom, with medians at 1, signaling regular group-stage exits and only a few outlier performances in later stages.

### ![Average Win Rate by Confederation](output/Average%20Win%20Rate%20by%20Confederation.png)  
**Figure 2: Average Win Rate by Confederation**

This bar chart shows the average match win rates for each confederation across all World Cup tournaments.

- **CONMEBOL** leads with a win rate of **0.43**, reflecting dominant performances across decades.
- **UEFA** follows with **0.37**, also indicating a strong historical record.
- **CAF**, **CONCACAF**, and **AFC** show lower win rates (0.20, 0.18, and 0.15 respectively), highlighting the challenge these regions face against top-tier opponents.
- **OFC** records **0.00**, showing no World Cup match victories, which aligns with its historically limited representation.
- Overall, this distribution aligns with the stage progression seen in Figure 1: confederations that win more often also tend to advance further.


### ![Stacked Histogram of GD per Game by Confederation](output/Stacked%20histogram-%20GD%20per%20Game%20by%20Confederation.png)  
**Figure 3: Stacked Histogram of GD per Game by Confederation**

This histogram shows the distribution of **goal difference per game** (GD/game) for each confederation, grouped in bins of 0.25.

- **CONMEBOL** and **UEFA** dominate the positive side, with most matches resulting in GD values between **+0.5 and +1.5**, suggesting consistent and decisive wins.
- **CAF**, **CONCACAF**, and **AFC** concentrate around **–0.5 to +0.5**, reflecting close games with narrow margins, often indicating parity or struggle against stronger opponents.
- **OFC** appears rarely, confirming the confederation’s minimal World Cup involvement.
- These results support earlier findings: South American and European teams not only win more often (Figure 2), but also win **by larger margins**.


### ![Total Stage Score by Confederation per Tournament](output/Total%20Stage%20Score%20by%20Confederation%20per%20Tournament.png)  
**Figure 4: Total Stage Score by Confederation per Tournament**

This stacked bar chart displays the **sum of all teams' stage scores** per World Cup, grouped by confederation.

- **UEFA** and **CONMEBOL** dominate each tournament’s total, contributing approximately **60–65 points** in recent editions.
- Between **1930 and 1978**, their joint contribution was lower (~45–55), mainly due to fewer European participants in earlier years.
- From **1998 onward**, contributions from **AFC**, **CAF**, and **CONCACAF** have **steadily grown**:
  - In **2022**, AFC and CAF each contributed **9 points**, and CONCACAF added **5**.
- **OFC** remains almost invisible, indicating minimal impact.
- While Europe and South America still **lead in cumulative performance**, the data suggests **increased competitive presence** from other regions in the knockout stages over the past two decades.


### ![Figure 5 - Average Stage Score Over Time by Confederation](output/%20Average%20Stage%20Score%20Over%20Time%20by%20Confederation.png)  
**Figure 5: Average Stage Score Over Time by Confederation**

This multi-line chart tracks the **average stage score** of each confederation across World Cups from 1930 to 2022.

- **CONMEBOL** and **UEFA** started strong, averaging around **3.0**, and peaked at:
  - **4.0 for CONMEBOL** in 1938 and **4.3 in 1978**
  - **3.4 for UEFA** in 1954 and **3.3 in 1978**
- Since **1982**, both confederations have hovered between **2.3 and 2.8**, with a dip to ~2.1–2.2 in the early 2010s.
- **CAF**, **AFC**, and **CONCACAF** have mostly remained below **2.0**, reflecting **limited progression beyond the Round of 16**.
  - Minor upticks occurred, such as **CAF hitting 2.0 in 1990**.
- **OFC** has consistently averaged **1.0**, indicating **group-stage exits**.

This trend confirms a **long-standing performance gap**: Europe and South America consistently advance to later rounds, while other confederations remain limited in tournament depth.


## Hypothesis Testing

This section presents two statistical tests designed to investigate historical performance patterns in the FIFA World Cup. Each test is supported with a data visualization and analytical interpretation.

---

### Test 1: UEFA vs. CONMEBOL – Total Stage Score

**Objective**  
To examine whether UEFA teams have achieved higher cumulative World Cup success than CONMEBOL teams.

**Test Used**  
Welch’s t-test (one-sided, unequal variances)

**Hypotheses**  
- **H₀:** CONMEBOL teams have equal or higher total stage scores than UEFA teams.  
- **H₁:** UEFA teams have higher total stage scores than CONMEBOL teams.

**Visualization**  
![Figure 1: Total Stage Score by Confederation](output/UEFA%20vs%20CONMEBOL%20Stage%20Scores.png)

**Interpretation**  
The boxplot comparing total stage scores by confederation reveals that CONMEBOL teams generally have slightly higher and more consistent success in the World Cup. Although UEFA teams include several high-performing outliers, the overall distribution is more spread out, suggesting greater variation in performance levels. In contrast, CONMEBOL teams show a narrower interquartile range and a higher median, indicating that they have delivered more stable and uniformly strong results over time. This pattern visually supports the idea that while UEFA includes both very strong and less competitive teams, CONMEBOL teams tend to perform well more consistently.


**Statistical Result**  
- **t-statistic:** –1.082  
- **p-value (one-sided):** 0.847

**Conclusion**  
The null hypothesis cannot be rejected.  
There is no statistically significant evidence that UEFA teams have outperformed CONMEBOL teams in total stage scores.  
Although UEFA features some exceptionally strong teams, the overall performance is not significantly better than CONMEBOL’s historically consistent success.

---

### Test 2: Correlation Between FIFA Ranking and Stage Score

**Objective**  
To assess whether there is a relationship between a team’s average FIFA ranking and its World Cup performance (measured as total stage score from 1994 onward).

**Test Used**  
Spearman Rank Correlation (two-sided)

**Hypotheses**  
- **H₀:** No monotonic correlation exists between FIFA ranking and stage score.  
- **H₁:** A monotonic correlation exists.

**Visualization**  
![Figure 2: Stage Score vs. Average FIFA Ranking](output/Stage%20Score%20vs.%20Average%20FIFA%20Ranking.png)

**Interpretation**  
The scatterplot examining the relationship between average FIFA ranking and World Cup stage score reveals a clear negative trend. As a team’s average FIFA ranking improves (i.e., the ranking number decreases), its stage score tends to increase. The majority of teams with high stage scores are concentrated in the lower-left part of the graph, meaning that better-ranked teams generally progress further in the tournament. This relationship holds across different confederations, particularly among UEFA and CONMEBOL teams, and aligns with the expectation that FIFA rankings, despite some limitations, are a meaningful reflection of actual competitive strength in World Cups.

**Statistical Result**  
- **Spearman’s ρ:** –0.822  
- **p-value:** < 0.001

**Conclusion**  
The null hypothesis is rejected.  
There is a strong and statistically significant negative correlation between FIFA ranking and World Cup performance.  
This confirms that FIFA rankings are reflective of actual team strength and are predictive of tournament success.




 



  

