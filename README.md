# Kickstarting with Excel

## Overview of Project

### Purpose
This project is to help Louise, a play wrighter who wants to start a crowdfunding for her play *Fever*, to gain the insights into crowdfunding data, which in this case, is the Kickstarter dataset.
After getting close to her play *Fever* fundraising goal, Louise now needs help to find out how different campaigns fared in relation to their launch dates and their funding goal.
Using the given Kickstarter dataset, we visualize campaign outcomes based on their launch dates and their funding goals and analyzes the outcomes to give Louise her answer.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
* To visualize campaign outcomes based on their launch dates, we first extract the launch years of all campains from their launch dates using Excel YEAR() function.
* We then create a pivot table to show the outcomes of the successful, failed, and canceled campaigns by months for each parent category and year.
* Since Louise is only interested the "Theater" category, we filter our pivot table by "Parent Category" to show only outcomes for "Theater".
* Since we are more interested the successful campaigns, which take the highest percentage in all outcomes for "Theater", we sort the outcomes in descending order so that "successful" is the first column.
* The last step for this part is to create a chart to visulize the data in our pivot table. Since the outcomes are tracked over a period of time, line chart would be the best option to use.
* This is what our "Theater Outcomes based on Launch Dates" line chart looks like:
!["Theater Outcomes based on Launch Dates" Line Chart](https://github.com/nhipqnguyen/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)
	
### Analysis of Outcomes Based on Goals
* To visualize campaign outcomes based on goals, we first divide all campaigns in the "plays" subcategory, which is the subcategory that Louise is most interested in, into different groups based on their goal ranges.
* We then use Excel formula COUNTIFS() to count the number of successful, failed, and canceled campaigns in the "plays" subcategory for each range.
* Next, we calculate the percentage of successful, failed, and canceled campaigns for each range.
* The final step is to plot the percentages of each outcome for each range into a line chart:
!["Plays Outcomes based on Goals" Line Chart](https://github.com/nhipqnguyen/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)  

### Challenges and Difficulties Encountered
* When the pivot table for outcomes based on launch date was first created, the row labels were an unwieldy list of dates, months, and years. Therefore, the Group function was used to show just the months of the year.
* For Excel formula COUNTIFS(), each criteria range can only have 1 criteria at a time, making the formula lengthy which can possibly lead to syntax errors.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  * The month that launched the most successful theater campaigns was May, followed by June. However, May and June along with October also launched the most failed campaigns.
  * While in May and June, there were more than twice as many failed campaigns as successful ones, the number of failed campaigns in October was roughly three quarters of the number of successful ones. Therefore, May seems to be the best month to launch a theather project crowdfunding.

- What can you conclude about the Outcomes based on Goals?

  Based on the chart, projects with goals from less than $1,000 to $4,999 and from $35,000 to $44,999 had the highest success rates. However, if we look at the data table, there were only 9 projects in the $35,000 - $44,999 range compared to 720 projects in the less than $1,000 - $4,999 range. Therefore, there will be a higher chance that Louise's project is successful if its goal is less than $5,000.

- What are some limitations of this dataset?

  * This dataset only contains data up to 2017 while Louise's campaign takes place in 2021, which means it could miss more recent trends in crowdfunding.
  * This dataset could possibly miss important parameters of the campaigns. Types of advertising could be one of them.

- What are some other possible tables and/or graphs that we could create?

  Since the goals of campaigns in the "plays" subcategory has a wide range, from less than $1,000 to more than $50,000, there could be outliers that have disproportionate effects on our statistical results. Therefore, a box and whisker plot of the "plays" campaigns' goals could help us identify potential outliers and from there decide whether to include those data points in the dataset.
!["Plays Goals Frequency Distribution" Box and Whisker Plot](https://github.com/nhipqnguyen/kickstarter-analysis/blob/main/Resources/Plays_Goals_Frequency_Distribution.png)
