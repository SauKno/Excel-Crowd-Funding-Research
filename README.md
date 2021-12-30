# Overview of Project
Louise is an up and coming playwrite who is seeking funding for her play, Fever. She has bene able to come close to meeting her fundraising goal in a short amount of time and is wanting to gain a deeper understanding of the outcomes of theater campaigns based on launch date and funding goals. This analysis uses 1,369 theater campaigns from around the world to determine trends around outcomes based on the launch date and funding goals. 

# Analysis and Challenges
The data table provided us with the following information about the campaigns that were used to answer Louise's question about the relationship between compaign outcomes and the launch date and the campaign goals: names, categories, goals, outcomes, and dates in Unix Timestamp. I first filtered the data set to only include Theater Campaigns, as this is the category Louise's campaign falls within. This shrunk the data set from 4, 115 to 1,369 campaigns. I then began working with the data required to uncover the outcomes of campaigns solely focusing on the fundraising goals.
## Outcomes Based on Goals
In order to address Louise's questions around outcomes based on goals, I first created a column (O) in the orignal data set on the Kickstarter sheet to determine the percentage funded based on the campagin goal, using the formula *ROUND(E522/D522* * *100,0)*. I then created a new sheet titled "Outcomes Based on Goals". On this sheet I built a table that categorically showed the outcomes of campaigns based on their fundraising goals, 0 - $1000, $1000 to $4999, $5000 to $9999, $10000 to $14999, $15000 to $19999, $20000 to $24999, $25000 to $29999, $30000 to $34999, $35000 to $39999, $40000 to $44999, $45000 to $49999 and Greater than $50000. Using the Countifs formula, I extracted the data from the original data set from the Kickstarter sheet to show how many campaigns within these categories were successful, failed, or canceled. I then created a column to find the Sum of all the projects within each category so that I could determine the percentage of success, failure, and cancelation. This would allow me to show outcome trends within each category, which allows Louise to see how the financial goals correlate with the outcomes.
### Outcomes Based on Goals Table
<img width="746" alt="Outcomes Based on Goal Table" src="https://user-images.githubusercontent.com/94129215/147785721-bd2c53a0-06e5-448e-ad59-30fe1c367291.png">

### Outcomes Based on Goals Line Graph 
<img width="1215" alt="Outcomes Based on Goal" src="https://user-images.githubusercontent.com/94129215/147785740-ad545927-6456-4987-99bf-3e8b9f2939bf.png">

## Outcomes Based on Launch Date
In order to answer her question about oucomes based on launch date, I created a column (S) in the original data set on the Kickstarter sheet where I converted the Unix Timestamps to Dates using the forumla *(((I522/60)/60)/24)+DATE(1970,1,1)*. I then created an additional column (U) to extract the year from the Launch Date using the formula *Years(Sxxx)*. I then created a sheet titled "Theater Outcomes by Launch Date". I created a pivot table with the filters as Parent Category and Years, Columns as outcomes, Rows as Date Created Conversion, and Values as Count of Outcomes. I then used the Parent Category filter to only include Theater since this is the same category as Louise's play. I also ordered the columns in descending order so that Successful would be first and only displayed the month for the date. This filter was important as it allowed me to show the success rate by months of the year instead of each individual date in the data set, which would have been to many data points to visualize on one graph.  

### Pivot Table 
<img width="359" alt="Screen Shot 2021-12-25 at 12 14 09 AM" src="https://user-images.githubusercontent.com/94129215/147377952-9da039b6-f9fc-47d2-bccf-af3326dc9ee0.png">

###  Outcomes Based on Launch Date Line Graph
![image](https://user-images.githubusercontent.com/94129215/147378014-8b908d81-faec-45a1-8b4b-dfb040f59f30.png)
## Challenges
I did not experience any challenges with this analysis, but there were a few challenges I believe one could encounter with this challenge. First, the graphs need to have the correct data for the x and y axis. If the pivot tables were not created correctly, the data points could be sitting on the wrong axis. The solution to this is to select format table and then select switch rows/columns. The second challenge I could see occurring was on the Outcomes Based on Goals table. The countifs formula was long and you had to put the $ in front of the column label to ensure it would continue to pull from that column, regardless of where you copied the formula. 
# Results
## Conclusions 1 about Theater Outcomes by Launch Date
Overall, more theater campaigns are successful than unsuccessful. I am able to draw this conclusion because the successful line is above teh failed and canceled line for every month, with December being the only month the come close to being the same. 
## Conclusions 2 about Theater Outcomes by Launch Date
May, June and July are the most successful months for theater fundaraising campaigns overall, with May being the month with the highest success rate by about 10%. 
## Conclusions about Outcomes based on Goals
Campaign goals that fell within the $1000 to $4999 category had 100% successrate and was the highest category by almost 25%. 
# Limitations
The data set is not particularly large within the theater category. If Louise wants to have a better understanding of how other campaigns do, it would be beneficial to have a larger data set. It would also benefit her to see the outcomes based on genre, not just category. In addition, it would be beneficial to compare the outcomes based on the countries the campaigns were launched. This would provide additional insight to countries that are more invested in theater than others. This graph would add an a layer of understanding that lives within the culture and climate of regions that they other graphs did not highlight. 
