 **#Experiment 1: EDA in IPL Dataset**
## NAME: SYED SAIF SYED GHOUSE
## REG NUMBER: 212224230286
**Aim:**
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

**Algorithm / Procedure:**

**1.Import Libraries**
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
**2.Load Dataset**
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
**3.Matches per Season (Univariate Analysis)**
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
**4.Top Winning Teams (Univariate Analysis)**
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
**5.Toss Decisions (Univariate Analysis)**
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
**6.Top Venues (Univariate Analysis)**
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
**7.Draw Insights**
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  **Program**
  ```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
matches = pd.read_csv("matches.csv")
print("Dataset Shape:",matches.shape)
print("columns:",matches.columns)
print(matches.head())
matches_per_season = matches['season'].value_counts().sort_index()
matches_per_season
plt.figure()
matches_per_season.plot(kind='bar')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played Per IPL Season | SYED SAIF : 212224230286")
plt.show()
team_wins = matches['winner'].value_counts()
team_wins
top_5_teams = team_wins.head(5)
top_5_teams
plt.figure()
top_5_teams.plot(kind='bar')
plt.xlabel("Team")
plt.ylabel("Number of Wins")
plt.title("Top 5 Winning Teams in IPL | SYED SAIF : 212224230286")
plt.xticks(rotation=45)
plt.show()
toss_decision_counts = matches['toss_decision'].value_counts()
toss_decision_counts
plt.figure()
toss_decision_counts.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Number of Times Chosen")
plt.title("Toss Decision Preference in IPL | SYED SAIF : 212224230286")
plt.show()
venue_counts = matches['venue'].value_counts()
venue_counts
```
 
 **Output**
 
<img width="711" height="806" alt="Screenshot 2026-02-02 090524" src="https://github.com/user-attachments/assets/8b59c7d7-6bc3-44b7-9fd8-99acad21ddc3" />
<img width="709" height="772" alt="Screenshot 2026-02-02 090535" src="https://github.com/user-attachments/assets/c302ebf8-6094-4ec0-add2-40b3f8b37bc4" />
<img width="710" height="554" alt="Screenshot 2026-02-02 090555" src="https://github.com/user-attachments/assets/e1069226-f83c-4296-983d-46f47279cfc4" />
<img width="714" height="390" alt="Screenshot 2026-02-02 090610" src="https://github.com/user-attachments/assets/bb489895-eaf5-430c-8ee4-d3e3b6193bed" />
<img width="717" height="678" alt="Screenshot 2026-02-02 090619" src="https://github.com/user-attachments/assets/68acc2ac-ee1a-4066-a8a2-8289daba8f3d" />

 ** Result**
 ThE experiment is executed successfully.

