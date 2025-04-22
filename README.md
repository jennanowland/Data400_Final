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
 

## Graphs: ##


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
