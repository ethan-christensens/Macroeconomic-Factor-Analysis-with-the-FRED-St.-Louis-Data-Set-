# Macroeconomic Factor Analysis Using the FRED St. Louis Data Set
Macroeconometric analysis of U.S. inflation, industrial output growth, and monetary transmission mechanics using Vector Autoregression modeling & IRFs developed in R.

This project was made by using and analyzing the monthly macroeconomic data provided from the https://fred.stlouisfed.org/ database.


## Approach 
This analysis is done using VAR to see what connections exist between various macroeconomic dynamics, and examines 3 times series to do so. 


1. **Stationarity**: All 3 integrated-time series are made stationary through either log-differencing (which produces percent inflation & industrial output growth) or simple first differencing (percent change in the effective Federal Funds Rate).

2. **VAR Estimation**: Determine optimal lag order ($p$) using Akaike's information criterion and estimate the VAR($p$).

3. **Orthogonal IRFs**: Use the Cholesky decomposition to estimate **Orthogonalized Impulse Response Functions ** via bootstrapped confidence intervals to identify how shocks to the federal funds rate disperse through the macroeconomy.

