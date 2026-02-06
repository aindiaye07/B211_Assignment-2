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
- Data is grouped by player and season to calculate metrics.

Class Attributes:
- FG_Pct, 3P_Pct, FT_Pct = Standard shooting percentages
- Pts_Per_Min = Total points divided by total minutes
- Overall_Shot_Pct = Combined field goal percentage (Total Makes/Total Attempts)
- Blk_Per_Game/Stl_Per Game = Defense metric calculated by diving totals by games played

Methods:
- __init___(file_path) = Loading CSV data
- calculate_shooting_accuracies() = Computing FG%, 3P%, FT%, and overall shooting percentage
- calculate_scoring_efficiency() = Computing points per minute
- calculate_defensive_stats() = Computing blocks and steals per game
- get_top_100(metric_name) = Ranks and returns top 100 players for a metrics

Limitations:
- Sample Size = Players who don't have a lot of playing time may appear in the top 100 because of skewed percentages. A minimum threshold should be added for better accuracy
- Data Completeness: Missing or zero values cause errors
- Dataset is assumed to be a single, cleansed CSV file
