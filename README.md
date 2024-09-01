# Pairs Trading Strategy
This project aims to scan the top 10 stocks of 5 sectors (Tech, Financial, Healthcare, Consumer Discretionary, Industrials) sector for stock pairs to implement a pairs trading strategy.

# Methodology
1. Identify stock pairs with correlation > 0.8 and visualize results using a correlation matrix heatmap using data from 2023 (Jan - Dec)
2. Check pairs for stationarity and cointegration using functions from statsmodel.tsa.stattools
3. Visualize spreads
4. Define trading strategy as buying the spread when it is +1 SD away from the mean and selling when it is -1 SD away from the mean
5. Backtest strategy against data from 2024 (Jan- Aug)
6. Plot equity curves for each pair, compare the return of portfolio with equal weights in each pair to the S&P 500 over the same timeframe.

# Correlation Matrix Heatmaps by Sector
Pairs identified with correlation > 0.8 are BAC- WFC, MA- V and HD- LOW.
![image](https://github.com/user-attachments/assets/c5c549df-a478-4710-8353-90f2d99d324b)
![image](https://github.com/user-attachments/assets/e6e448cb-6e9a-4fb8-b080-092819be5d59)
![image](https://github.com/user-attachments/assets/b8045878-df7f-488b-ab67-322e8d5b939b)
![image](https://github.com/user-attachments/assets/53f24076-240e-4c06-b0f3-166519846227)
![image](https://github.com/user-attachments/assets/31992841-b3a4-4a32-8598-7dd177aceddf)

# Pair Spreads (spread means are normalized to 0)
![image](https://github.com/user-attachments/assets/31e01b9d-65a1-49f4-afea-ebbdabb847a5)

# Equity Curves and Results
![image](https://github.com/user-attachments/assets/2b236ebf-c198-4b08-9008-6b45ad63df80)

| Stock Pair   | % Return (Jan 2024 - Aug 2024)|
|--------------|-------------------|
| BAC - WFC    | 31.06%            |
| MA - V       | 26.80%            |
| HD - LOW     | 8.56%             |
| Portfolio    | 22.14%            |
| S&P 500      | 16.43%            |




