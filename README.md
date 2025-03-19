# 2026worldcup_prediction
Predicting the FIFA 2026 World Cup Qualification and Winner

## Project Overview
This project aims to predict which teams will qualify for the FIFA 2026 World Cup and determine the potential tournament winner by analyzing historical international football match data.

## Motivation  
Football has always been a passion of mine, and the FIFA World Cup has been one of my favorite sporting events since childhood. The excitement, unpredictability, and high-level competition make it a unique tournament where data-driven insights can help uncover hidden patterns and trends.As someone who aims to build a career at the intersection of **football and data science**, I wanted to use this project as an opportunity to gain hands-on experience in football analytics. By applying **data science techniques to real-world football data**, I hope to develop practical skills that will be useful in my future career.

## Objectives
- Predict World Cup 2026 qualification outcomes based on past qualifiers and current group standings.
- Predict the 2026 World Cup winner using historical match data.
- Analyze significant factors influencing match results, including FIFA rankings, home advantage, and squad strength.

## Dataset  

This project utilizes **nine datasets** to predict FIFA 2026 qualification and the tournament winner. Each dataset is explained below:  

### Historical World Cup Match Results (1872-2024)
- This dataset contains all international matches played from **1872 to 2024**.  
- It includes match date, teams involved, goals scored, and match results (**Win, Draw, Loss**).  
- It also provides information on the tournament stage (**Group, Knockout, Final**).  
- This data helps train the model by identifying patterns in match outcomes.  

### FIFA Rankings (1992-2024)
- This dataset includes **FIFA rankings and Elo ratings** for national teams from **1992 to 2024**.  
- It provides insight into how a team’s ranking evolved over time.  
- It helps measure **team strength** and predict match results.  

### 2026 FIFA World Cup Qualifier Groups
- This dataset includes the **official qualification groups** for the **FIFA 2026 World Cup**.  
- It contains information on **teams in each group, match schedules, and qualification format**.  
- Since qualification matches are still ongoing, this data will be used to predict **which teams will qualify** based on historical trends and FIFA rankings.  

### Goalscorers & Team Performance Data
- This dataset contains **goal statistics** from past FIFA World Cups.  
- It tracks **total goals scored per team and individual top scorers**.  
- It helps analyze **offensive performance trends** in international tournaments.  

### Shootout Data (For Knockout Stage Analysis) 
- This dataset includes records of **penalty shootouts** from past World Cups.  
- It helps analyze **how teams perform in high-pressure knockout situations**.  
- It is useful for predicting **tournament knockout round outcomes**.  

### Team Name History (Data Cleaning Support) 
- This dataset ensures **historical team name consistency** for accurate data merging.  
- It includes **changes in country names** (e.g., Yugoslavia → Serbia, Netherlands Antilles → Curaçao).  

### List of FIFA World Cup Finals
- This dataset contains **past FIFA World Cup final matches** and their results.  
- It helps analyze trends in **finalist success and championship-winning teams**.  

### Teams Reaching the Top Four
- This dataset includes all **semi-finalists and finalists** from past tournaments.  
- It helps identify **historically strong teams** that consistently reach the final stages.  

### Squad Market Values (2006-2026)
- This dataset contains the **total market value of each national team** from **2006 to 2026**.  
- The data is collected from **Transfermarkt** and represents **player market values** aggregated by team.  
- It helps estimate **team strength based on financial value**.

## Data Collection Plan  

The datasets will be sourced from **Kaggle, FIFA and Transfermarkt**. The key steps are:  

- **Historical match results (1872-2024)** and **FIFA rankings (1992-2024)** will be downloaded from Kaggle and FIFA.com.  
- **2026 World Cup qualifier groups** will be manually compiled from FIFA.  
- **Goalscorers, team performance, and shootout data** will be obtained from Kaggle.  
- **Squad market values (2006-2026)** will be collected from Transfermarkt.  

 



  

