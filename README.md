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


**Sample Dashboard**
A sample of the interactive dashboard is shown below. 
<img width="2399" height="1349" alt="Dashboard 3" src="https://github.com/user-attachments/assets/26a9b839-aec7-410a-8615-bebf5c837ab2" />

The full dashboard can be viewed [here](https://public.tableau.com/views/PositionMattersStatististicalProfilesAcrossthePLL/Dashboard3?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

## The Suggestions

## The Files
*PLL_EDA_Data_Pre-Processing (1).ipynb* - Data cleaning and pre-processing for Positional Analysis. <br>
*PLL_Positional_Analysis.ipynb* - Positional Analysis process and results. <br>
*PLL_EDA_Team_DataCleaning.ipynb* - Data cleaning and pre-processing for Team Analysis.<br>
*PLL_EDA_TeamAnalysis.ipynb* - Team Analysis process and results. <br>

*Timeline.md* - A file detailing the status of the project after each work session.
