# DataScienceFantasyFootballRankings

## Intro:
 This project was undertaken because we sometimes look at fantasy rankings all the time and we just take people for their word. 
 It's common that in Fantasy Football the more targets and carries (usage) the more points. 
 I wanted to see how accurate it really is and if it's better to model with each position or with ALL position in football. For this project just WR and QB compared to the whole league
 Testing the hypothesis that the best way to rank the league is best on usage by position and not by the whole league in general. Helping me do better in my own league draft next year.

## Selection of Data:
### The source of the dataset https://www.kaggle.com/mur418/espn-2019-stats-and-2020-nfl-fantasy-projections?select=wr_stats_and_projections.csv. 

### The dataset was a little hard to work with football is a little weird because it is filled with small sample sizes and its really hard to predict based on a coaches game plan for each game so we are just making some educated guesses on player performance. I also had to deal with missing stats NAN values. What hurt the most not able to see stats like fumbles making an impact production.

### Methods: 

#### from sklearn.model_selection import train_test_split 
#### from sklearn.linear_model import LinearRegression
#### from sklearn.metrics import r2_score
#### from sklearn.metrics import accuracy_score

### Everything above was used to help me figure out correlation and standard error to see how accurate the model was
![alt text](https://github.com/Delizcolonj/DataScienceFantasyFootballRankings/blob/main/ModelExample.PNG)
# This is how I modeled each dataset using LinearRegression


## Results: 
![alt text](https://github.com/Delizcolonj/DataScienceFantasyFootballRankings/blob/main/League%20Usage%20v.s%20Total%20fantasy%20points.PNG)
## coeffecient of determination: 0.7906181930234907, want to be as close to 1 as possible,  Error in points: 29.486804515059248 almost 30 points innaccuracy 
![alt text](https://github.com/Delizcolonj/DataScienceFantasyFootballRankings/blob/main/QB%20Usage%20v.s%20FantasyPoints.PNG)
## coeffecient of determination: 0.9847091096554346 super close to 1,  Error in points: 5.7732321650908025 only a 5 point error difference
![alt text](https://github.com/Delizcolonj/DataScienceFantasyFootballRankings/blob/main/WR%20usage%20v.s%20fantasy%20points.PNG)
## coeffecient of determination (r^2): 0.986955247513537 super close to 1, Standard error of points per QB and usage 16.07464543035994 pretty normal for a QB
# Answer to Results: Since the coefficient of determination is .79 for league usage v.s fantasy points super low,  and the standard error is super high compared to the other two models, it would be best to just model the positions separately. And since the correlations based on postion QB and WR is super high it is safe to say that there seems to be a correlation between usage and fantasy points. Thus, backing up the original hypothesis

# Why it matters:
## We take no L's out here :D. because based on usage we can model and now try to predict injuries that can occur and test a new hypothesis on; "the more usage the more likely one is to be injured". Now models can be used to extend the longevity of position players and add more rules to protect players just like the NFL has done with the QB position.
## Most Important Finding: Figuring out how rankings are done to make my own and tailor the data to the way I like to play fantasy football, so I don't have to rely on the opinons of others but so that I could rely on facts and use statistics to help me gain a competitive advantage

