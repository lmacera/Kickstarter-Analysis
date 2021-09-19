# Kickstarter Analysis 

## Overview and Purpose

Louise, a playwriter, asked our team to assist her in launching her new play *Fever*. With a budget of approximately $10,000, Louise would like assistance mirroring her
production off other successful productions in the U.S. Using a data set from Kickstarter, our team sorted, interpreted, and analyzed various Kickstarter projects to help Louise 
understand and visualize her possibilities of producing a successful play based on the launch dates and funding goals of other productions.

## Analysis 

Our analysis was based on a data set from Kickstarter that provided various data pulled from approximately 4000 Kickstarter projects ranging from theater productions, TV 
productions, food and restaurant creations, and technology startups. Our analysis researched the success, failure, and cancellation outcomes of Kickstarter plays based on launch 
dates and funding goals.

### Analysis of Outcomes Based on Launch Date

The analysis based on launch date took the Kickstarter data set and created a Pivot Table to show the count of each outcome (successful, failed, canceled, and live) and each 
count’s launch date month. The data was filtered to exclude live data outcomes and only include data for the theater category. Having put this data into a line 
graph, Theater_Outcomes_vs_Launch (shown below), we saw that most successful productions were launched in the summer months May-August and that the failure outcomes appeared to 
be steady throughout the year with a slight increase in October. The data also appeared to have successes decrease starting around September with December being the month in 
which failures and successes were almost equal and at their lowest point.
 
![Theater_Outcomes_vs_Launch](https://github.com/lmacera/Kickstarter-Analysis/blob/main/Resources(1)/Theater_Outcomes_vs_Launch.png )

![Theater_Outcomes_vs_Launch_Table](https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Theater_Outcomes_vs_Launch_%20Table.png )

As Louise is producing a play in the U.S. we took a deeper dive and sorted the launch date data by plays produced in the U.S. From the below graph and table, 
Theater_Outcomes_vs_Launch_US_Analysis and Theater_Outcomes_vs_Launch_US_Analysis_Table, we saw similar results showing May-August being the highest months of success. 
The failures were less steady and had peaks in February and some summer months, however, the number of success outcomes in the summer months are significantly higher than the 
number of failures in the summer months. Unlike the overall theater analysis, the U.S. play analysis showed failure outcomes were more than those of the successful outcomes in 
December.


![Theater_Outcomes_vs_Launch_US_Analysis]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Theater_Outcomes_vs_Launch_US_Analysis.png )

![Theater_Outcomes_vs_Launch_US_Analysis_table]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Theater_Outcomes_vs_Launch_US_Analysis_Table.png )

### Analysis of Outcomes Based on Goals

The analysis based on goals took the Kickstarter data set and created a *COUNTIFS* formula to pull the count of each Outcome, Successful, Failed, and Cancelled, based on various 
$5,000 intervals starting from $0 to $50,000. The counts for each category were totaled and each outcome was compared to its corresponding percentage of total production. The 
data was summarized in the below graph, Outcomes_vs_Goals, and table, Outcomes_vs_Goals_Table.  

![Outcomes_vs_Goals](https://github.com/lmacera/Kickstarter-Analysis/blob/main/Resources(1)/Outcomes_vs_Goals.png )

![Outcomes_vs_Goals_table]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Outcomes_vs_Goals_%20Table.png )


As the table and graph show, there was a slight negative correlation between the successful outcomes and the goal amounts, and a slight positive correlation
between the failed outcomes and the goal amounts. In other words, as the goal amounts went up the successful outcomes went down, and failed outcomes went up. 
There was an inconsistency in which this correlation was not presented, as the goal range of $35,000 to $40,000 had an increase in successful outcomes and a decrease 
in failure outcomes. This slight deviation could be from outliers being in the data. As such, using the measures of central tendency, Mean, Median, quarterlies, and the 
Interquartile Range, it was determined that any goal amount above $10,700 would be considered an outlier. By removing all values over the $10,700 limit our analysis 
showed a clearer negative correlation between the successful outcomes and a positive correlation between the failed outcomes.

![Outcomes_vs_Goals without outliers]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Outcomes_vs_Goals%20without%20outliers.png )

 
### Challenges and Difficulties Encountered

While analyzing there were a few issues sorting and filtering the data appropriately and outliers that skewed results. With filtering and sorting data, 
the filter did not expand to ensure the proper data stayed with its assigned project ID and corresponding information. To fix this the original data was copied over 
to the correct ID and all formulas were checked to ensure they were still working properly. As discussed under the Analysis of Outcomes Based on Goals section there was a 
challenge in interpreting the data presented because some outliers were throwing off the ranges between $35,000 and $45,000. Using statistical measures of central tendency, the
outliers were removed, and the analysis was based on the remaining data set.

## Results

### Outcomes based on Launch Date

Based on the above Launch Date Analysis, Louise’s highest possibility of success would be to launch *Fever* during May or June. From the above analysis and the below tables, we 
can see that the summer months of May-August have the highest number of successes. Though May-August appears to have a high count of successes, May and June have the highest 
number of successes for both the overall launch data analysis and the U.S. plays launch date analysis.

With regards to times not to launch, both the overall launch data analysis and the U.S. plays launch date analysis show the highest probability of failing to be launch dates in 
November and December. The above Launch Date Analysis shows a decrease in successful production after August with the lowest number of successes, and an almost equal number of 
failures, being in December.

###Outcomes based on Goals

Based on the above goal analysis, Louise’s highest possibility of success would be for a goal of under $15,000. As Louise set a funding goal of $10,000 and is close to reaching 
that goal, Louise will have the best possibility of success if she sticks to a $10,000 or less funding goal.

## Data Set limitations

A few data limitations with this data set were if the data set was a fair representation of the population and if we were working with “clean data”

### Data Representation

Our data set may not be big enough to accurately represent the U.S. play population. As Louise is looking to produce a play we wanted to look mainly at the theater and play
outcomes from the data set of approximately 4000 Kickstarter. Per the below, Total Theater Table and Total Plays Table, we can see the theater productions only represent about 
one-third of our total population, and play productions represent about 25%. Furthermore, as Louise is looking to produce her play in the U.S., the U.S. play sample represents 
only 16% of our total population, shown in the Total U.S. Plays table below.

![Total Theater Table]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Total%20Theater%20Table.PNG )

![Total Plays Table]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Total%20Plays%20Table.PNG )

![Total US Plays Table]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Total%20US%20Plays%20Table.PNG )

### Clean Data

Having pulled the Kickstarter data from the Kickstarter database we cannot control the quality of our data. After a high-level review of the data, we had to clean the data to 
get the proper launch and deadline dates to pull correctly and saw through our outcomes based on goals analysis the data contained outliers. Additionally, our total data set 
has launch dates between 2009-2017, however, or play dates were clustered between the 3 years of 2014-2016, as shown below in the Data set Dates table.

![Data set Dates]( https://github.com/lmacera/Kickstarter-Analysis/blob/main/Secondary%20Resources/Dataset%20Dates.PNG )

	
## Additional Measures

From this data set, there are several other measures we could’ve based our analysis on. Other measures that could have been useful for Louise would be measuring the outcomes 
based on percentage funded as well as outcomes based on different countries. 

