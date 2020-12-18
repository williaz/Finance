- The function of the risk manager is to evaluate financial risks using both quantitative tools and judgment.
- standard deviation/volatility is a measure of dispersion around the mean.

- absolute risk
  - initial value of the investment
- relative risk
  - benchmark
  - after accounting for the effect of inflation
  - TEV x P (Tracking error volatility)
  
  
- Bad luck VS a Flaw in the risk model
### Risk category
- Known knowns
  - properly identified and measured
  - Losses due to bad luck or portfolio decisions should not happen too often
  - backtesting to detect
- Known unknowns
  - model risk
    - model weakness
    - stess tests to shock finanacial var or model beyond typical ranges
  - liquidity risk
    - instrinsic liquidity of the asset
    - size of the position
 - Unknown unknowns
   - regulatory risk
   - counterparty risk
   - liquidity risk due to similiar traders
   - Knightian uncertainty: massive ctrpty failure or systemic risk 
### Risk Management Failures

- tasks:
  - Identifying all risks faced by the firm
  - Assessing and monitoring those risks 
  - Managing those risks if given the authority to do so 
  - Communicating these risks to the decision makers

## PORTFOLIO CONSTRUCTION
### Comparing Multiple Assets

- we observe a trade-off between higher risk and higher return. Without risk measures, deciding where to invest would be difficult.
- a bank must decide how much leverage to assume, as defined by the amount of assets divided by the amount of equity on its balance sheet.

### Risk-Adjusted Performance Measurement

- the Sharpe ratio (**SR**), which is the ratio of the average rate of return, μ(RP), in **excess** of the risk-free rate RF, to the absolute risk:
- The Sharpe ratio focuses on total risk measured in absolute terms. This approach can be extended to include VAR in the denominator instead of the volatility of returns.
- The information ratio (IR) is the ratio of the average rate of return of portfolio P in excess of the benchmark B to the TEV:
  - An information ratio of 0.50 is typical of the performance of the top 25th percentile of money managers and is considered “good.”
  - TEV does not adjust for average returns.
### 1.3.3 Mixing Assets 
- asset allocation
- correlation coefficient

### 1.3.4 Efficient Portfolios

- assumption that all assets follow a jointly normal distribution.
- the efficient set
- the locus of points

### 1.4.1 CAPM

- Beta: systematic risk, exposure to market factor
- Alpha: intercept, actively management skill
- mapping: a widely used process in risk management. Mapping replaces individual positions by a smaller number of exposures on fundamental risk factors.

- the mean-variance efficiency of the market implies a linear relationship between expected excess returns and the systematic risk of all stocks in the market portfolio.
- TR, Treynor ratio, penalize for high beta, fot well-diversified
- SR, undiversified portfolio
- Jensen's alpha: CAPM
- the CAPM assumes that (1) investors have homogeneous expectations, (2) distributions are normal, (3) capital markets are perfect, and (4) markets are in equilibrium.

#### 1.4.2 APT

- highly granular: sufficient num of common factors is identified, and well-diversified portfolio
- PCA: principal component analysis, best fit to the correlation matrix of asset returns

#### 1.6 formula
- TEV: vol diff with benchmark, corr
- Absolute risk: port * vol of return
- relative risk: TEV * port
- SR(Sharpe): risk-free, own vol
- IR: benchmark, TEV
- TR(Treynor) risk free, Beta
- Jenson's alpha: return diff with risk free and beta multiply exceeding (market - risk-free)
- CAPM: systemic risk, exceeds risk free, beta
- APT                                                    
- CML(capital market line): the highest Sharpe ratio of any portfolio on the efficient frontier.

#### 2.1
- cumulative distribution function: <=
- p.d.f(probabulty density function): =
- A random variable is characterized by its distribution function, it is convenient to summarize it by a few param(moments)




