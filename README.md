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

# ADF (Stationarity) Test and Cointegration Test Results

## ADF Results

| Sector               | Pair              | ADF Stat Stock1 | ADF Stat Stock2 | ADF p-value Stock1 | ADF p-value Stock2 | ADF Stationarity Stock1 | ADF Stationarity Stock2 |
|----------------------|-------------------|-----------------|-----------------|--------------------|--------------------|-------------------------|-------------------------|
| Financial Services   | (BAC, WFC)        | -13.865826      | -9.238028       | 6.600628e-26       | 1.610591e-15       | True                    | True                    |
| Financial Services   | (MA, V)           | -15.898216      | -10.468862      | 8.387689e-29       | 1.300054e-18       | True                    | True                    |
| Financial Services   | (V, MA)           | -10.468862      | -15.898216      | 1.300054e-18       | 8.387689e-29       | True                    | True                    |
| Financial Services   | (WFC, BAC)        | -9.238028       | -13.865826      | 1.610591e-15       | 6.600628e-26       | True                    | True                    |
| Consumer Discretionary | (HD, LOW)       | -11.891555      | -6.861978       | 5.852387e-22       | 1.593923e-09       | True                    | True                    |
| Consumer Discretionary | (LOW, HD)       | -6.861978       | -11.891555      | 1.593923e-09       | 5.852387e-22       | True                    | True                    |

## Cointegration Results

| Sector               | Pair              | Cointegration   | Cointegration p-value | Cointegrated |
|----------------------|-------------------|-----------------|-----------------------|--------------|
| Financial Services   | (BAC, WFC)        | -12.352679      | 6.396368e-22          | True         |
| Financial Services   | (MA, V)           | -15.874742      | 7.001214e-28          | True         |
| Financial Services   | (V, MA)           | -15.624532      | 1.379227e-27          | True         |
| Financial Services   | (WFC, BAC)        | -17.874831      | 2.073644e-29          | True         |
| Consumer Discretionary | (HD, LOW)       | -15.809165      | 8.321765e-28          | True         |
| Consumer Discretionary | (LOW, HD)       | -12.224898      | 1.216816e-21          | True         |

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




