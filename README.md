# Position Matters: Statistical Profiles Across The PLL
This is a project in progress. Pages will be updated as work is completed.


## Background

The Premier Lacrosse League (PLL) is a professional lacrosse league created in 2018 by Paul and Mike Rabil. It consists of eight teams split into two conferences, East and West. The regular season is made up of ten weekends with a break for the all-star weekend in the middle. The PLL is one of the fastest-growing sports leagues in the United States, and it is expected to continue growing in popularity. 

Each year, the PLL holds a draft to allow each team the opportunity to change its roster. Each team tries to create a combination of players that maximizes their wins during the regular season in order to make it to the Post-Season Playoffs. 

## The Project
Hence, this project is a two-part exploratory data analysis to analyze player and team performance in the Premier Lacrosse League in 2025. First, a positional analysis is done to establish positional statistics and identify the top players (by position) using a combination of volume, efficiency, and position-based metrics. Then, a team-level analysis extends the project to determine if individual statistics are associated with team wins. A Random Forest Regressor model validated the correlation results to pinpoint faceoff win percentage and shooting percentage as the top statistics a team should prioritize.

The model could be improved with the addition of multiple seasons' data, which could impact the feature importances. Despite this, multiple models were used to corroborate the results, so I can safely assume the results are accurate. 

The findings were then integrated into a Tableau Dashboard available to view [here](https://public.tableau.com/views/PositionMattersStatististicalProfilesAcrossthePLL/Dashboard3?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

## The Results
First, an exploratory data analysis of each position was completed. The rankings of top players based on statistics aligned with industry results within one rank on four of six analyses performed, highlighting accuracy in the methods used. Notable findings included the importance of working with teammates to deliver successful offensive plays (see *Attack* below), win clean faceoffs (see *Faceoff* below), and defend against opposition (see *Defensive Midfielders*). There were some clear limitations due to the use of only one season's data, small numbers of highly-skilled positions (goalies, faceoffs), and lack of defenseman-specific statistics (lockdown rating). Despite this, the underlying emphasis on teamwork highlights a fundamental skill when playing professional lacrosse.

Then, using the same dataset from individual players, team-level statistics were calculated. A feature-analysis was done using a basic correlation model (Pearson's correlation coefficient) and a Random Forest Regression model. The results validated one another and indicated that shooting percentage and faceoff win percentage had the strongest relationship with team wins. However, no feature had a relationship that was considered statistically strong. This is attributed to the small sample size of ten teams and a single season's data.

Overall, the importance of teamwork and collaboration in a professional lacrosse is made clear through the statistical analyses of both player-level and team-level data.

**Sample Dashboard** <br>
A sample of the interactive dashboard is shown below. 
<img width="2399" height="1349" alt="Dashboard 3" src="https://github.com/user-attachments/assets/26a9b839-aec7-410a-8615-bebf5c837ab2" />

The full dashboard can be viewed [here](https://public.tableau.com/views/PositionMattersStatististicalProfilesAcrossthePLL/Dashboard3?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

## The Suggestions
As stated earlier, each team in the PLL drafts players each year in an attempt to win games in the regular season and make it to the Play-offs in the post-season. While specific statistics are not strongly correlated with team wins, teams can still focus on recruiting players that help them succeed in games. It is suggested that teams:
- Prioritize improving faceoff win percentage and shooting percentage to win games.
- Highlight the importance of teamwork to ensure smooth play execution.
- Utilize a variety of statistics to evaluate players against one another.

## The Files
*PLL_EDA_Data_Pre-Processing (1).ipynb* - Data cleaning and pre-processing for Positional Analysis. <br>
*PLL_Positional_Analysis.ipynb* - Positional analysis process and results. <br>
*PLL_EDA_Team_DataCleaning.ipynb* - Data cleaning and pre-processing for Team Analysis.<br>
*PLL_EDA_TeamAnalysis.ipynb* - Team Analysis process and results. <br>

*Timeline.md* - A file detailing the ongoing status of the project over time.

## Detailed Results

**Positional Analysis** <br>
In the *attack* results, the top three attackmen had almost equal amounts of one-point goals and assists, indicating a strong ability to work with their teammates to set up successful plays. None of the top attackmen scored any two-point goals during the 2025 season which indicates their preference for close-range strategies.

Through investigating the *midfielders*, the average number of assists per game is skewed towards the lower end, with 75% of players having less than an average of 0.5 assists per game. It is considered typical for a midfielder's role because they focus on transitions between offense and defense without necessarily taking part in attack strategies.

Next, the *long-stick midfielders* and *short-stick defensive midfielders* were analyzed together as the defensive midfielders. I looked at the distribution of caused turnovers to turnovers for the top players and determined that caused turnovers were in the majority for most players, highlighting the primarily defensive role of these positions. When ranking players, however, the findings were limited because the results skewed towards long-stick midfielders. It is suggested that different statistics are used to analyze short-stick defensive midfielders in future studies.

Then, the *defensemen* were investigated. However, the scope of the results was very limited due to the lack of industry-standard statistics available (Lockdown rating was not included).

The *faceoff* players were the second-to-last to be analyzed. While the top players had faceoff win percentages of safely over 50%, the proportion of clean to unclean faceoff wins had great variation between the top players. This suggests that midfielders and teammates play a larger role in faceoffs and starting plays than anticipated.

Finally, the distribution of the *goalies* statistics was visualized. The average number of saves per game was skewed towards the higher end, demonstrating the high number of shots goalies face every game. To differentiate the top goalies, I investigated the distribution of clean save percentages to determine whether it correlated with higher rankings. The boxplot showed that a higher ranking does not necessarily correlate with a higher clean save percentage. A further hypothesis test was considered but not pursued due to the small sample size of only 10 goalies.  

**Team Analysis** <br>
Through a basic correlation analysis (using Pearson's correlation coefficient *r*), faceoff percentage has the highest correlation to a team's wins, with shooting percentage close behind. However, no statistic of the sample set had a strong relationship to team wins. In the future, it is suggested to use statistics from multiple seasons to prevent limitations from small sample sets.

The correlation analysis was further investigated using a Random Forest Regression model. The statistics were treated as features and the importance of each feature was analyzed in the results. The importances are Mean Decreases in Impurity and values over about 0.4 are considered features of high importance because they have a larger impact on determining the results. 

Shooting percentage is considered a feature of high importance with a value of 0.448. Faceoff percentage has the second-highest importance, so it is considered a support feature. These values validate the statistics found by the basic correlation model. However, only one of the features was considered high importance, which could be attributed to the small sample size.  

## References
Lacrosse, P. (2025). Premier lacrosse league stats. In Premier Lacrosse League Stats. https://stats.premierlacrosseleague.com/games

PLL awards. (2024). In Premier Lacrosse League. https://premierlacrosseleague.com/awards

Premier lacrosse league stats. (2025). In Premier Lacrosse League Stats. https://stats.premierlacrosseleague.com/player-table

Standings. (n.d.). In Premier Lacrosse League. Retrieved August 18, 2026, from https://premierlacrosseleague.com/standings
