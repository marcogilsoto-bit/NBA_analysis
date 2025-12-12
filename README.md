# NBA_analysis
Player stats analysis and visualization

## Table of contents
- [Project overview](#project-overview)
- [Data sources](#data-sources)
- [Stack](#stack)
- [Data cleaning and preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)

## Project overview
Built an interactive dashboard using NBA data (1996–2023) with key stats — points, rebounds, and assists — to explore and compare player performance across seasons.
## Data sources
Used NBA player data from Kaggle (nba_players.csv), covering the 1996–1997 to 2022–2023 seasons..
## Stack
- CSV file - Data Source
- Python 3.14 - Data Analysis
  - pandas
  - numpy
  - matplotlib.pylot
  - matplotlib.dates
  - seaborn
  - statsmodels.formula.api
  - sklearn import datasets
  - scipy.stats
- Jupyter - Data Analyisis
## Data cleaning and preparation
The data required minimal preparation — I filled a few null values and built a pivot table for analysis.
## Exploratory data analysis
Verified player name formatting (first/last name and separators like “-” or “_”) and checked for duplicates to ensure unique player identification.
## Data analysis
- I began the analysis by creating a plot showing Kobe Bryant’s points per season, using distinct colors to highlight his best and worst seasons.
- The next step was to generalize this plot so that it could display the seasonal performance of any player (only the player’s name needs to be modified in the function).
- I further extended the function to accept other performance metrics as inputs — namely, assists (AST) and rebounds (REB).
- In addition to the main analysis, I was curious about which colleges have produced the most successful NBA players, so I visualized the top 10 colleges by total career points.
- Within each college, I highlighted the top five players and their respective statistics.
- While creating the charts in Python, I found them not particularly user-friendly, so I migrated the analysis to Tableau to make it more interactive for end users.
- Finally, I conducted a hypothesis test to verify whether the average points per season differed between Kobe Bryant and Allen Iverson, and between Tony Parker and Pau Gasol.
- Since the dataset was relatively small, I couldn’t rely on the Central Limit Theorem (and the sampling distribution of the statistics was not approximately normal). To address this, I performed a bootstrap analysis, generating 10,000 resampled means for each player to obtain more robust results.
## Results
- I created visualizations in Python and Tableau that display each player’s points (PTS), assists (AST), and rebounds (REB) by season.
- Kentucky stands out as the most successful college overall (the full top 10 is shown in the chart), and its top performer in points per season is Anthony Davis.
- With a 95% confidence level, we cannot reject the null hypothesis that the average season performance of Kobe Bryant and Allen Iverson are similar — the same conclusion applies to Tony Parker and Pau Gasol.
## Recommendations
Based on these results, it would be worthwhile to work with a larger historical dataset to enable comparisons across more players. In addition, incorporating additional variables that explain player performance could provide valuable insights and support the development of predictive models for future seasons.
