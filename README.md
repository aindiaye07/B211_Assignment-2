# B211_Assignment-2

Purposes of Program:
- Analyze player statistics from the provided Kaggle subset
- Identify top performers across various shooting and defefensive metrics
- Assisting in scouting, team optimization, and player evaluation

Class Design and Implementation:
- Python Class: PlayerStatsAnalyzer
- Data Loading
- Calculation = Calculating new columns for percentages and per-minute/per-game stats
- Ranking = Using .sort_values() and .head(100) to generate top-100 lists

Class Attributes:
- FG_Pct, 3P_Pct, FT_Pct = Standard shooting percentages
- Pts_Per_Min = Total points divided by total minutes
- Overall_Shot_Pct = Combined field goal percentage (Total Makes/Total Attempts)
- Blk_Per_Game/Stl_Per Game = Defense metric calculated by diving totals by games played

Limitations:
- Sample Size = Players who don't have a lot of playing time may appear in the top 100 because of skewed percentages. A minimum threshold should be added for better accuracy
- Data Completeness: Missing or zero values cause errors
