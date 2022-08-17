# kickstarter-analysis

## Louise, a creative friend of mine, asked me to analyze Kickstarter data on various campaigns from around the world in order to be more successful during her own Kickstarter campaign.

### The purpose of this analysis is to provide Louise, an aspiring playwright, with plenty of information regarding outcomes based on goal, location, campaign category, and  subcategory.

## Analysis and Challenges
	Initially, we had created a simple bar graph showing amount of successful, failed, cancelled, and live campaigns based off parent category. We did this by taking the outcomes column, and filtering it by outcome. We did the same for the category column, filtering by category.

![ParentCategoryOutcomes.png](/resources/ParentCategoryOutcomes.png)

	We then had created new columns that showed the percentage funded and the average donation of each campaign, as well as delineating subcategories from parent categories of the kickstarter campaigns as seen below.

![ColumnsDelineatingCampaigns.png](/resources/ColumnsDelineatingCampaigns.png)

	We further described each campaign based off of date starter/ended, and the year that it took place. By including this additional information for each campaign, we were able to create several pivot tables and charts showing different metrics of successful/failed campaigns based on campaign goals and campaign start/end dates.

	Thankfully, the information gathered from the data analysis was pretty straight forward. However, challenges arose when creating the pivot tables for outcomes based on launch date in the form of syntax errors contained in the formula for the =COUNTIFS() function. I initially was not obtaining correct percentages of successful/failed/canceled campaigns based on their campaign goal, but with further inspection I found that I simply was not including an '=' before each range. After correcting this omission, the percentages made much more sense for the type of information we were looking for.

### Analysis of Outcomes Based on Launch Date

	After creating a pivot table from the Kickstarter data, we choose to filter by Parent Category and Years. We choose Outcomes to be the columns, and Date Created to be the Rows. We choose outcomes to be the the Values we are wanting to see. By choosing 'Theater' to be our Parent category we are looking for, we are able to see how successful each theater campaign is depending on the time of year it started.

![LaunchDatePivotTableFields.png](/resources/LaunchDatePivotTableFields.png)

![Theater_Outcomes_vs_Launch.png](/resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

	After we have viewed outcomes of campaigns based on start date, we wanted to further our knowledge of successful kickstarter campaigns for specifically plays by looking at their outcomes based on goals. We did this by creating a table for various goal ranges using the =COUNTIFS() function. By using the goal range, outcome, and plays as criteria we were able to calculate the percentage of successful, failed, and canceled kickstarter campaigns for plays based on goal.

![OutcomesBasedOnGoalTable.png](/resources/OutcomesBasedOnGoalTable.png)

![Outcomes_vs_Goals.png](/resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

	With the kickstarter data being generally straight forward, not many challenges arose from retrieving the specific data we were interested in. However, learning to apply the different types of functions proved troublesome to some degree. Using the =COUNTIFS() function seemed slightly tedious in regards to including the several different criteria we were trying to analyze. Reviewing the function by looking at each criteria individually was beneficial in making sense of the delineation of data. After finding the correct syntax to use for each criteria, we were able to create a useful table and line graph of outcomes based on goals.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
	
	1. May is the best month to start a kickstarter campaign.
	2. October, or rather the fall entirely, is the worst time to start a kickstarter campaign.

- What can you conclude about the Outcomes based on Goals?

	1. The lower the goal for kickstarter campaigns, the more successful it is likely to be.

- What are some limitations of this dataset?

	The range of the goal category seems to be to large to give campaigns serious credibility. Many goals are either too small and become too easy to succeed, or too large to take as a serious campaign.

- What are some other possible tables and/or graphs that we could create?

	We could create a graph based on amount pledged vs country to see which countries are more willing to donate to various kickstarter campaigns. We may also see which countries were more willing to back certain categories of campaigns compared to other categories.
