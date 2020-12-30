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
- mean: central tendency, or center of gravity of the population.
- quantile: the cutoff point x with an associated probability c
- median: 50% quantile
- variance: the squared dispersion around the mean,
- skewness: the scaled third moment, describes departures from symmetry
  - negative -> left
- kurtosis: The scaled fourth moment, describes the degree of flatness of a distribution, or width of its tails.
  - leptokurtic, or fat-tailed, high peak > 3
  - 3, normal
  - platykurtic, < 3
  
#### 2.2 MULTIVARIATE DISTRIBUTION FUNCTIONS

- marginal density:
- conditional density: Bayes' rule.
- covariance: comovement
- correlation coefficient: scale the covariance into a unitless number
  - Independence implies zero correlation, but the reverse is not always true.

#### 2.3 FUNCTIONS OF RANDOM VARIABLES
- E
  - product: + cov
- V
  - linear tranf: drop constant
  - sum: + cov
  - portf: w' * cov matrix * w
- For general density functions and transformations, risk managers turn to numerical methods, especially when the number of random variables is large.

#### 2.4 IMPORTANT DISTRIBUTION FUNCTIONS

- uniform: 
  - As any cumulative distribution function ranges from zero to unity, we first draw X from U(0, 1) and then compute y = F−1(x). The random variable Y will then have the desired distribution f(Y).
- normal
  - skewness: 0
  - +/-e: 95
  - stable under addition: a linear combination of jointly normally distributed random variables has a normal distribution.

- lognormal: 
  - A random variable X is said to have a lognormal distribution if its logarithm Y = ln(X) is normally distributed.
  - X = EXP(Normal)
  - X = P1/P0
- student t

#### 3.1 PARAMETER ESTIMATION

- significance level: 1 - confidence level
- se(m) = vol/ (T)-1
- se(vol^) = vol / (2T) -1
- type1 err: rejeact true
  - The type I error rate or significance level is the probability of rejecting the null hypothesis given that it is true. 
- type2 err: accept false


#### 3.2 REGRESSION ANALYSIS
- param meaning
- explain the eq


- Ordinary Least Squares (OLS) Estimation; estimators provide the least sum of squared errors.
- Cov(y, x) = beta x V(x)
- R^2: the regression R-squared
  - the coefficient of determination.
  - p(y, x)^2: R-squared is also the square of the usual correlation coefficient
  - 1: fit excellent
  - 1 - V(e)/V(y) = beta^2 V(x) /V(y)
  - the contribution of independent var * beta
- A smaller p-value means that there is stronger evidence in favor of the alternative hypothesis




- Autoregression: is a regression of a variable on a lagged value of itself,
  - Autocorrelation changes normal patterns in risk across horizons. When there is no autocorrelation, risk increases with the square root of time. With positive autocorrelation, shocks have a longer-lasting effect and **risk increases faster than the square root of time**.

- multicollinearity: two variables xi can be highly correlated

- Problems with **efficiency** arise when the estimation does not use all available information. For instance, the residuals can have different variances across observations, in which case we have **heteroskedasticity**. This is the opposite of the constant variance case, or **homoskedasticity**.

#### 4.1 SIMULATIONS WITH ONE RANDOM VARIABLE

- Markov process: a particular stochastic process independent of its past history; the entire distribution of the future price relies on the current price only.
  - The Ito process.

- geometric Brownian motion (GBM)
  - As the limit of this model is a normal distribution for dS/S = dln(S), S follows a lognormal distribution.
  - S(t + 1) = S(t) + S(t)x(mean x deltaT + vol x e x deltaT^-0.5)

- equilibrium models
  - lognormal model: r = 1
  - Vasicek model: rate = 0
  - Cox, Ingersoll, and Ross (CIR) model: r = 0.5
- no-arbitrage models are designed to be consistent with today's term structure.
  - Ho and Lee model
  - Hull and White model: incorporate mean reversion
  - Heath, Jarrow, and Morton model: volatility is a function of time.
#### 4.2 IMPLEMENTING SIMULATIONS

- risk management uses physical distributions, whereas pricing methods use risk-neutral distributions.
- Since Monte Carlo simulations involve independent draws, one can show that the standard error of statistics is inversely related to the square root of K.

Financial Risk Manager Handbook: 625 (Wiley Finance) (p. 93). Wiley. Kindle Edition. 











