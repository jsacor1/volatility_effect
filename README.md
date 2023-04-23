# volatility_effect

## Overview

In financial literature is regarded that higher risk leads to higher returns. The standard deviation or volatility is regarded as one of the most important measures of risk in finance. In this exercise, I am showing the volatility effect anomaly in the financial markets, in which low volatility stocks actually have higher returns than high volatility stocks.

## Methodology

The universe of data consists of the 48 industry portfolios from the Kenneth R. French database, which consists of returns from 1926 to the first month of 2023. For purposes of this analysis, I used monthly returns.

At the end of every month, equally weighted decile portfolios are constructed based on the ranking of the stocks depending on their past 36 months volatility (3 years) of monthly returns. Industries with the lowest volatility are assigned to the top decile portfolio. For more details, look at the code in the src folder.

## Results

![Picture 1](https://user-images.githubusercontent.com/114669230/233850964-83b5a88d-b6eb-4ac8-a62d-019d32c8813a.png)

Can be seen that most portfolios have similar performance with respect to their annualised return, so there seems to be a weak relation between historical volatility and the return on the following month if the last decile is not considered. The difference between the top and bottom decile is of around 3.5%.

However, if we switch the focus of the analysis from merely excess annualised returns to the return per unit of risk (Sharpe ratio), interesting things arise. Can be seen a clear relationship in which the portfolios in the top deciles have higher Sharpe ratio and as we go to the bottom deciles the Sharpe ratio decreases substantially. The top decile portfolio has a Sharpe ratio that is more than 3 times that of the bottom decile portfolio. The standard deviation is the main factor impacting the variation in the Sharpe ratio.

Furthermore, can be seen the alpha is significant and positive for top decile portfolios and it starts to decrease in significance as we move to the bottom decile portfolios. Actually, after the 5th decile the alpha is no longer significant (D8 being an exception) implying that the alpha is equal to zero, and therefore suggesting that those portfolios do not generate abnormal returns with respect to the CAPM.

With respect to the beta, can be seen that it tends to increase as we move from top decile portfolios to bottom decile portfolios. This makes sense because the beta is a measure of systematic risk, therefore the fact that top decile portfolios have lower volatility implies that their beta should be lower. The low beta stocks generate higher risk adjusted returns than the high beta stocks.

In conclusion, low-volatility stocks show higher risk adjusted returns than the universe portfolio and than higher-volatility stocks. Additionally, the volatility effect is another factor that is not explained by the single factor model: CAPM.

