# Fantasy Football Foresight
## Overview
- 1. Selected Topic: Predicting 2022 Fantasy Football Outcomes
- 2. Reasoning: All five members of our team are sports fans and we were deciding between predicting what cities would most likely receive a professional sports team in a hypothetical relocation and predicting future sports outcomes at a player level. Upon further review, we felt that predicting future performances at the player level had more ample data to train a model with and we could achieve more reliable data insights. Naturally, given the popularity of fantasy football we felt predicting 2022 NFL player outcomes would be both a fun and fulfilling project to jump into. Additionally, with the rise of mobile sports betting, we felt being able to create a model to accurately predict fantasy football outcomes could also be helpful in the sports betting decision making process. 
- 3. Source Data: Most, if not all, of our data will be providing through web scapes of Pro-Football-Reference, a website where statistics are presented in tabular form and have an easy to access API. 
- 4. Questions:
    - What variables carry the most weight in predicting a player's fantasy football performance?
    - Can a future season be predicted using a previous seasons statistics?
    - What will the final fantasy football rankings be for the 2022 season?

## Communication Protocols
- Square - John Clarke
- Triangle - Matt Barton
- Circle - Emery Hollar
- X - Barry Bingham and Brian Ernest

## Visualization
We will be using Tableau to visualize the story our data tells. So far we have a table showing the relationship between the predicted stats and the actual stats and a graph showing the difference in predicted vs. actual stats broken down by position. We will be adding a final graph showing what the model predicts for next year based on last year's stats.

We hope to use our class time efficiently to accomplish a lot of our team-oriented work given our conflicting schedules, but we stay in constant contact via slack

## Project Outline
### Tools Used
- We used Python, Pandas, Splinter, BeautfiulSoup, and ChromeDriver to scrap our data and prepare our datasets
- We used pgAdmin, Postgres, and the SQL language to create tables to be fed our datasets, and in turn, feed into an AWS database
- We used SKLearn and SQLAlchemy to create our models and feed in the data from our database directly into our model
- We used R Studio to create some initial visualizations
- We will use Tableau for our dashboard and storytelling with other visualizations

### Data Preprocessing
Our "Database" folder includes our jupyter notebooks with functions we created to scrape a number of pages on the Pro-Football-Reference website using an input year. We also have a function that combines our individual datasets into a database given a start and end year. 

During our initial preprocessing phase, we cleaned up the dataset to remove unnecessary characters, renamed our columns, and standardized certain columns on a per game basis. 

### Data Decisions
We needed 4 separate models for the 4 different football positions given difference in weight of certain statistics on certain positions. For example, passing and rushing stats were more heavily weighted for QBs and RBs, while targets and receptions were more heavily weight for WRs and TEs. With this in mind, we created a robust dataset that could then be sliced before being put into our models so we could gear each model to a specific position. 

### Training and Testing Data
We decided to use a decade worth of statistics and we split our model to train on 7 years of data (2012-2018), test on 2 (2018-2019), then test once again on 2019 data to see how the 2020 predicted outputs compared to the actual outputs. 

### Model Choice
We decided on a Linear Regression model given the continuous data inputs and outputs we were expecting. The limitation of this is not being able to use a more robust model like a neural network, which could find a greater number of connections within the data. However, given the non binary nature of the outputs we were expecting (points per game), a linear regression model made more sense.

### Dashboard Storyboard
We will begin with an explanation of how fantasy points are scored and the differences by position. We fill continue with a visualization showing predicted 2020 points per game plotted against the actual 2020 points per game. We will continue with a visualization showing the median error in our predictions, and finish with a interactive visualization that allows a user to filter by position and team on the projections for the 2022 season. 