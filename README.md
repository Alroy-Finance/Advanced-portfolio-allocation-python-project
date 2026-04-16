**Overview**  
This project implements a portfolio optimization model based on Modern Portfolio Theory (MPT) to construct an optimal portfolio that maximizes risk-adjusted returns.
Unlike basic models, this version incorporates real-world constraints such as asset diversification limits and sector exposure control, making the output more practical and aligned with institutional portfolio management approaches.

**Objectives**  
Build an optimal portfolio using historical market data.  
Maximize Sharpe Ratio using mean-variance optimization.  
Incorporate real-world investment constraints.  
Enable dynamic user input for asset selection.    
Visualize risk-return trade-offs using the Efficient Frontier.

**Tools & Technologies**  
Python, Pandas, NumPy, Matplotlib, SciPy, Data Source: Yahoo Finance

**Key Features**  
Accepts 5 user-defined stock tickers  and validates inputs using live market data.    
Incorporates user-defined risk-free rate and calculates true Sharpe Ratio.     
Maximum allocation per asset is 40% and prevents over-concentration in a single stock.      
Automatically fetches sector data using API and maximum exposure per sector is capped at 60%.     
Simulates thousands of portfolios, plots risk vs return and highlights optimal portfolio  

**Methodology**  
Collect historical stock data.  
Compute daily returns and covariance matrix.  
Define portfolio performance (return & volatility).  
Optimize weights using Sharpe Ratio maximization.  
Apply constraints:  
    - Fully invested portfolio (weights sum to 1)  
    - Asset cap (≤ 40%)  
    - Sector cap (≤ 60%)  
Generate Efficient Frontier

**Sample Output**  
<img width="655" height="232" alt="image" src="https://github.com/user-attachments/assets/eba1702d-c009-4093-9c13-b5291bd1fcef" />
<img width="671" height="612" alt="image" src="https://github.com/user-attachments/assets/e5b54796-3f0c-4710-8038-0830c6532163" />


**Key Insights**    
Constrained optimization produces more realistic portfolios compared to unconstrained models.  
Diversification constraints reduce concentration risk.  
Sector balancing improves robustness against industry-specific shocks.  
There is a clear trade-off between return and risk along the Efficient Frontier.  

**Limitations**  
Model relies on historical data (backward-looking).  
Assumes returns follow a normal distribution.  
Sector data retrieval may occasionally default to "Other".  

**Author**  
Alroy Fernandes  
LinkedIn: linkedin.com/in/alroy-fernandes-ab0335153/
