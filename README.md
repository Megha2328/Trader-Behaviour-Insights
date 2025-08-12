📌 Overview
This project analyzes the relationship between trader performance and the Fear & Greed Index over time.
By merging trading data with sentiment index data, we visualize how market emotions (fear or greed) may influence or correlate with trading outcomes.

📂 Dataset
We use two main datasets:

Trader Data

Columns include:
Account, Coin, Execution Price, Size Tokens, Size USD, Side, Timestamp IST, Closed PnL, etc.
A new metric Trader Performance is calculated from trading results (Closed PnL).

Fear & Greed Index Data

Columns include:
timestamp, value (Fear & Greed score), classification (e.g., Fear, Greed), date

⚙️ Methodology
1. Data Cleaning
Converted timestamps into human-readable dates.
Ensured numeric conversion for relevant columns.
Removed any missing or invalid rows.

2. Feature Engineering
Created trader_performance = sum of Closed PnL over a period (daily).
Mapped value from the Fear & Greed index as fear_greed_value.

3. Merging Datasets
Both datasets were merged on the date column.

4. Normalization
Applied MinMaxScaler to scale trader_performance and fear_greed_value between 0 and 1 for visual comparison.

5. Visualization
Created a time-series line plot to compare trends of trader performance and Fear & Greed Index.

📈 Results & Insights
The graph highlights periods where high greed aligns with positive trader performance and vice versa.
Possible correlation patterns suggest that market sentiment could be a factor influencing trading outcomes.

📈 Actionable Strategies for Smarter Trading
Based on this analysis, here are three data-driven strategies:

Strategy 1: Adopt the Elite Trader's Pattern. The most successful traders in this dataset follow a clear rule: Sell into fear, hold during greed. A practical application would be to use the Fear & Greed Index as a behavioral guide. When the index drops into "Fear," it's a signal to review long positions and consider taking profits or cutting losses. When the index rises to "Extreme Greed," it's a signal to resist the urge to sell and instead let profitable positions continue to grow.

Strategy 2: Know Your Environment. For the average trader (the "Bottom 80%"), the data shows that the highest-quality trades (Average P&L) occur during "Greed" and "Extreme Greed". This suggests that for those still developing their edge, the path of least resistance is to trade with the trend in strongly positive markets. The "Fear" zones are the most dangerous for this group and should be approached with extreme caution or smaller position sizes.

Strategy 3: Use Sentiment as a Risk Management Tool. The performance gap between top and average traders is a direct measure of how difficult the trading environment is. The gap is widest in "Extreme Fear" and "Extreme Greed". This means risk should be managed most actively at the emotional poles. When sentiment becomes extreme, it is a data-backed signal to double-check your positions, confirm your strategy, and ensure you are not making an emotionally-driven decision.
