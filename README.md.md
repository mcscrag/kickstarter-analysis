# Kickstarter Funded Plays Analysis

## An analysis of the outcomes of kickstarter funded plays based on launch date and funding goal 

### The goal of this analysis was to discover any trends in the succeess rate of kickstarter funded plays. The study focused on the month of the campaign's launch, as well as the size of the funding goal. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

The Kickstarter data on all theater related campaigns was broken down by the month of the campaign's launch using a pivot table. Campaigns were sorted by the three main outcomes of "successful", "failed", and "cancelled". The following chart was generated from the table:
![Outcomes Based on launch Date](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

The outcomes of campaigns for plays was also analyed based on the size of the funding goals. The funding goals were broken down into $5,000 brackets over the range of $0 to $50,000. The number of successful, failed, and cancelled campaigns with funding goals in each of these brackets was summed and then calculated as a percentage of the total campaigns in that bracket. The following chart was generated from this data and shows the outcomes as a percentage of the total campaigns in the the labelled funding bracket:
![Outcomes Based on Funding Goal](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

I am very experienced with Excel, so I didn't experience any specific challenges in gathering the data or creating the charts. However, I did find the method used to create the COUNTIFS functions to be tedious. Having to edit each cell to include the text arguments was time consuming. In the past I have created cells underneath the table that have each text argument and thus can be referenced in the COUNTIFS function as a cell rather than text. For example, instead of COUNTIFS(Kickstarter!$E:$E, "=successful") I would just have a cell with the text "successful" and then reference that cell in the formula, thus allowing me to drag the formula across all the cells in the row I want to apply it to.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

    1. There appears to be a greater quantity of Kickstarter campaigns in the theater category that launch in the late spring and early summer months. However, the percentage of campaigns that succeed in these months is only marginally higher. Therefore we can conclude that there is only a slight advantage to launching a theater Kickstarter campaign between the months of April and July. 

    2. There is a significant drop in not only the number of campaigns launched in December, but also their success rate, with nearly 50% of all campaigns launched in december failing to reach their funding goal. It's difficult to say why without further study, but one possible explanation is that individuals who might otherwise donate are less likely to in December since they may be already spending more of their money on holiday gifts and thus have less available for kickstarter donations. Based on this data it would be advised to avoid launching a campaign in December.

- What can you conclude about the Outcomes based on Goals?

    1. There is a consistent downward trend in the success rate of a campaign as the funding goal increases between the brackets of 0-$30,000. This data is also the most reliable in the set as the total number of campaigns in this bracket is over 100 times over the total number of campaigns between $30,000-$50,000. It can be said the sample size for the latter bracket is not large enough and the data is unreliable.

    2. Using "outcome" as a metric for success is inherently biased in this data since increasing the funding goal will by it's very nature make it harder for the campaign to "succeed". I think it is difficult to suggest that the data shows whether it is "better" or "worse" to have a lower funding goal, just that clearly it will be easier to meet that goal and thus be labelled a "successful" campaign the smaller the funding goal. 

- What are some limitations of this dataset?

    1. There are a lot of metrics that would need to be added to get more insight on what funding goals to set or what month to launch the campaign. For instance, it is tempting to suggest that the campaigns launched between April-June are more successful because good weather tends to make people want to look for events in their communities, and thus be more inclined to fund these events. However, if we drew in regional data we could learn more about whether this is true or not depending on what hemisphere the campaign was launched in. 
    2. The funding goal data set is set up in a way where the majority of the data points are in the first three funding brackets. In fact, approximately 90% of the data is in the first three brackets, and thus the chart is **skewed to the right**. This conclusion is also represented by looking at the difference between the mean and the median of the data. In this case, the average total projects for a funding bracket is 87, while the median value is 18. Because the mean is so much greater than the median, it means the data is skewed to the right. Finally, this can be visualized with a simple bar chart of total projects as seen below:
    ![Total Projects per Funding Bracket](/Resources/Total_Projects_vs_Funding_Bracket.png)

- What are some other possible tables and/or graphs that we could create?

    1. As mentioned earlier in the limitations, a useful addition to the pivot table would be a filter and values for country. This would allow us to investigate why campaigns launched in December are less likely to meet their fundraising goals. We could also look to combine the two analyses of funding goal and launch date into a single table. This would allow us to consider that maybe more of the campaigns started in december had higher funding goals and therefore the start month had less to do with their failure.
