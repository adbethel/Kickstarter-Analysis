# An Analysis of Kickstarter Campaigns
Performing analysis on kickstarter data to uncover trends.



                                               Deliverable 3: Written Analysis


Project Overview

  The purpose of this this analysis is to is to examine, in depth, the fundraising outcomes based on the goals set by Louise the playwright, who is interested in fundraising her play, Fever. Using the Kickstarter dataset, the analysis organized the theatre fundraisers into different categories based on success, failure,and cancellation of each campaign. The dataset also documented the outcomes of the fundraisers based on their goal and launch date. 

  The goal was to consolidate the findings into a visually appealing and understandable dataset that could be explained clearly to the client, Louise, who is not an expert in data analysis. Louise would be able to easily see the trends in fundraising, including the time of year that a fundraiser would be most profitable, as well as the percentage of successful, canceled and failed outcomes for fundraisers for plays, so that she would be able to calculate the probability  of success based on historical data.
 
 
Project Analysis


  Theater Outcomes Based on Goals: 
  Using the Kickstarter dataset the subcategory column was filterec to display "Plays”, and a table was created on the "Theatre Outcome Based onn Goals" sheet. The table was first stratified by Goal" amount, and then the following columns were orgnaized to display the number and percentage of successful, failed and cancelled plays, and total projects. Using the Kickstarter as the reference page, the following code was created to pull the number of successful plays based on the row number and the goal value of the row: =COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!D:$D,"<=4999",Kickstarter!$F:$F,"Successful",Kickstarter!$O:$O,"Plays"). 

  To pull the data from the Kickstarter sheet, the "COUNTIFS" function was used to instruct excel to count the cells, followed by  the code “Kickstarter!”, instructing excel to pull from the sheet as named, and followed by "$D:$D", telling excel to pull the goal data from the entire row “D”.  For each row, the range of the fundraiser dollar amount was changed in the code to adjust for the selected parameters: Kickstarter!$D:$D,">=1000",Kickstarter!D:$D,"<=4999". In this example, the code is instructing to pull for fundraisers between the goal of $1000.00 to $4999.00. To pull the data for "Successful", “Failed” or “Canceled” plays in the outcome column in the Kickstarter, I substituted the code with “Kickstarter!$F:$F,”Successful”, “Kickstarter!$F:$F,”Canceled” or  “Kickstarter!$F:$F,”Failed”. I instructed excel to pull the code from the entire “F” column by coding “$F:$F”. Finally, to select “Plays” from the subcategory column, I selected the full column “O” by coding”$O:$O” and included in the code: Kickstarter!$O:$O,"Plays".  

  To create an image to consolidate this data, I created a line chart using the chart design tab. I instructed excel to create a chart based on the percentage of failed, successful and cancelled goal outcomes.   

 ![Outcomes_vs_Goal](https://user-images.githubusercontent.com/112285856/187814112-1e4dcb3b-5d77-48a0-a137-26eef95d6d6c.png)
 
 
 
 
 
  Theatre Outcomes Based on Launch Date:
  Using the Kickstarter datasheet, I created a Pivot Table displaying the number of Successful, Failed, and Cancelled fundraisers based on their initial launch dates during the month of the year the fundraiser was launched. This table was also stratified by month, to show the outcomes of the fundraiser during each month of the year.  Using the data on the pivot table a line chart was inserted depicting the Successful, Failed, and Cancelled theatre outcomes during on the months of the year. 
  
![Theatre_Outcomes_vs_Launch](https://user-images.githubusercontent.com/112285856/187814141-33871939-ce8a-4ec7-a7de-48be421f07f8.png)




  Challenges:
    There were two main challenges encountered while modifying the dataset. The first was when creating the pivot table to display the months of the year in the rows in words, rather than the month number. Initially, the row showed each individual date from the “date created conversion” column in the Kickstarter sheet, instead of just the month. To change this, I created a new column  in “U” that showed only the year by using the code =YEAR(S2), and in the “V” column I used the code  =TEXT(S2,"mmmm") to convert the month date from the number to the word.  

Another area of challenge was finding the code for the number of successful, failed and cancelled plays in the “Outcomes Based on Goals” sheet. The initial code written produced zeros in the >50000 column for the successful, failed and cancelled outcomes. I combed through the code to see that I had used the wrong greater than/less than sign in the code. By reading through what I wrote and making sense of the code I was able to find where my mistake was and correct it. 


Project Results

  Conclusions Based on Theatre Launch Date Outcomes:
  We can conclude that the Theatre Outcomes by Launch Date has the highest success rate during the months of May and June. We can also conclude that there doesn’t seem to be a particular spike in failure during any specific month in the same way the early summer brings noticable success.  

  Conclusions Based on Goal Outcomes:
  We can conclude that highest number of successful plays are those with the goal fundraisers of less than $9999.00. Additionally, the higher fundraiser goals saw highest rates of failure, some as high as 100%.

  Other Possible Graphs:
  We could create a line graph showing the "goal vs actual pledged" amount of the plays or a pivot table depicting the number of backers in comparison to the goal and actual outcome amount.  
