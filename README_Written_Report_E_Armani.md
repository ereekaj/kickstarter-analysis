# Kickstarting with Excel

## Overview of Project
This project analyzed data from thousands of crowdfunding projects in Kickstarter. My client, Louise is interested in starting a theater crowdfunding campaign.  

### Purpose
The purpose of this project to is analyze the kickstarter data from the [Kickstarter_Challenge.xlsx](https://github.com/ereekaj/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx) document to compare different theater campaign outcomes based on their launch date and their campaign goals. This analysis will provide insights to my client to ensure success of her own theater campaign. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To start my analysis, I created a new column called "Years" and used the `YEAR()` function to extract the Year from the "Date Created Conversion" column. I then created the following pivot chart from the Kickstarter data using a filter based on the columns "Parent Category" and "Years". I used "Outcomes" for the columns and "Date Created Conversion" for the Rows to show the count of "outcomes" in the pivot chart.  
![Pivot Table](https://github.com/ereekaj/kickstarter-analysis/blob/main/Resources/PivotTable.png)

I then filtered the columns to only show "successful", "failed" and "canceled" campaigns. I also filtered the rows to show the results by month to get the pivot table contained in the document [Kickstarter_Challenge.xlsx](https://github.com/ereekaj/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx) under the "Theater Outcomes by Launch Date" tab. This pivot table was used to create a line graph below to visualize the relationship between the campaign outcomes and the month they were launched.
![Theater Outcomes Based on Launch Date](https://github.com/ereekaj/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png) 

### Analysis of Outcomes Based on Goals
I continued my analysis in the [Kickstarter_Challenge.xlsx](https://github.com/ereekaj/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx) document under the "Outcomes Based on Goals" tab by creating the following chart with new data. 
![Outcomes Data](https://github.com/ereekaj/kickstarter-analysis/blob/main/Resources/Outcomes%20data.png)
    
Under the "Goal" column, I created various dollar ranges to group the Goals into 12 rows from "Less than 1000" all the way up to "Greater than 50000". I then used the `COUNTIFS()` function on the "Outcomes" column in the Kickstarter tab to populate a count of plays that fit into each of the "Number Successful", "Number Failed", and "Number Canceled" columns in each row. I then calculated the sum of Total Projects and calculated the percentage of successful, failed and canceled projects for each row. Lastly, I created a line graph below to visualize this new data. 
![Outcomes Based on Goal](https://github.com/ereekaj/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)   

### Challenges and Difficulties Encountered
I did not encounter many challenges. I know excel pretty well and have worked with it in the past. I was a little rusty using it, but was able to get over that pretty quickly by going through the various exercises in BootCampSpot.  I did make a mistake analyzing the outcomes based on goals initially.  I first used the wrong column from kickstarter to make my calculations. I used the "Pledged" column instead of the "Goals" column. When my results and my line graph were way off from the example in the instructions, I re-evualated all of the inputs in the `COUNTIFS()` functions I used and discovered the error.  

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. Theater campaigns had the highest rates of success during the months of May, June and July. 
    2. Theater campaigns resulted in success more often than failure in all months. 

- What can you conclude about the Outcomes based on Goals?

The percentage of successful and failed plays does not go up or down consistently across the goal ranges.  It doesn't appear that the amount of the goal is an automatic predictor of success or failure based on this data. 

- What are some limitations of this dataset?

Fortunately, the dataset provided a large set of results for theater and play campaigns which were the type of campaigns I was evaluating.  For other campaigns like journalism or the subcategories like gadgets or restaurants, the data was very limited and may not provide good insights.

- What are some other possible tables and/or graphs that we could create?

We could use pivot tables to determine which types of campaigns had the highest percentage of successful, failed or canceled column and visualize it in line graph.  That may not be helpful for Louise but could be helpful for someone who wasn't sure what type of campaign they wanted to conduct. 
