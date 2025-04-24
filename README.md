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

### Exploratory Data Analysis (EDA)

EDA was used to understand long-term performance patterns and compare confederation-level success.

**Visualization Types:**
- Boxplots for stage score and goal difference by confederation
- Histograms for win rate and goal difference per game
- Stacked bar charts for confederation success per year
- Line charts for average stage score over time
- Bar charts for comparing averages across groups

These visuals helped highlight historical dominance, variability, and competition trends among confederations.

---
## Statistical Analysis

The third stage of the project focuses on examining long-term patterns in World Cup performance using statistical methods. The goal is to evaluate whether measurable indicators of success—such as **stage progression**, **win rate**, and **goal difference per game**—reveal systematic advantages between confederations, particularly between **UEFA** and **CONMEBOL**. In addition, statistical tests are used to explore the relationship between team success and **FIFA rankings**.

### Hypothesis Testing

Two key hypothesis tests are conducted in this phase:

#### 1. UEFA vs. CONMEBOL Total Stage Score Comparison

- **Test Type**: Independent-samples *t-test*  
- **Objective**: Determine if UEFA teams have statistically higher total stage scores than CONMEBOL teams from 1930 to 2022.  
- **Interpretation**: This test measures whether UEFA teams have consistently advanced further in the tournament across all World Cups.

#### 2. Correlation Between Stage Score and FIFA Rankings

- **Test Type**: *Spearman Rank Correlation*  
- **Objective**: Assess the relationship between a team’s average FIFA ranking (1994–2022) and its post-1994 tournament stage scores.  
- **Note**: Since FIFA rankings were introduced in 1992, only tournaments from 1994 onward are included in this analysis.  
- **Interpretation**: This test evaluates whether better-ranked teams perform better in World Cups.

Appropriate statistical thresholds and p-values are used to evaluate the significance of findings.

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


### ![Average Stage Score Over Time by Confederation](output/Average%20Stage%20Score%20Over%20Time%20by%20Confederation.png)  
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






 



  

