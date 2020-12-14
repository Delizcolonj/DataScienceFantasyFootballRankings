# DataScienceFantasyFootballRankings

## This project was undertaken because we see and sometimes look at fantasy rankings all the time and we just take people for their word. It's common to that in Fantasy Football the more targets and carries one gets (usage) usually scores the most points I wanted to see how accurate it really is and if it's better to model with each position or with ALL position in football. For this project just WR and QB compared to the whole league

## Testing the hypothesis that the best way to rank the league is best on usage by position and not by the whole league in general. Helping me do better in my own league draft next year.

### The source of the dataset https://www.kaggle.com/mur418/espn-2019-stats-and-2020-nfl-fantasy-projections?select=wr_stats_and_projections.csv. 

### The dataset was a little hard to work with football is a little weird because it is filled with small sample sizes and its really hard to predict based on a coaches game plan for each game so we are just making some educated guesses on player performance. I also had to deal with missing stats NAN values. What hurt the most not able to see stats like fumbles making an impact production.

### Methods: 
#### import numpy as np 
#### import pandas as pd
#### from sklearn.model_selection import train_test_split 
#### from sklearn.linear_model import LinearRegression
#### from sklearn.metrics import r2_score
#### from sklearn.metrics import accuracy_score

### Everything above was used to help me figure out correlation and standard error to see how accurate the model was

## Results: 
