# Co-integration-Test-MSFT-TESLA
This Python project tests whether the stock prices of two companies are co-integrated, meaning they move together in the long term, even if they deviate in the short term. Co-integration is a statistical property that can be useful for traders who want to identify pairs of stocks for strategies like pairs trading.

How It Works
Fetching Historical Stock Data: The script fetches historical stock prices for two tickers (in this example, Apple (AAPL) and Microsoft (MSFT)) from Yahoo Finance using the pandas_datareader library. The date range is set to the past 5 years.

Using Closing Prices: The closing prices of both stocks are extracted for analysis, as these reflect the final prices of the stocks at the end of each trading day.

Engle-Granger Co-integration Test: This is a statistical test to check whether two time series (in this case, the two stocks' prices) are co-integrated. If they are co-integrated, it means that although they may diverge in the short term, they maintain a stable long-term relationship.

Interpreting the Results:

Score: A numerical result from the test.
P-value: The probability that the observed relationship is due to chance.
If the p-value is less than 0.05, it suggests that the two stock prices are co-integrated. This means they tend to move together in the long term.
If the p-value is greater than 0.05, the two stock prices are not co-integrated, meaning they do not maintain a stable relationship over time.
Example Output:
Co-integration test score: -1.23 (example score)
P-value: 0.03 (example p-value)
If the p-value is less than 0.05, the series are likely co-integrated, meaning they move together in the long run. If it’s greater than 0.05, they are not co-integrated.

Running the Script
Install the required Python libraries:

bash
Copy code
pip install pandas pandas_datareader statsmodels
Run the script:

bash
Copy code
python co_integration_test.py
The script will output whether the two stocks are co-integrated or not based on the test results.

Conclusion
This project allows you to analyze the relationship between two stocks over time and determine if they are co-integrated, which can help in financial trading strategies.
