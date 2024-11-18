# NBA Fantasy Draft Tool - PowerBI

### Dashboard Link :https://app.powerbi.com/view?r=eyJrIjoiZTUyZmRmMDktYmU5OC00YWJmLWIxZmMtOGE5ZDFjNTI1NDUzIiwidCI6ImI1MmJlNDcxLWY3ZjEtNDdiNC1hODc5LTBjNzk5YmI1M2RiNSIsImMiOjZ9&pageName=ReportSection33f1e9a18d0687ee0e36
## Problem Statement

This dashboard helps the user understand the fantasy value of a player. It helps the user know if they are selecting the most valuable point getter based on their draft position and the risk associated. Through different ratings, they get to know their players risk before they select them in the draft, & thus they can improve their ability to score points week to week and produce wins. It also lets them know the volatiltiy in a players game scoring, thus by using this dashboard they are able to see the consitstency of players and can focus on building a sustainable team over the course of the season and produce more wins.

Since, the number of available good starting players accross the five postions is not even, the user must draft the less available position stars first before going towards the best player at a more available position. 

Also since injuries are a factor that can affect winning opportunity, the user can factor in less risky options during the course of the draft.


### Steps followed 

Steps:

Step 1: Data Collection

Downloaded two CSV files containing NBA seasonal statistics from BasketballReference.com.

Step 2: Database Preparation

Created two blank tables in SQL Server Management Studio (SSMS), ensuring column structures matched the CSV files.
Imported the data from the CSV files into these SQL tables.

Step 3: Data Integration

Wrote SQL queries to merge the two datasets, using the player name as the primary key for joining.

Step 4: Fantasy Points Calculation

Incorporated custom fantasy league point calculations into the merged dataset:
1 NBA point = 0.6 fantasy points
1 rebound = 0.75 fantasy points
1 block or steal = 2 fantasy points
1 assist = 1 fantasy point
1 three-point shot = 0.5 bonus points

Step 5: Data Connection to Power BI

Connected the SQL query to a Power BI desktop file using the Direct Import method.


Step 6: Data Visualization
Created a variety of visualizations in Power BI:
Line Graphs: Displaying player performance trends over the season.
Scatter Plots: Comparing fantasy points per game with games played.
Position Group Analysis: Grouped players by position to determine which groups play the most games and score the highest fantasy points.

Step 7: Filters and Slicers

Added dynamic filters and slicers in Power BI to allow users to view specific data points, such as:
Player statistics by position
Fantasy points trends by team
Seasonal performance within a custom date range

Step 8: Efficiency and Value Analysis

Analyzed player efficiency to identify potential high-value players who could excel with increased playing time.
Measured the number of star players at each position to assess positional scarcity.

Step 9: Insights for Fantasy Drafts

Determined the relative value of players by position, e.g., centers being more valuable than point guards due to positional scarcity.
Provided actionable insights to guide player selection in fantasy drafts.
           
 
        
 
 Step 10 : The report was then published to Power BI Service.
 


# Insights

A multi-page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Fantasy Output by Position 

   Average PPG for PG  = 21.29 

   Average PPG for SG  = 19.46 

   Average PPG for SF  = 20.91 

   Average PPG for PF  = 19.76 

   Average PPG for C  = 20.54


thus, the most points generate from PGs.
           
### [2] Lesser known players that Produce

 Least injury prone and highest output players were Domantas Sabonis and Nikola Jokic


  ### [3] Players affect on winning 
  
Players in sitatuions where their play doesn't affect winning adds risk due to potential lineup shifts

 ### [4] Some other insights
 
 ### Durability
 
 1.1) PLayers on the left side of the chart are the ones to avoid while players on the right side are the ones who have a higher usage(Touch the ball)
 
 1.2) Dark blue dots represent players with littl to no injury history
 
 1.3) Gren dots reperesent players with high probability to miss games.
 
thus, the dot furthest to the top right and with a dark blue color is the ideal selection.
 
