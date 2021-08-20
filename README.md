[Written_Report_Template.md](https://github.com/jasonyoo0508/Kickstarter-analysis/files/7008932/Written_Report_Template.md)
# Kickstarter-analysis
performing analysis on Kickstarter

## Overview of Project
The purpose of this analysis is to visualize campaign outcomes based on their launch dates and their funding goals for "plays" subcategory.
The latter part of the project is to create a visual image of the percetange of successful, failed. and canceled plays based on the funding goal amount. 

## Analysis and Challenges

### Theater outcomes based on Launch Date Analysis 

In order to review the campaign outcomes, one should categorize and organize the outcome of the parent category, which is 'theater' for the analysis. 
We would get the total outcomes for successful, failed, and canceled outcomes for all theater parent category based on the launch date (month)
In order to obtain the launch date (month), one would refer to the 'launched_at' (Cell J2) and implement the formula: (((J2/60)/60)/24)+DATE(1970,1,1) to obtain the timestamp. (DD-MM-YYYY)
One can indicate the months in 3 digit letters by using the formula: TEXT(S2*29,"mmm"). In this instance, 
![excel table_1](https://user-images.githubusercontent.com/89154507/130298731-2ea50497-2425-44e1-a375-4f999f7ba8da.png)

Create the pivot table based on the excel file by visiting Insert->Pivot table in a new sheet. 
Filters: Parent Category, Years
Columns: Outcomes
Rows: Months
Values: Outcomes
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/89154507/130299351-5062f7f7-b614-414c-9edc-7eec0367ca2b.png)

**In parent category of 'theater', there are more successful outcomes if the plays are launched in between Q1, and Q2 but the plays tend to be less successful when it gears towards Q3 and Q4. 
The overall fail/unsuccessful plays or the cancelled plays for the theater are mostly happening on end of the year. They should focus adjusting the launch date to Q1 and Q2 for successful outcomes.**

With the information above, one would create new sheet in excel to visualize percentage of successful, failed, and canceled plays based on funding goal amount.

After creating 12 dollar amount ranges, use the COUNTIFS() function to obtain numbers for the 3 different outcomes.
In order to obtain the percentages, divide the value of the outcome to the Total number of projects.

![Projects   Percentages](https://user-images.githubusercontent.com/89154507/130299591-9b96d890-3ead-4820-bc78-c9a2cce0cf4e.png)

After getting the figures, create line chart with x axis indicating the dollar ranges, and y axis indicating the outcome percentages. 

**The outcomes are likely to fail in the 'plays' subcategory if the goal amount are greater than $40,000. In the otherhand, the outcomes are more successful if the overall goal amount has a value over $40,000.**

### Possible challenges  

Although the data has a solid conclusion based on the linechart, one may have to consider the cash availability for the fundraising project. People tend to spend or donate more money when they have cash, and there should be a surge in the cash activity during April~June period as tax income payments are distributed to people. Also, based on the Goal dollar amount, it shows people tend to be more successful if the total fundraising amount is less than $25,000. 


## Results

### Conclusion - Theater Outcomes by Launch Date
In parent category of 'theater', there are more successful outcomes if the plays are launched inbetween Q1, and Q2 but the plays tend to be less successful when it gears towards Q3 and Q4. 
The overall fail/unsuccessful plays or the cancelled plays for the theater are mostly happening on end of the year. They should focus adjusting the launch date to Q1 and Q2 for successful outcomes.

### Conclusion 
The outcomes are likely to fail in the 'plays' subcategory if the goal amount are greater than $40,000. In the otherhand, the outcomes are more successful if the overall goal amount has a value over $40,000.

### Minor limitations on the dataset
It would be helpful to obtain the demographics of the target audience and to consider the currency as donations are considered gift, and the dollar amount may vastly vary based on the currency. 

