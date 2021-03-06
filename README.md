# Kickstarter-analysis

## Overview of project

  The purpose and background was to help Louise find out more about the successes and failures of different Kickstarter campaigns based off their launch dates and their funding goals. We used Kickstarter data that dated back to 2009 and from various countries as well as various goals in many different categories and subcategories to see what Louise could do to make her campaign as successful as possible. 
  
## Analysis and Challenges

### Analysis
  
  There were two categories that we were mainly trying to figure out for Louise's situation. One was outcomes based on financial goal set by the kickstarters. Second was finding out what the theater outcomes would be based on the launch date of the campaign.
    
  For the first analysis, we took incremental ranges of set financial goals (starting at less than 1000, greater than 50000, and then increments of 4000 inbetween - shown below) from the campaigners. With those increments in mind, we analyzed the number of successful, failed, and canceled campaigns. Additionally, filtered the data by analyzing campaigns based mainly on the subcategory of "plays" as that is what Louise is most interested in and was the most pertenent to her campaign.
  
 ![image](https://user-images.githubusercontent.com/75653952/102957258-9a0d8c00-449f-11eb-9cea-ff54c01e1c75.png) 
    
  The code in which we did this was a 'COUNTIFS' function that included the financial goal range, the outcome situation, and the "plays" subcategory (shown below). We then created a chart based off the percentage of total projects in the goal range. This visual of the percentage difference between successful, failed, and canceled campaigns helps us determine which incremental goal ranges make the most sense to choose to have a more successful outcome. 
  
 ![image](https://user-images.githubusercontent.com/75653952/102956102-24082580-449d-11eb-9daf-b4b68a496d8c.png) 
    
  For the second anaylsis, we were trying to figure out when the best time to post a new campaign would be for the "theater" parent category. In order to get this to work properly, we had to first convert the 'deadline' and 'launched_at' columns in unix format to short date format (shown below).
  
![image](https://user-images.githubusercontent.com/75653952/102957306-b7425a80-449f-11eb-83b0-de144396f809.png)  
  
  We then separated the year from the shortdate in the next column. We then created a pivot table to then deduce the count of how many successful, failed, and canceled outcomes there were per month per the theater category. We then charted this to create a visual to display which months would be best to launch a new campaign and which months to avoid (shown below).
  
 ![image](https://user-images.githubusercontent.com/75653952/102957339-cf19de80-449f-11eb-9699-9a4ba306f402.png) 
    
### Challenges
  
  The main challenge we had was writing an CountIF function that included all the parameters of the goal range was well as the subcategory range. Figuring out how to structure the code to include the goal range took some time to figure out and then also that I had to include plays in the equation, not knowing it couldn't be filtered out manually.
    
## Results

### Theater Outcome by Launch Date Conclusions
  
  Two conclusions we can make about Theater Outcomes by Launch Date are: 1) the best time to launch a campaign would be in May or June and, 2) the worst time to launch a campaign would be May or October.
    
    
  A Conclusion that we can make about Outcomes Based on Goals would be that the most successful campaigns are those with financial goals of less than 1000 to 4999 as well as 35000 to 44999.
    
### Limitations
  
  The limitations of this dataset is the limited number of datapoints in both categories, subcategories, countries, and time in years. This is a small sample size compared to the population of total campaigns.
    
### Additional Tables/Graphs
  
  Other information that we could have provided or used would be utilizing the average donation column as well as the backers count column. We could have used this data to figure out which parent categories and and subcategories ended up with the most/least amount of backers as well as what the average donation would be per category and number of backers.
