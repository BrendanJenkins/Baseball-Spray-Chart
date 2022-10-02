# Baseball Expected Spray Chart
## Introduction
In baseball, the defensive shift has become more and more popular over recent years. A defensive shift is when the defense moves an infield player to the other side of the infield, they do this because that batter tends to pull the ball more, so if they have more defenders on the batter's pull side then they can potentially make it harder for him to get a hit. You can read more information about the shift [here](https://en.wikipedia.org/wiki/Baseball_positioning).

#### Normal Defensive Placement: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Overshift Defensive Placement:
<img src="https://github.com/BrendanJenkins/Baseball-Spray-Chart/blob/main/images/Baseballpositioning-normal.png" align="left" title="Normal Defensive Alignment">  <img src="https://github.com/BrendanJenkins/Baseball-Spray-Chart/blob/main/images/Baseballpositioning-shift.png" align="centerright" title="Shift Defensive Alignment">

Teams have many different ways that they develop their shift, but essentially you want information about the batter and pitcher to create this shift. Some problems can arrise when only looking at the specific batter or pitcher in this matchup because when a rookie player comes up to the MLB, they have very limited data available, baseball's version of a cold start problem! In this repo, I explore a technique to combat this problem.  

## Data
I used pitch level data from 2015 to 2022 for this project. I utilized the [pybaseball](https://github.com/jldbc/pybaseball) library in order to harvest the data. The code for the data harvesting is located in `data_harvesting.ipynb`.

## Techniques
In `pitcher_batter_cluster.ipynb`, I utilized two KMeans clustering models to group similar pitchers together. For one model, I clusters with respect to the pitchers' average pitch characteristics. The motivation behind this is to group pitchers that through with similar velocities and breaks together. The other cluster is clustered with respected to the pitchers' pitch distribution. The idea behind this is that if a pitcher relies on his fastball more, then the batter can cheat to the fastball and pull it easier.

## Next Steps
A potential next step is to conduct more analysis about what is the optimial number of clusters in each KMeans model.
