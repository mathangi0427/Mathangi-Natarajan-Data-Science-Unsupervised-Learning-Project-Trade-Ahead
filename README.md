# Data-Science-Unsupervised-Learning-Project-Trade-Ahead

**Context**

The stock market has consistently proven to be a good place to invest in and save for the future. There are a lot of compelling reasons to invest in stocks. It can help in fighting inflation, create wealth, and also provides some tax benefits. Good steady returns on investments over a long period of time can also grow a lot more than seems possible. Also, thanks to the power of compound interest, the earlier one starts investing, the larger the corpus one can have for retirement. Overall, investing in stocks can help meet life's financial aspirations.

It is important to maintain a diversified portfolio when investing in stocks in order to maximise earnings under any market condition. Having a diversified portfolio tends to yield higher returns and face lower risk by tempering potential losses when the market is down. It is often easy to get lost in a sea of financial metrics to analyze while determining the worth of a stock, and doing the same for a multitude of stocks to identify the right picks for an individual can be a tedious task. By doing a cluster analysis, one can identify stocks that exhibit similar characteristics and ones which exhibit minimum correlation. This will help investors better analyze stocks across different market segments and help protect against risks that could make the portfolio vulnerable to losses.

**Objective**

Trade&Ahead is a financial consultancy firm who provide their customers with personalized investment strategies. They have hired you as a Data Scientist and provided you with data comprising stock price and some financial indicators for a few companies listed under the New York Stock Exchange. They have assigned you the tasks of analyzing the data, grouping the stocks based on the attributes provided, and sharing insights about the characteristics of each group.

**Data Dictionary**

Ticker Symbol: An abbreviation used to uniquely identify publicly traded shares of a particular stock on a particular stock market
Company: Name of the company
GICS Sector: The specific economic sector assigned to a company by the Global Industry Classification Standard (GICS) that best defines its business operations
GICS Sub Industry: The specific sub-industry group assigned to a company by the Global Industry Classification Standard (GICS) that best defines its business operations
Current Price: Current stock price in dollars
Price Change: Percentage change in the stock price in 13 weeks
Volatility: Standard deviation of the stock price over the past 13 weeks
ROE: A measure of financial performance calculated by dividing net income by shareholders' equity (shareholders' equity is equal to a company's assets minus its debt)
Cash Ratio: The ratio of a company's total reserves of cash and cash equivalents to its total current liabilities
Net Cash Flow: The difference between a company's cash inflows and outflows (in dollars)
Net Income: Revenues minus expenses, interest, and taxes (in dollars)
Earnings Per Share: Company's net profit divided by the number of common shares it has outstanding (in dollars)
Estimated Shares Outstanding: Company's stock currently held by all its shareholders
P/E Ratio: Ratio of the company's current stock price to the earnings per share
P/B Ratio: Ratio of the company's stock price per share by its book value per share (book value of a company is the net difference between that company's total assets and total liabilities)

**EDA - Summary of Observations**

The distribution of the Current Price is right skewed with some outliers on the right. The current stock price of 50% of the companies listed in the Stock dataset is less than 60 dollars.

The Energy Sector has a price change of -10% in 13 weeks time span. Hence the Investors need to be cautious in investing in the Energy Sector as the stock prices has gone down 10%.

The Health care sector is performing well with an increase in price of around 9% in the 13 weeks timeframe.

The Cash ratio of the Information technology sector is highest with 140 followed by Telecommunication services and Health care sectors. The Utilities sector has a very low cash ratio of 15.

The Energy Sector has a very high P/E ratio hence it is bad idea to invest in the Energy sector. The P/E ratio of Industrials, Consumer Staples, Financials, Utilities, Materials are below 20. It might be a good decision to invest in the stocks of these sectors.

The Current Price and the Earnings Per share has a positive correlation between each other meaning as the stock price is increased the earnings per share also increases. The Net Income has a good positive correlation with Earnings per share and Estimated shares outstanding. As the companies Net Income increases its obvious that their earnings per share also increases and so is the number of outstanding stocks.

The Volatility has a negative correlation with Price change, Net Income and Earnings per share. The Financial measure ROE has a moderate negative correlation with Earnings per share.

**Conclusion**

The Silhouette score of K-Means gave a clear idea on choosing the good number of clusters than the Elbow plot.

The K-Means clustering algorithm took less time for execution than the Hierarchical Clustering. The difference in execution time is not very significantly high as the number of datapoints is low.

The Hierarchical clustering algorithm with ward linkage and Euclidean distance measure gave more distinct clusters and it was clear enough to segment to proceed with the insights.

The Cluster 0 of the K-Means clustering algorithm and the Cluster 3 of the Hierarchical clustering algorithm are very similar in nature. K-Means yielding 277 observations in cluster 0 and Hierarchical clustering algorithm yielding 285 observations in cluster 3 which are of similar characterisitcs.

The appropriate number of clusters obtained from K-Means is 4.

The appropriate number of clusters obtained from Hierarchical clustering is 6.

**Actionable Insights and Recommendations**

The following are the insights and recommendations for the Trade & Ahead Financial firm.

The companies in Cluster 0 is good in terms of Net Income, Earnings per share and Estimated shares outstanding. The Volatility and the price change is also low. Hence new investors can target these companies as the current price is also low and the risk factor in investing is moderately low.

The companies in cluster 1 has very high ROE but the Net Income, Earnings per share are all low. Hence Investors need to gauge the attributes other than the ROE to invest in these companies.

The companies in Cluster 2 are good investment strategy companies for investors who tend to buy high value stocks and it is good in terms of price change and volatility as well.

All the attributes in the cluster 3 companies are in the moderate range meaning investors who tend to take no risk at all can invest in these companies as the fluctuation of all the attributes are moderately less than other clusters.

The Cluster 4 and Cluster 5 companies are performing poorly in terms of Volatility, P/E ratio, Net Income, Earnings per share etc. These companies are poor Investing strategy based on the data of the 13 weeks timeframe. The one factor the investors can take risk about is the current price is low in cluster 4. Hence first time investors can take less risk in buying some low priced stocks.
