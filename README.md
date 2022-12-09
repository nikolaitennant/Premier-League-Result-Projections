Final Project on Predicitng Premier League Results

Project uses data on the Premier League seasons of 2021/2022 and the current season, 2022/2023. With billions of dollars, football is the most funded sport in the world. For example, the cost of this year’s World Cup is $220 billion.  In addition, bettors stake an average of £2.7 million per Premier League match, and the Premier League and its clubs have a billion social media followers.  Therefore, reliably forecasting the next winner could be helpful in betting, fantasy sports leagues, and overall game enjoyment.

Data consists of eight features, including the target variable, Results, and 457 data points (matches) before lagging and preprocessing. The features are Referee, B365H, B365D, B365A, HICT, AICT, DifICT, and Result (target). Referee is a categorical variable that stores each match’s referee. This data was downloaded from an intermediary that holds every Premier League Season match record.  B365H, B365D, and B365A are continuous variables originating from 365Bets that are included in the Premier League match records intermediary data.  Each indicates the likelihood that its corresponding postfix will occur: (H - Home win, D - Draw, A - Away win). In addition, their values govern the amount of money returned for each $1 wagered; thus, the higher the value, the smaller the likelihood that the event will occur. The continuous features HICT (Home) and AICT (Away) reflect the strength of each team, while the DifICT (difference between HICT and AICT) shows the difference in strength between the two teams. I derived these scores from the Fantasy Premier League (FPL) ICT index, which is available in a GitHub repository that holds Fantasy Premier League API data.  ICT scores are evaluations of a player’s performance in each match. A better performance earns a better score. I based each team’s first rating on their FIFA 22 or 23 rating, which I got from Kaggle, and then used the sum of each player’s ICT score for each match to update the teams' ratings from match to match continuously.  A positive DifICT suggests that the Home team is stronger, whereas a negative DifICT indicates that the Away team is stronger. Lastly, there are three possible outcomes for the multiclassification target variable Result: Home win/Away loss (2.0),  Draw (1.0) and Home Loss/Away win (0.0). This variable was represented numerically and taken from the Premier League match record intermediary.  Result is ordinal after this transformation, with the order being: win, draw, and loss (from best to worst). 

Python version is 3.10.5
numpy version 1.22.4
matplotlib version 3.5.2
sklearn version 1.1.1
pandas version 1.4.2
xgboost version 1.5.1
shap version 0.40.0
lightgbm 3.3.3

MIT License
