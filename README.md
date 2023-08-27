# NFL Super Bowl Analysis

# Project Summary

The purpose of the project was to analyze data from all 57 Super Bowls that have been held by the NFL and projecting
point totals that Super Bowl winners and losers will score in the upcoming 15 Super Bowls. A secondary purpose was to determine whether or not geographic location plays a role in Super Bowl scores. This project does not account for plays run by Super Bowl teams, as well as any penalities that occurred.

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

- usmap

# Data Preparation

The superbowl.csv file was uploaded into R and was called NFL. The NFL dataset had 54 observations and 10 variables. The superbowl2.csv file was uploaded into R and was called NFL2. The NFL2 dataset had 3 observations and 10 variables. Once these 2 datasets were uploaded into R, they were merged together as one whole dataset that was called NFL_list. The NFL_list contained 57 observations and 10 variables.

There were several subsets of the NFL_list dataset that were created by the state location where Super Bowls were held. The subsets created were called Florida, Texas, California, Georgia, Arizona, Louisiana, Michigan, Minnesota, Indiana, and New Jersey.

<img width="911" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/1b2aca67-8249-4cd8-a0dd-528dc5f958dd">



# NFL_List Data

An exploratory data analysis was conducted on all 57 Super Bowls before subsets occurred. Super Bowl winning teams scored roughly 30 points per victory (30.14 to be exact), with a maximum of 55 points and a minimum of 13 points. Super
Bowl losing teams scored roughly 16 points per defeat (16.47 to be exact), with a maximum of 35 points and minimum of 3 points.

Two teams (New England Patriots and Pittsburgh Steeleres) are tied for the most Super Bowl victories with 6. Two teams (Denver Broncos and New England Patriots) are tied for the most Super Bowl lossess with 5.

# Florida Super Bowls

<img width="911" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/cbba7356-286e-469b-bc45-10e571ead401">


There have been a total of 17 Super Bowls held in the state of Florida. The summary statistics show that Super Bowl winning teams have scored an average under 29 points (28.76 exactly), with a maximum of 49 points and a minimum of 16 points. Super Bowl losing teams have scored an average under 17 points (16.76 exactly), with a maximum of 31 points and a minimum of 7 points. After looking at summary statistics, graphical displays of the number of Super Bowl winning and losing teams were created.


<img width="713" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/c167e94c-99bb-4af3-972b-55dd7742e682">

The Pittsburgh Steelers have the most Super Bowl victories in Florida with 3 (17.6%) and the San Francisco 49ers have the second most Super Bowl victories with 2 (11.8%).

<img width="661" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/c636f056-6b0b-4205-9019-393f72280e14">

The Dallas Cowboys have the most Super Bowl losses with 3 (17.6%) and the remaining losing Super Bowl teams each have
one defeat.

# Texas Super Bowls

<img width="911" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/d210b74d-cf84-4d3e-ad77-d4ce1c7da5a2">


There have been a total of 4 Super Bowls held in the state of Texas. The summary statistics show that Super Bowl winning teams have scored an average over 30 points (30.25 exactly), with a maximum of 34 points and a minimum of 24 points. Super Bowl losing teams have scored over 22 points (22.25 exactly), with a maximum of 29 points and a minimum of 7 points. 

After viewing the statistical summaries, the Super Bowl winners and losers were determined. The New England Patriots have won the most Super Bowls in Texas with 2 victories. Each Super Bowl losing team (Atlanta Falcons, Carolina Panthers, Minnesota Vikings, and Pittsburgh Steelers) has one defeat.

# California Super Bowls

<img width="485" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/e76e8682-2c1e-470b-9efc-91421eb505bc">


There have been a total of 13 Super Bowls held in the state of California. The summary statistics show that Super Bowl winning teams have scored an average under 34 points (33.54 exactly), with a maximum of 52 points and a minimum of 14 points. Super Bowl losing teams have scored an average under 16 points (15.77 exactly), with a maximum of 24 points and a minimum of 7 points. After looking at summary statistics, graphical displays of the number of Super Bowl winning and losing teams were created.

<img width="1158" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/854641a1-d992-40c7-ad23-be9bf8d39603">


The Denver Broncos and Washington Redskins (now called the Washington Commanders) each are tied with two Super Bowl victories in California.

<img width="1158" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/b1abb1ce-8a45-4627-ac11-c38853d488cd">


The Denver Broncos and Miami Dolphins are tied with two Super Bowl defeats in California.

# Georgia Super Bowls

<img width="594" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/49e426c4-04f4-47db-b3fa-7ca698683672">


There have been a total of three Super Bowls held in the state of Georgia. The summary statistics show that Super Bowl winning teams have scored an average of 22 points, with a maximum of 30 points and a minimum of 13 points. Super Bowl losing teams have scored an average under 11 points (10.67 exactly), with a maximum of 16 points and a minimum of 3 points. 

There have been three different teams that won Super Bowls in the state of Georgia: Dallas Cowboys, New England Patriots, and St. Louis Rams. There have been three different teams that lost Super Bowls in the state of Georgia: Buffalo Bills, Los Angeles Rams, and Tennessee Titans.

# Arizona Super Bowls

<img width="594" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/2f6fa004-0621-45ab-bcf9-13ce8b2ebfb4">


There have been a total of four Super Bowls held in the state of Arizona. The summary statistics show that Super Bowl winning teams have scored an average of under 28 points (27.5 exactly), with a maximum of 38 points and a minimum of 17 points. Super Bowl losing teams have scored an average under 23 points (22.5 exactly), with a maximum of 35 points and a minimum of 14 points. 

There have been four different teams that won Super Bowls in the state of Arizona: Dallas Cowboys, Kansas City Chiefs, New England Patriots, and New York Giants. There have been four different teams that lost Super Bowls in the state of Georgia: New England Patriots, Philadelphia Eagles, Pittsburgh Steelers, and Seattle Seahawks.

# Louisiana Super Bowls

<img width="717" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/f6cf02d1-25f8-403b-8be4-999e59f876f8">


There have been a total of 10 Super Bowls held in the state of Louisiana. The summary statistics show that Super Bowl winning teams have scored an average of under 31 points (30.7 exactly), with a maximum of 55 points and a minimum of 16 points. Super Bowl losing teams have scored an average under 13 points (12.5 exactly), with a maximum of 31 points and a minimum of 3 points. 

<img width="1161" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/f0dcee57-b535-4914-921f-16fb1a145896">

The Dallas Cowboys have won two Super Bowls in the state of Louisiana. 

<img width="1160" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/9bf5cd6f-44d3-4385-8757-598c5a9bfa0a">

The Denver Broncos, Minnesota Vikings, and New England Patriots are all tied with two Super Bowl defeats in the state of Louisiana.

# Michigan Super Bowls

<img width="717" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/cd0ab76d-2245-460e-afa4-0807e7c473be">

There have been a total of two Super Bowls held in the state of Michigan. The summary statistics show that Super Bowl winning teams have scored an average of under 24 points (23.5 exactly), with a maximum of 26 points and a minimum of 21 points. Super Bowl losing teams have scored an average under 16 points (15.5 exactly), with a maximum of 21 points and a minimum of 10 points. 

The Pittsburgh Steelers and San Francisco 49ers are the only teams who have won a Super Bowl in Michigan. The Cincinnati Bengals and Seattle Seahawks are the only teams that have lost a Super Bowl in Michigan.

# Minnesota Super Bowls

<img width="717" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/27f42f02-e6d3-4e05-ba51-01f77269f2fc">

There have been a total of two Super Bowls held in the state of Minnesota. The summary statistics show that Super Bowl winning teams have scored an average of 39 points, with a maximum of 41 points and a minimum of 37 points. Super Bowl losing teams have scored an average under 29 points (28.5 exactly), with a maximum of 33 points and a minimum of 24 points. 

The Philadelphia Eagles and Washington Redskins (now known as the Washington Commanders) are the only teams who have won a Super Bowl in Minnesota. The Buffalo Bills and New England Patriots are the only teams that have lost a Super Bowl in Minnesota.

# Indiana Super Bowl

<img width="410" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/7f53a8fe-6cb1-413d-8574-83f6d0b0c9b1">


There has only been one Super Bowl that occurred in Indiana. The score was 21-17 with the New York Giants as the Super Bowl winner and New England Patriots as the Super Bowl loser.

# New Jersey Super Bowl

<img width="410" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/5abf18ea-0185-49da-a41b-d5d3fd8745ea">


There has only been one Super Bowl that occurred in New Jersey. The score was 43-8 with the Seattle Seahawks as the Super Bowl winner and Denver Broncos as the Super Bowl loser.

# Super Bowl Scores

Two different bar graphs were created to look at the number of points scored by Super Bowl winners and losers.

<img width="1143" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/1386c119-6091-42c1-849f-d785c807d5f7">


The bar graph above shows the Super Bowl winner scores from all 57 Super Bowls. The point scores have a 10 point break between each number (10-20, 20-30, 30-40, 40-50) with a 5 minute break in the middle of each 10 point break. From the graph, it's evident that most Super Bowl winners (16 teams) scored between 30-35 points to win their respective Super Bowl games. Two Super Bowl teams were able to win games with scores between 10-15 points and two Super Bowl teams were able to win games with scores between 50-55 points.

<img width="1143" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/c1c203de-1ff6-4e9e-8b0e-ea0b0f84b3e0">


The bar graph above shows the Super Bowl loser scores from all 57 Super Bowls. The point scores have a 10 point break between each number (10-20, 20-30, 30-40, 40-50) with a 5 minute break in the middle of each 10 point break. From the graph, it's evident that most Super Bowl losers (17 teams) scored between 5-10 points or 15-20 points to lose their respective Super Bowl games. Two Super Bowl teams lost games with scores between 0-5 points and four Super Bowl teams lost games with scores between 30-35 points.

# Super Bowl Winning Team Score Projections

A time series analysis was conducted to project the next 15 Super Bowl winning scores that teams could score between 2024-2038.

<img width="410" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/95a170a1-32e7-494d-9042-f918683c7cb2">


The picture above shows the next 15 Super Bowl victory points scored by teams in Super Bowls from 2024-2039. On average, winning teams will need to score under 30 points (29.19 exactly) to secure a Super Bowl victory. One team will score a maximum of 43 points during their Super Bowl victory and one team will only need to score 13 points to secure their Super Bowl victory.

<img width="1066" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/616b28a5-0429-4b7d-822a-6437b0de9f52">

The graph above shows the time series analysis for the next 15 Super Bowl winners between 2024-2038.

# Super Bowl Losing Team Score Projections

A time series analysis was conducted to project the next 15 Super Bowl losing scores that teams could score between 2024-2039.

<img width="376" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/3e1f1b80-3b9d-48ad-a590-d58088337b76">


The picture above shows the projected 15 Super Bowl points scored by losing teams in Super Bowls from 2024-2039. On average, losing teams will score under 20 points (19.81 exactly) to have a Super Bowl defeat. One team will score a maximum of 35 points during their Super Bowl loss and one team will score 3 points to secure their Super Bowl defeat.

<img width="1071" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/0bde881b-b04b-41a5-a7e3-89cc3dbc206e">


The graph above shows the time series analysis for the next 15 Super Bowl losers between 2024-2038.

# Super Bowl State Projections

A time series analysis was conducted to project the next 15 Super Bowl states that should host between 2024-2038. 

<img width="446" alt="image" src="https://github.com/reimerb13/NFL-Super-Bowl-Analysis/assets/79723505/4bdc2ad9-3c21-498d-bd46-abcaae73b071">

The next 15 Super Bowl states were projected. Arizona should host two Super Bowls, California should host two Super Bowls, Florida should host four Super Bowls, Georgia should host one Super Bowl, Indiana should host one Super Bowl, Louisiana should host one Super Bowl, Minnesota should host one Super Bowl, New Jersey should host one Super Bowl, and Texas should host two Super Bowls.

# Conclusions

Geographic location does play a role in Super Bowl scores. 








