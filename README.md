# NFL Super Bowl Analysis

# Project Summary

The purpose of the project was to analyze data from all 57 Super Bowls that have been held by the NFL and projecting
point totals that Super Bowl winners and losers will score in the upcoming 15 Super Bowls. This project does not account
for plays run by Super Bowl teams, as well as any penalities that occurred.

# Data Collection

There were two data sets used to complete the analysis. The first dataset was created by Timo Bozsolik titled 'Super Bowl History 1967-2020' and was saved as a CSV file called superbowl.csv. This dataset included data from Super Bowls that were held between 1967 and 2020. The second dataset was one that I created that included Super Bowl data from 2021-2023. The second dataset was saved as a CSV file called superbowl2.csv.

# Super Bowl Data

The 'Super Bowl History 1967-2020' dataset contained 54 observations and 10 variables. 8 of the 10 variables were considered 'character' and 2 of the variables were considered 'integer'. The variables for the Super Bowl data consist of the following:

Date: Date that the Super Bowl was held. The format of the date is written as month, day, and year

SB: The Super Bowl number as a Roman numeral and in numerical format

Winner: Winner of the Super Bowl

Winner.Pts: Number of points scored by the winning Super Bowl team

Loser: Loser of the Super Bowl

Loser.Pts: Number of points scored by the losing Super Bowl team

MVP: Most Valuable Player (MVP) of the Super Bowl

Stadium: Stadium where the Super Bowl was held

City: City where the Super Bowl was held

State: State where the Super Bowl was held

# Libraries Used in R

The following libraries were used in R to complete the Super Bowl analysis:

- dplyr

- readr

- adabag

- tseries

- ggplot2

- stats

- forecast

- magrittr

# Data Preparation

The superbowl.csv file was uploaded into R and was called NFL. The NFL dataset had 54 observations and 10 variables. The superbowl2.csv file was uploaded into R and was called NFL2. The NFL2 dataset had 3 observations and 10 variables. Once these 2 datasets were uploaded into R, they were merged together as one whole dataset that was called NFL_list. The NFL_list contained 57 observations and 10 variables.

There were several subsets of the NFL_list dataset that were created by the state location where Super Bowls were held. The subsets created were called Florida, Texas, California, Georgia, Arizona, Louisiana, Michigan, Minnesota, Indiana, and New Jersey.

# NFL_List Data

An exploratory data analysis was conducted on all 57 Super Bowls before subsets occurred. Super Bowl winning teams scored roughly 30 points per victory (30.14 to be exact), with a maximum of 55 points and a minimum of 13 points. Super
Bowl losing teams scored roughly 16 points per defeat (16.47 to be exact), with a maximum of 35 points and minimum of 3 points.

Two teams (New England Patriots and Pittsburgh Steeleres) are tied for the most Super Bowl victories with 6. Two teams (Denver Broncos and New England Patriots) are tied for the most Super Bowl lossess with 5.

# Florida Super Bowls

There have been a total of 17 Super Bowls held in the state of Florida. The summary statistics show that Super Bowl winning teams have scored an average under 29 points (28.76 exactly), with a maximum of 49 points and a minimum of 16 points. Super Bowl losing teams have scored an average under 17 points (16.76 exactly), with a maximum of 31 points and a minimum of 7 points. After looking at summary statistics, the numbers of 


<img width="713" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/c167e94c-99bb-4af3-972b-55dd7742e682">

The Pittsburgh Steelers have the most Super Bowl victories in Florida with 3 (17.6%) and the San Francisco 49ers have the second most Super Bowl victories with 2 (11.8%).

<img width="661" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/c636f056-6b0b-4205-9019-393f72280e14">

The Dallas Cowboys have the most Super Bowl losses with 3 (17.6%) and the remaining losing Super Bowl teams each have
one defeat.






