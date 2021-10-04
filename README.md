# Kickstarting with Excel

## Overview of Project

An analysis on theater kickstarter campaign data was performed to uncover trends based on launch dates and funding goals.

### Purpose

Theater campaign data was analyzed to trend successful, failed, and canceled campaigns in relation to the month of their launch date.  The plays subcategory was analyzed to trend the percentage of successful, failed, and canceled play campaigns based on their funding goals.  These trends may help theater campaigns to appropriately align their launch dates and funding goals.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

A pivot table was created to filter data by the theater category and by the month of their launch dates, count the outcomes by successful, failed, and canceled campaigns, and plot the outcomes on a line chart.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/90982811/135784309-59f08d58-5dd2-4851-94ee-b49fd8a16a8c.png)

### Analysis of Outcomes Based on Goals

The COUNTIFS() function was used to categorize play data by funding goal increments, starting with funding goals of $1,000 or less, $1,000 to $4,999, then by $5,000 increments up to $49,999 with the maximum category of $50,000 and Greater.  The COUNTIFS() function was used to break these increments into failed, successful, and canceled play campaigns.  

Example code:  =COUNTIFS(Kickstarter!$D:$D, ">=1000",Kickstarter!$F:$F, "successful", Kickstarter!$O:$O, "plays",Kickstarter!$D:$D, "<=4999")

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/90982811/135784341-fb9a76c6-15f7-481c-8492-ce03707e4e77.png)

### Challenges and Difficulties Encountered

It is challenging to generalize outcomes based on the number of successful launch dates because the months with the most successful campaigns were also the same months with the most campaigns launched.  Similarly, the dollar ranges that hold the percentage of the most successful play campaigns based on funding goals were also the same ranges with the most campaigns.

## Results

Theater launch dates in May and June returned the most successful campaigns.  July and October returned the most campaigns that failed.  December's failure rate was the highest with 35 of 75 campaigns failing for a 47% failure rate.

Play campaigns with funding goals of less than $5,000 had the highest success rates.  Campaigns with funding goals between $35,000 to $45,000 also had a high success rate but did not have a significant amount of campaigns in this funding range.  Play campaigns with funding goals of $45,000 and greater had the highest failure rate.  

Other factors that may have contributed to the failure or cancellation of a project were not given, so the dataset is limited to making inferences based on launch dates and funding goals. 

Additional tables and graphs could be created to trend data based on pledged amounts and the length of the funding campaigns.
