# Robust-Asset-Allocation
Replication of Wes Gray's Robust Asset Allocation 

# Robust Asset Allocation Replication

This repository contains the replication code for the Robust Asset Allocation strategy, originally proposed by Wes Gray. The strategy aims to provide a diversified and adaptive investment approach by dynamically allocating assets based on momentum and simple moving average signals.

## Strategy Overview

The Robust Asset Allocation strategy is designed to create a balanced portfolio of various asset classes using a combination of momentum and moving average signals. The strategy involves the following steps:

1. Retrieve Daily Price Data: The code fetches daily adjusted price data for a set of ETFs representing different asset classes.

2. Monthly Returns Calculation: The daily price data is converted to monthly prices, and the corresponding monthly returns are calculated.

3. RAA Balanced Portfolio: The strategy constructs a balanced portfolio using predefined weights for each asset class. The portfolio is rebalanced on a monthly basis.

4. TMOM Signal: The strategy calculates the TMOM (Trend Following Momentum) signal by comparing the cumulative returns of the balanced portfolio to a bond ETF (IEF). If the cumulative returns are greater than zero, the portfolio goes long with 50% allocation.

5. SMA Signal: The strategy calculates the SMA (Simple Moving Average) signal by comparing the cumulative returns of the balanced portfolio to its 10-month moving average. If the cumulative returns are greater than the SMA, the portfolio goes long with 50% allocation.

6. Realized Returns: The calculated signals are used to determine the realized returns for the strategy. Each signal is multiplied by the subsequent period's balanced portfolio returns to generate realized returns.

7. RAA Balanced Returns: The final RAA Balanced Returns are obtained by combining the realized returns from both the TMOM and SMA signals, each with a 50% allocation.

## How to Use

1. **Prerequisites:** Make sure you have R and the required packages (quantmod and PerformanceAnalytics) installed.

2. **Clone the Repository:** Clone this repository to your local machine using Git.

3. **Adjust Parameters:** Open the R script and modify the parameters as needed, such as `startDate`, `endDate`, `retLookBack`, and `smaLookBack`.

4. **Run the Code:** Run the R script in your preferred R environment. The script will replicate the Robust Asset Allocation strategy and print the resulting RAA Balanced Returns.

5. **Review Results:** Review the printed RAA Balanced Returns to assess the performance of the strategy over the specified period.

## Disclaimer

Please note that the replication code provided in this repository is for educational and informational purposes only. The performance of the strategy may vary in real-world scenarios due to various factors. Always conduct thorough research and consider seeking professional advice before making any investment decisions.

## Author

This replication project was created by [Your Name] as part of [Your Project's Name] at [Your Institution/Organization].

## References

For more information about the original Robust Asset Allocation strategy, you can refer to the research by Wes Gray and Alpha Architect.

- [Alpha Architect Website](https://alphaarchitect.com/)
- [Original Research Paper](https://alphaarchitect.com/2014/12/the-robust-asset-allocation-raa-index/)
















