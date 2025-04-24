# Cultural Competition: How American Culture Plays a Part in Pepsi vs Coca-Cola  #

![cokepepsiboxing630](https://github.com/user-attachments/assets/ed2627e3-cb53-4c2f-8367-945647d69d95)

## Introduction: ##
This project explores the long-standing rivalry between Coca-Cola and Pepsi using a data analytics lens. We investigate how key advertising moments—like Coca-Cola's Christmas campaigns and Pepsi's Super Bowl halftime show sponsorship—impact each company’s sales, stock performance, and consumer interest (via Google Trends). By combining time series, web search, and financial data, our goal is to understand whether heightened consumer interest translates into measurable economic signals. 

 
## Project Description: ##
We analyze how Coca-Cola and PepsiCo advertisements actually translate to sales and increase in stock prices.  Specifically, Pepsi hosted the Super Bowl Halftime show for a while; while millions of American Football fans watch the halftime show, this positive increase in marketing may have led to positive revenue and stock prices.  By looking into Pepsi sales from 2012 to 2022 (the most recent ten years of the Pepsi Halftime show before selling it to Apple Music), one can analyze if there is an increase in sales during the month the Super Bowl occurs – every February.   
Moreover, Coca-Cola has a well-known Santa Campaign during the Holiday season (November to Early January) which could be seen as a similar marketing strategy to Pepsi’s Halftime show.  Therefore, also looking into Coca-Cola sales from 2012 to 2022 during the months of November to January 1st, one can analyze if this marketing strategy translates to a drastic improvement in revenue.   
During both these time frames for the respective companies, we will analyze how the stock prices are also influenced.  Additionally, since there has been an increase in social media influencing consumers, analyzing how Google Trends play a role in the searches during the respective time frames.  The frequency of how often people Google either Coca-Cola / Coke vs Pepsi may also translate to stock prices, sales, and overall consumer perceptions.   

 
## Datasets: ##
This project uses multiple data sets. The first dataset used is the sales of both Coca-Cola and Pepsi provided by MacroTrends.  We specifically look into the sales during the company’s specified times to see the respective outcomes of their marketing.   
Another dataset that we used was provided by Yahoo Finance’s Python package, where we could see closing prices for both the Coca-Cola Company and PepsiCo. Finally, we created a csv file with Google searches (or Google Trends.) This dataframe showed how often people are interacting or searching for Coca-Cola, Coke, Pepsi, or PepsiCo.   

**Main Variables:**

*For sales:* 

* Revenue (in Millions) – Total annual revenue for Coca-Cola and Pepsi from Macrotrends 

* Quarterly Revenue – took the total revenue for each quarter to consolidate Q4 for Coca-Cola (holiday season) and Q1 for Pepsi (when Super Bowl occurs).   

 
*For Stocks:*

* Close, Adj Close, Open – Daily and monthly stock price data for KO and PEP, used to compute log returns. 

* ret_log_KO, ret_log_PEP – Daily log returns for Coca-Cola and Pepsi. 

* rolling_corr – 6-month rolling correlation between KO and PEP stock returns. 

* Month, Season – Custom variables to isolate holiday and Super Bowl periods. 


*For Google Trends:*

* Google Trends Index – Relative search interest for Coca-Cola, Pepsi, Coke, and PepsiCo.
  
* Frequency – Graphing the difference in relative search interest between Coca-Cola and Pepsi via how often they are searched. 

## Models: ## 

**Sales**

Our analyses of Revenue for both Coca-Cola and Pepsi include a time series visualization and a comparative revenue growth model.  The time series visualization depicts the differences in revenue for Coca-Cola and Pepsi during the first and last quarter (Q1 and Q4) for the years 2012-2022.  By doing so, we can pinpoint if the Super Bowl Halftime Sponsorship for Pepsi translates to sales - similarly for Coca-Cola's Santa and Holiday marketing campaign.

The comparative revenue growth model shows the percentage of revenue growth or decline compared to the year prior.  One can use this to see if each company's marketing campaign is assisting in overal company growth and more.  By identifying if the marketing is helping revenue trend upward or downward, each company can identify if allocating resoruces to the sponsorships is worth it.

---

**Stocks**

Our analysis used descriptive and inferential statistical methods to explore stock behavior for Coca-Cola and Pepsi. We computed monthly log returns to analyze relative changes over time and examined how closely the two stocks moved together using a 6-month rolling correlation. To describe return behavior in more detail, we calculated summary statistics such as mean, standard deviation, skewness, and kurtosis. We also explored the correlation between the two brands by comparing monthly percentage changes in their stock prices.

One key feature of our analysis was the use of seasonal event windows to assess performance around key marketing moments. We grouped and averaged Coca-Cola’s log returns during the holiday season (November, December, January) and Pepsi’s returns during February to capture the Super Bowl effect. To account for the fact that January belongs to the previous year’s holiday campaign, we adjusted the calendar year accordingly. By combining these returns into a single visual, we were able to directly compare the average impact of seasonal marketing campaigns on each company's stock performance across multiple years.

---

**Consumer engagement**

Our Google Trends analysis focused on search interest in Coca-Cola and Pepsi during key advertising periods. We used a cleaned and time-indexed dataset of monthly search frequencies extracted via the Google Trends platform. For Pepsi, we isolated searches during the months of January, February, and March to capture the Super Bowl season. For Coca-Cola, we focused on November and December to capture interest during the holiday campaign window.

We visualized search interest over time using line plots created with matplotlib and styled with seaborn. To improve interpretability, we ensured that date formats were consistent and replaced any <1 search values with numeric approximations. There were no machine learning models or advanced statistics in this part of the analysis, just clear and effective use of exploratory data analysis (EDA) and time-based filtering to interpret consumer behavior through search activity.

---

## Graphs: ##
![revenue](https://github.com/user-attachments/assets/202ee4d0-de62-406b-aefa-f8676b4c5930)
The Pepsi vs Coca-Cola rivalry can be answered in this graph alone.  Pepsi is the "winner" in terms of total yearly revenue.  However, one must note that Pepsi owns other large snack companies like Cheeto's and Lay's Chips.  Meanwhile, Coca-Cola remains in the beverage world with Powerade, Sprite, and more.  Overall, it also cannot be concluded that the Santa marketing for Coca-Cola and the Super Bowl for Pepsi lead to a direct translation in increasing revenue. 
![yearly](https://github.com/user-attachments/assets/ca9de793-5f40-4e14-a546-7e9a4872df6e)

This graph displays the yearly revenue growth rate of both Pepsi and Coca-Cola.  Pepsi, for the most part, is on a steady upward increase in revenue each year.  On the other hand, Coca-Cola has some large dips.  Specifically, around 2017 Coca-Cola refranchising their bottling systems to emphasize value over volume. 
![close](https://github.com/user-attachments/assets/edb95265-8e35-48ff-9030-75be9068a03d)
Over the past decade, PepsiCo consistently maintained a higher stock price and steeper growth than Coca-Cola. Both stocks briefly dipped during the 2020 recession but recovered quickly, highlighting their resilience as consumer staples.
![output_season](https://github.com/user-attachments/assets/63103721-e56f-42a5-b6f9-441caa8ad41d)
Coca-Cola's holiday season returns are generally more stable, while PepsiCo’s Super Bowl returns are more volatile with occasional spikes. Volume trends show Coca-Cola’s holiday periods typically attract higher trading activity, whereas PepsiCo’s Super Bowl-related volume fluctuates more across years.
![returns_season](https://github.com/user-attachments/assets/88687ce7-1634-4997-a4df-0796df900553)
Coca-Cola shows positive average returns during the holiday season (Nov–Jan), followed by a drop in February. In contrast, Pepsi experiences negative returns during the Super Bowl month (Feb), but sees a strong rebound in March, suggesting a delayed market reaction to its major campaign.
![trends](https://github.com/user-attachments/assets/f20094e6-4a05-4cd8-84ec-85df5f43ce6f)
The Google Searches display that the highest peaks occured the first two Super Bowl's for Pepsi.  Coca-Cola does not receive nearly as many searches.  Some things to keep in mind are that people had to specifically search "Coca-Cola" in order for it to be counted in the data.  In the future, it might be useful to broaden the search with proper data cleaning techniques.


## Takeaways ##

**Sales**

The data showed that there was no significant effect from the respective advertising events for Coca-Cola and Pepsi. Coca-Cola has a very consistent stream of revenue; Q1 and Q4 are consistently very close to one another. This suggests that if the holiday marketing campaigns aren’t too costly, they may still be worth running due to other emotional or brand-building benefits.

On the other hand, Pepsi shows a drastic difference between Q1 and Q4 revenue. Although the Super Bowl takes place in Q1, Pepsi repeatedly generates significantly more revenue in Q4 year after year.

When comparing overall performance, Pepsi is ahead in total revenue. However, this is partially because PepsiCo owns a wider range of snack brands (e.g., Cheetos, Lay’s, Doritos), while Coca-Cola focuses mostly on beverages (e.g., Sprite, Powerade).

---

**Stocks**

The stock analysis revealed that both Coca-Cola and PepsiCo experienced steady long-term growth from 2012 to 2022, with PepsiCo consistently maintaining a higher stock price. Although Coca-Cola’s growth was more gradual, it demonstrated stability and resilience throughout the decade. 

Both companies showed a brief decline during the 2020 recession but recovered quickly, reinforcing the idea that consumer staples stocks tend to be reliable during periods of economic uncertainty. 

When analyzing short-term performance around key promotional periods (during the Santa campaign for Coca-Cola and around the Super Bowl for Pepsi), Coca-Cola saw higher returns during its holiday campaign months, while PepsiCo tended to experience stronger returns in the month following the Super Bowl. These patterns suggest that while both companies benefit from seasonal marketing, the timing and impact on investor behavior vary across strategies.

---

**Google Trends**

Google Trends data revealed a notable difference in consumer search activity. Across relevant time periods, Pepsi consistently had more searches than Coca-Cola. However, the limitations of the dataset must be noted. For instance, Google Trends data was limited to “Coca-Cola,” excluding related terms like “Coke” or misspellings that might still lead to Coca-Cola content.

Additionally, it's unclear how Google handles autocorrections in search queries (e.g., "Did you mean...?"). Despite these limitations, it is clear that Pepsi had stronger online search engagement than Coca-Cola throughout the campaign periods.
