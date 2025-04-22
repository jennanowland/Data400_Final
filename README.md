# DATA 400: Capstone in Data Analytics (Spring 2025) #
## Course description ##

# Cultural Competition: How American Culture Plays a Part in Pepsi vs Coca-Cola  #

![Alt text](/Users/malenamalka/Desktop/SPRING 2025/DATA 400/cokepepsiboxing630.jpeg)

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

For sales:  

* Revenue (in Millions) – Total annual revenue for Coca-Cola and Pepsi from Macrotrends 

* Quarterly Revenue – took the total revenue for each quarter to consolidate Q4 for Coca-Cola (holiday season) and Q1 for Pepsi (when Super Bowl occurs).   

 
For Stocks: 

* Close, Adj Close, Open – Daily and monthly stock price data for KO and PEP, used to compute log returns. 

* ret_log_KO, ret_log_PEP – Daily log returns for Coca-Cola and Pepsi. 

* rolling_corr – 6-month rolling correlation between KO and PEP stock returns. 

* Month, Season – Custom variables to isolate holiday and Super Bowl periods. 


For Google Trends: 
* Google Trends Index – Relative search interest for Coca-Cola, Pepsi, Coke, and PepsiCo. 

* Frequency – Graphing the difference in relative search interest between Coca-Cola and Pepsi via how often they are searched. 


 

Graphs: 
