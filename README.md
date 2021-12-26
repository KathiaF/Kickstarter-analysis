# Kickstarter-analysis
# Kickstarting with Excel

## Overview of Project

### Purpose
Help Louis with her project campaign to found her play *Fever*, through the analysis of the *Kickstarter* database which shows the project's campaigns that have resulted in success, failure or have been canceled, using excel to analyze and understand real world campaigns from start to finish through visualization. Our goal is to be able to set her campaign to mirror other successful ones in the same category and help her to start her production.

# kickstarter-analysis
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Visualize campaign outcomes ("successful," "failed," and "canceled") based on launch date.
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
   
   
 ### Analysis of Outcomes Based on Goals
 Visualize the percentage of successful, failed, and canceled plays based on the funding goal amount
 1. Create a new sheet and label it *Outcomes Based on Goals*
    - Add the following columns:
      - *Goal*, *Number Successful*, *Number Failed*, *Number Canceled*, *Total Projects*, *Percentage Successful*, *Percentage Failed*, *Percentage Canceled*.
    - Create dollar-amount ranges so projects can be grouped based on their goal amount.
    - Use **COUNTIFS()** functions in the columns: *Number Successful*, *Number Failed* and *Number Canceled* 
    - <img src="/Images/img4.png" width="50%" height="50%">
    - Use the **SUM()** function in the column *Total Projects* with the *Number Successful*, *Number Failed* and *Number Canceled* columns and get the percentage of successful, failed, and canceled projects for each row
    - <img src="/Images/img5.png" width="50%" height="50%">
