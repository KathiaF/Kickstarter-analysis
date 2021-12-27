# Kickstarter-analysis
# Kickstarting with Excel

## Overview of Project
Kickstarter is an online crowdfunding platform for launching creative projects and in this activity examines Kickstarter campaigns from 2009 to 2017 and aims to uncover trends related to theater projects to help Louise launch a successful campaign.

### Purpose
The purpose of this project is to help Louise launch a Kickstarter campaign to found her play *Fever*, through the analysis of the *Kickstarter* database which shows the project's campaigns that have resulted in success, failure or have been canceled, using excel to analyze and understand real world campaigns (specifically theater projects) from start to finish by visualizing the relationship of launch dates and their funding goals. Our goal is to be able to set her campaign to mirror other successful ones in the same category and help her to start her production.

gain insights on how different campaigns, specific to plays, fared in relation to their launch dates and their funding goals.
# kickstarter-analysis
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
The focus of this analysis is to visualize campaign outcomes ("successful," "failed," and "canceled") based on launch date. In order to do this, the following steps needed to be taken prior to conducting the analysis:
1. Create a new column: 
   - Name the first cell as *Years*
   - Use the **YEAR()** function to extract the year from the *Date Created Conversion* column.
   <img src="/Images/img1.png" width="50%" height="50%">
   
2. Create a pivot and place the pivot table in a new sheet and label it: *Theater Outcomes by Launch Date*.
   - Fields
     - Filters: Parent Category and Years
     - Columns: outcomes
     - Rows: Data Created Category
     - Values: Count of outcomes
   - Filter the column labels to show only "successful," "failed," and "canceled." and sort the campaign outcomes in descending order so "successful" is first.
   - Filter the *Parent Category* to show only the data for **theater**.
   <img src="/Images/img2.png" width="50%" height="50%">

3. Create a pivotChart
   - Create a line chart to visualize the relationship between outcomes and launch month.
   - Save the chart as *Theater_Outcomes_vs_Launch.png*.
   <img src="/Images/img3.png" width="50%" height="50%">
   
 4. Analysis outcome
   <img src="/Resources/Outcomes_vs_Goals.png" width="50%" height="50%">
  
   
 ### Analysis of Outcomes Based on Goals
 Visualize the percentage of successful, failed, and canceled plays based on the funding goal amount
 1. Create a new sheet and label it *Outcomes Based on Goals*
    - Add the following columns:
      - *Goal*, *Number Successful*, *Number Failed*, *Number Canceled*, *Total Projects*, *Percentage Successful*, *Percentage Failed*, *Percentage Canceled*.
    - Create dollar-amount ranges so projects can be grouped based on their goal amount.
    - Use **COUNTIFS()** functions in the columns: *Number Successful*, *Number Failed* and *Number Canceled* 
    - <img src="/Images/img4.png" width="50%" height="50%">
    - Use the **SUM()** function in the column *Total Projects* with the *Number Successful*, *Number Failed* and *Number Canceled* columns and get the percentage of successful, failed, and canceled projects for each row
    <img src="/Images/img5.png" width="50%" height="50%">
 2. Create a line chart to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled projects.
    - Chart elements:
      - Chart title: *Outcomes Based on Goal*
      - x-axis: goal-amount ranges
      - y-axis: percentage of successful, failed, or canceled projects.
    - Save the chart as *Outcomes_vs_Goals.png*.
    <img src="/Images/img6.png" width="50%" height="50%">
    
 3. Analysis outcome
   <img src="/Resources/Theater_Outcomes_vs_Launch.png" width="50%" height="50%">

### Challenges and Difficulties Encountered
The main challenge I had while doing this activity was time management. The activity is well explained and is guided in a simple way through module 1 and although I had no problems developing the activity in Excel, some possible difficulties could perhaps be creating the pivot tables correctly or the correct use of the **COUNTIFS()** function and its attributes. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  1. It looks like about 61% of all Kickstarter projects get successfully funded by the deadline and the best months to launch a campaign are May and June, as the campaigns that were launched in those months resulted in 68% and 65% success respectively. And the worst month to launch a campaign is December as 47% of campaigns tend to fail.
  2. It is observed that during the period from 2009 to 2015, 47% of the campaigns that were launched during October failed, however, historically none of the campaigns were canceled. 

- What can you conclude about the Outcomes based on Goals?
  - The biggest factor in having a successful campaing project is the funding goal. The lower the budget requested for financing the campaign for the project, the greater the probability of success. Campaigns that request a fundraiser greater than $50,000 are more likely to fail or be canceled.

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?

