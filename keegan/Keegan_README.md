# Data Bootcamp Project 1 - Keegan
## Description
keegan.ipynb uses data from the NBA and nba_api package to determine if playoff performance can be predicted by regular season performance when looking at average point differential and win percentage.
## Requirements
The pandas, matplotlib.pyplot, scipy.stats, numpy, and nba_api modules are required for this project. 
## Installation
Clone the repository: git@github.com:kcwaggs/project_1.git
## Usage
Select a python kernel and run all code blocks to create the necessary dataframes and visualizations. The bar graphs need to be manually saved to avoid having the team names cut off on the x-axis labels. 
## Data Sources
Get team by ID - https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/static/teams.md \
NBA champions by year - https://en.wikipedia.org/wiki/List_of_NBA_champions \
Points against and opponents points scored for playoffs and regular season - https://www.nba.com/stats/teams/opponent?Season=2019-20 \
NBA team hex colors - https://nbacolors.com/ \
Team stats by year (nba_api) - https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/endpoints/teamyearbyyearstats.md 
## Code Sources and Errors
Double bar graph with labels on top of bars - https://matplotlib.org/stable/gallery/lines_bars_and_markers/barchart.html#sphx-glr-gallery-lines-bars-and-markers-barchart-py \
Need to manually save double bar graph or else the team names are cut off 
## Analysis
When trying to determine if playoff performance can be predicted by looking at regular season performance, the average point differential and win percentage were observed for the regular season and playoffs for NBA championship teams in the 2000-2020 finals. After retrieving the data from the nba_api package and other NBA datasets, a double bar graph was created to visualize the point differential in the regular season and the playoffs for all teams. In order to find if there is a linear relationship between regular season and playoff scoring differential, the regular season point differential was plotted against the playoff point differential on a scatter plot. A linear regression was performed and the r-value was 0.104 and the p-value was 0.654. Given these results, the r-value indicates there is a weak positive linear correlation between point differential in the regular season and the playoffs, but because the p-value is much greater than 0.05, the correlation is not statistically significant and could be due to random chance. To find if there is a linear relationship between regular season and playoff win percentage, the regular season win percentage was plotted against the playoff win percentage on a scatter plot. A linear regression was performed and the r-value was -0.066 and the p-value was 0.775. Given these results, the r-value indicates there is a very weak negative linear relationship between regular season win percentage and playoffs win percentage, but because the p-value is much higher than 0.05, the correlation is not statistically significant and could be due to random chance.
