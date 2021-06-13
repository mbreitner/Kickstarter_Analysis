# Kickstarting With Excel
Columbia Bootcamp Module 1 Kickstarter Analysis

## Overview of Project
The project is to use excel formulas, pivot tables, and visualization techniques to analyze a large data set of information pertaining to kickstarter campaigns. 

### Purpose
The purpose of this analysis is to identify how other kickstarter campaigns, similar to her goal of putting on a play, were succussful in reaching their end goals. Through the use of analyzing other Kickstarter campaigns quickly in excel, we can help Louise make strategic data driven decisions to help her reach her short term fundraising goal for her play Fever. Excel gives us the ability to drive insights out of a large datatset and create simple visualizations that best display the data in a way Louise can make a quick decision on how to continue proceeding to reach her goal. 

## Analysis & Challenges

### Analysis of Outcomes based on Launch Date
First, in the outcomes based on goals section, we wanted to identify the total # of outcomes (successful, failed, or canceled) in the theater category overall and if there were any monthly trends we could showcase. To do this, I created a pivot table, which can be found in the "Theater Outcomes by Launch Date". [Kickstarter_Challenge Final.xlsx](https://github.com/mbreitner/Kickstarter_Analysis/files/6644461/Kickstarter_Challenge.Final.xlsx)
The pivot table is set in the following format: I added the parent category and the year of date creation to the filters. Then, I added the outcomes to the columns and the values section. I made sure the values section was selected to Count of Outcomes so we could see the total number for each outcome value. Next, I put the years into the rows section of the pivot table. To change the row values from years into months, I selected the data in the rows within Column A, went to PivotTable Analyze > Grouping > Months. This changed the valuse in Column A to months instead of years. Lastly, I selected the full data set and created a line chart to easily visualize any month over month trends based on the outcomes. ![Theater_Outcomes_vs_Launch_](https://user-images.githubusercontent.com/84791455/121819079-0fcd0600-cc40-11eb-882e-e0faa97eff37.png)
  
### **Analysis of Outcomes Based on Goals**
Second, in the outcomes based on goals section, I used a countifs function to find the total amount of successful, failed, or canceled campaigns in the large data set. I had to figure out how to write multiple statements within one countifs formula to make sure I could get the range that was required. [Kickstarter_Challenge Final.xlsx](path/to/Kickstarter_Challenge Final.xlxs) For example, the formula that I used to get the data within a range, to get the outcome, and ensure it only came from the plays subcategory was as follows: =COUNTIFS(Kickstarter!D:D,">=20000",Kickstarter!D:D,"<=24999",Kickstarter!F:F,"Failed",Kickstater!R:R,"plays"). Then, I used the =SUM() formula to get the total # of projects across all outcome types in the goal range. Then to find the % of each outcome, I divided the the total # of outcome per goal range by the total # of projects per goal range. To finish the analysis, I selected the entire data set in my new table, inserted it into a line graph , then selected the data to only include the goal ranges and %'s of each outcome. I gave the chart a name and saved it.
  ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/84791455/121819070-0a6fbb80-cc40-11eb-95e8-7f955aea10ec.png)


### Challenges and Difficulties Encountered
The challeneges I encountered were specifically in writing the countifs function. I had to make sure my syntax was correct a couple of times so the formula could run properly. I also needed assistance when grouping the years into months to have my pivot table sorted by month instead of year. I used my google-fu techniques and the hints included in BCS to help me solve the porblems. 

## Results
  - **What are two conclusions you can draw about the Outcomes based on Launch Date?**
  1. May & June are the months with the most amout of successful theater launched. The start of the summer is likely the best time to launch a theater. 
  2. September - December had least amount of successful campaigns. The end of the year will likely have the least amount of success when launching a theater. 
  
  -** What can you conclude about the Outcomes based on Goals?**
  1. The vast majority of successful campaigns happen when the fundraising goal is less the $10,000.
  2. Fundraising goals greater the 50,000 have an 88% chance of failure
  
  - **What are some limitations of this dataset?**
  1. Diferent currencies are not identified in the goals column, it is all listed in US dollars 
  2. The deadline and launched at columns had to be restructured to show the correct values
  
  - **What are some other possible tables and/or graphs we could create?**
  1. We could identify how many donors there were for each campaign within each goal range and create a line chart to see how many donors would be needed in each price range on average. 
  2. We could create a pie chart for each outcome value and filter the chart by subcategory. 
  3. We could pivot the data by country of origin, outcome, & month to identify if the specific regions have different month over month trends. 
