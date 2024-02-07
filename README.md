# Data Bootcamp Project 1

# Project Information: 
Executive Summary: https://docs.google.com/document/d/1xhIPxAR5KVHRAyKF5ryFT5mmiWvbziGh75YVDfb3IDo/edit \
Slide deck: https://docs.google.com/presentation/d/1BPzSST4ZOAHA2o2NfFrhEX57UMo1IZ9aTmDza9jV8FA/edit#slide=id.g35f391192_04

## keegan.ipynb
### Description
keegan.ipynb uses data from the NBA and nba_api package to determine if playoff performance can be predicted by regular season performance when looking at average point differential and win percentage.
### Requirements
The pandas, matplotlib.pyplot, scipy.stats, numpy, and nba_api modules are required for this project. 
### Installation
Clone the repository: git@github.com:kcwaggs/project_1.git
### Usage
Select a python kernel and run all code blocks to create the necessary dataframes and visualizations. The bar graphs need to be manually saved to avoid having the team names cut off on the x-axis labels. 
### Data Sources
Get team by ID - https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/static/teams.md \
NBA champions by year - https://en.wikipedia.org/wiki/List_of_NBA_champions \
Points against and opponents points scored for playoffs and regular season - https://www.nba.com/stats/teams/opponent?Season=2019-20 \
NBA team hex colors - https://nbacolors.com/ \
Team stats by year (nba_api) - https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/endpoints/teamyearbyyearstats.md 
### Code Sources and Errors
Double bar graph with labels on top of bars - https://matplotlib.org/stable/gallery/lines_bars_and_markers/barchart.html#sphx-glr-gallery-lines-bars-and-markers-barchart-py \
Need to manually save double bar graph or else the team names are cut off 
### Analysis
When trying to determine if playoff performance can be predicted by looking at regular season performance, the average point differential and win percentage were observed for the regular season and playoffs for NBA championship teams in the 2000-2020 finals. After retrieving the data from the nba_api package and other NBA datasets, a double bar graph was created to visualize the point differential in the regular season and the playoffs for all teams. In order to find if there is a linear relationship between regular season and playoff scoring differential, the regular season point differential was plotted against the playoff point differential on a scatter plot. A linear regression was performed and the r-value was 0.104 and the p-value was 0.654. Given these results, the r-value indicates there is a weak positive linear correlation between point differential in the regular season and the playoffs, but because the p-value is much greater than 0.05, the correlation is not statistically significant and could be due to random chance. To find if there is a linear relationship between regular season and playoff win percentage, the regular season win percentage was plotted against the playoff win percentage on a scatter plot. A linear regression was performed and the r-value was -0.066 and the p-value was 0.775. Given these results, the r-value indicates there is a very weak negative linear relationship between regular season win percentage and playoffs win percentage, but because the p-value is much higher than 0.05, the correlation is not statistically significant and could be due to random chance.

## casey.ipynb
### Description
This analysis uses data from public Kaggle CSVs for player data and stats to evaluate players and their experience to the college they attended. 
### Data Sources
Player Stats Data: https://www.kaggle.com/datasets/bme3412/nba-player-stats-20002020-seasons?resource=download \
NBA Player Data: https://www.kaggle.com/datasets/justinas/nba-players-data \
college hex colors: https://teamcolorcodes.com/ncaa-color-codes/# \
NBA Logo hex colors: https://www.brandcolorcode.com/nba-national-basketball-association \
### Analysis
When evaluating a player's background and college attended I quickly realized that I would need more information than what was available in the API our team had found. I found public-source data in Kaggle to utilize in order to better dig into my question - "Does the college a player attended impact their NBA career?". In my analysis I saw that there were 290 colleges for the 2,061 players in the NBA from 2000-2020. 406 of these players came from the top 10 colleges (shos in my figures). From hre I created bins to group colleges by how many players they had go into the NBA. From this analysis I can conclude that the average length of a player's career increases for those who went to colleges that had more NBA players. The average amount of games also increased for the top colleges. 
