# An Analysis of Kickstarter Campaigns
## Performing Analysis on Kickstarter Data to Uncover Trends

### Overview
In this analysis, we examined an extensive amount of crowdfunding projects to pinpoint any trends that would help our client, Louise, successfully launch and fund her own kickstarter for a play that she wants to put on. From here, Louise requested to see trends that helped other campaigns be successful based on their launch dates and goals set.

### Analysis and Challenges
To begin, we took a look at a variety of kickstarter data that included film, technology, food, etc., and found that theatre was the most popular type, making up 912 out of the 3,038 kickstarters, thus giving us more concrete trends to observe.  

From here, we narrowed the data down to specifically look at Theatre Outcomes based on two things per Louises request: **Launch Date** and **Goals.**

To analyze the data by **Launch Date**, we created a new column that would organize the information by the month launched using ther YEARS() function, and then turned this into a pivot table to create a graph. We then filtered this to just examine theatre kickstarters that succeeded, failed, or were cancelled. Some challenges I faced with this pertained to editing the pivot chart fields and deciding what information to include in filters and values sections. I think going over some of this in class helped give me some clarity, as did some googling.

The **Goals Outcomes** section was a little more labor intensive. We again organized the number of successful/failed/and canceled kickstarters based on 12 different goal ranges and turned those categories into percentages based on the total amount of projects. We then used the COUNTIF() function to pull data from the Kickstarter Worksheet. The function referenced either the successful/failed/canceled column, the range in which we were searching, and specifically "plays" from the subcategory column. We then created another column and used the SUM() function to get a total number of projects per row. We then found the percentage of each category from the total number of projects and put them into their own successful/failed/canceled percentage columns and turned this into a line graph. A problem that I ran into here was that I had accidently included the country in my COUNTIF() function and filtered for the United States, and therefore was coming up with the numbers slightly off. I eventually went to a classmate for some help, and she helped identify the problem. 

### Results

**Theater Outcomes Based on Launch Date:**
There was a very clear indication that the most promising time to launch a kickstarter would be May, which showed 111 out of 166 projects proving successful, while launching a kickstarter in December or October would be the least successful. This is indicated in the line graph below in the gap between May's successful vs failed, compared to December's which are practically overlapping on the graph, or October which has the most number of failed kickstarters.To be safe, it would best to avoid launching from September-January.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/103979087/166076475-d622443a-1af6-49fe-8d58-4f98243c769e.png)


**Theater Outcomes Based on Goals:**
From the informationw we gathered, we can confidently report to Louise that keeping her goal range under $4,999 will be most successful. Goals set at $45,000 had a 100% percentage of failure, so surely stay away from that amount. Keeping the goal attainable seems to be key here. 

![OutcomeBasedOnGoals](https://user-images.githubusercontent.com/103979087/166077934-41f02e23-04fd-4b38-aa44-e9f29108e29d.png)

**Limitations:** Some limitations of this data would include the percentages given in the Outcomes Based on Goals chart. While the percentages for the goals ranging from $35,000-$39,999 and $40,000-$44,999 show that they are 67% successful, this is misleading because they are only dealing with 6 and 3 total projects. Compare this to the percentage of the most successful categories, which are dealing with 534 and 186 total projects, which gives a more concrete indication that they are actually successful because it is analyzing more data.

For the Outcomes Based on Launch Date data set, it would have been helpful to include a second chart that also included percentages of successful vs failed in regard to the grand total.
