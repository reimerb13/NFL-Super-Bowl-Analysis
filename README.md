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

An exploratory data analysis was conducted on all 57 Super Bowls before subsets occurred. Overall, 






