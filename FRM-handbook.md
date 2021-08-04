

##
- Cholesky factors

##

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

#### 4.3 MULTIPLE SOURCES OF RISK

- generate N joint values of ε that display the correlation structure V(ε) = E(εε') = R.
- R: symmetric real matrix can be decomposed into its so-called Cholesky factors:
- perform a statistical decomposition of the covariance matrix
  - A widely used method for this is the principal component analysis (PCA),

#### 5.1 REAL DATA

- volatility clustering: risk changes in a predictable fashion.

- efficient markets: any change in the asset price must be due to news,
- random walk: conditional distribution of returns depends on only current prices,
  - distribution of returns is constant over time, the variables are said to be independent and identically distributed (i.i.d.).

- time aggregation
  - extension to a multiple period follows a square root of time rule.
  - trend: longer-term volatility increases faster
  - mean reversion: more slowly

- Portfolio Aggregation @@

#### 5.2 NORMAL AND LOGNORMAL DISTRIBUTIONS

- normal VS lognormal
  - The difference between the two distributions is driven by the size of the volatility parameter over the horizon. 
  - The normal and lognormal distributions are very similar for short horizons or low volatilities.

#### 5.3 DISTRIBUTIONS WITH FAT TAILS

- one 4 std dev per year each market; one 10 std dev per market each year
  - Every financial market experiences one or more daily price moves of four standard deviations or more each year. And in any year, there is usually at least one market that has a daily move greater than 10 standard deviations.

- a rule of thumb would be to correct the VAR measure from a normal distribution by a ratio of 1.61 to achieve the desired coverage in the presence of fat tails. 
  - Basel multiplicative factor of 3.

#### 5.4 TIME VARIATION IN RISK
- MA: can't clustering vol
- GARCH
  - conditional variance: time-varying var, indexed by time
  - innovation: pervious day's return
  - the GARCH(p, q) model has p lagged terms on historical returns and q lagged terms on previous variances.
  - persistence (a1 + b): the speed at which shocks to the variance revert to their long-run values.
  - high persistence mean shower mean reversion
  - The square root of time rule used to scale one-day returns into longer horizons is generally inappropriate when risk is time-varying.
  - annualized volatility: ```T**0.5```

- EWMA
  - decay factor on h(t-1), recent observaton vol
  - special GARCH
  - permanent persistence: Shocks to the volatility do not decay, when the persistence is 1.00.
  - undefined long-run average variance
#### 6.1 DISCOUNTING, PRESENT VALUE, AND FUTURE VALUE
- T: tenor
- discounting factor: interest rate, yield(internal rate of return)
- anual rate: need divide compounding period
- EAR(effective annual rate): percentage term  on an annual basis
  - comparable across assets
- exp(y), (1 + y/T)^T
  - y = Pt / Pt-1

#### 6.2 PRICE-YIELD RELATIONSHIP

- par bond: coupon rate = yiled
- premium bond: >
- discount bond: <
- payoff function: higer yiely lower price
- consoles/perpetual bond
- The negative of the first derivative is the dollar duration (DD):
- risk is measured as the dollar value of a basis point (DVBP)
  - DVBP = DD * deltaY = D* * P * 0.0001
  - with 0.0001 representing an interest rate change of one basis point (bp) or one-hundredth of a percent. The DVBP, sometimes called the DV01
  - The dollar value of a basis point is the dollar exposure of a bond price for a change in yield of 0.01%.

- Macaulay duration
  - (Macaulay) duration represents an average of the time to wait for all cash flows.
  - With a zero coupon, Macaulay duration is equal to maturity.
  - time weighted PV of cash flows
  - for coupon-paying bonds, Mac duration is slightly lesss than the maturity
- The modified duration is an adjusted version of the Macaulay duration, which accounts for changing yield to maturities. 
  - modif D = Mac D/(1 + y)
- Duration
  - D=T for zero-coupon bond
  - the average time to wait for each payment, weighted by the present value of the associated cash flow.
  - For bonds with fixed coupons, duration is less than maturity.
  - The duration of a long-term bond can be approximated by an upper bound, which is that of a consol with the same yield, DC = (1+y)/y.
- DD: dollar duration
  - modified DD * P0
- coupon curve duration
  - the market prices of securites with diff coupons
  - calc df
- Convexity is always positive for regular coupon-paying bonds. Greater convexity is beneficial for both falling and rising yields.
  - convexity is much greater for long-maturity bonds because they have payoffs associated with large values of t.
  - convesity is mainly driven by the cash flows far into the future

- All else equal, duration and convexity both increase for longer maturities, lower coupons, and lower yields.
- barbell portfolio: consisting if very short and very long maturity
  - greater convexity
- bullet portfolio: maturies in the same range
- the market value of each bond is obtained by multiplying the par amount by the ratio of the market price divided by 100.

#### 7.1 DERIVATIVES MARKETS

- swap: portfolios of forward
- interest rate contracts, especially swaps, are the most widespread type of derivatives.
- Counterparty risk can be addressed with a clearinghouse.
  - central counterparty (CCP) clearing
  - CCPs generally have very high credit ratings,


- All exchanges have a clearinghouse.
  - vertical integration: 1:1
  - horizontal integration: many to one

#### 7.2 FORWARD CONTRACTS

- F * (1+r*)^t = S * (1+r)^t
- dividend: Ft * ^(-rt) = St - PV(Div)
- interest rate
#### 7.3 FUTURES CONTRACTS

- Futures contracts are standardized, negotiable, and exchange-traded contracts to buy or sell an underlying asset.
  - daily Marking to market: credit risk
  - margin: buffer against future losses
    - margin call: the amount to fill up is not to the maintenance margin, but to the initial margin.
  - Volume is the number of contracts traded during the day, which is a flow item. 
  - Open interest represents the outstanding number of contracts at the close of the day, which is a stock item.
  
#### 7.4 SWAP CONTRACTS

- Swap contracts are OTC agreements to exchange a series of cash flows according to prespecified terms.  
- Typically, swaps are established for longer periods than forwards and futures.

#### 8.1 OPTION PAYOFFS

- premium: option price
- put call parity: c - p = S * e^(-dt) - K * e^(-rt)

- covered call: long stock + short call
- protective put: long stock + long put
- colar: long stock + long put with lower K + short call with higher K
- straddle: combo of call and put with same maturity and K 
- stangle: combo of call and put with diff K 
- horizontal spread: diff t
- vertical spread: diff K
- butterfuly spread: same t: profitable when S stable

#### 8.2 OPTION PREMIUMS

- premium increases with higher S in a nonlinear, convex fashion
- time value increases with the volatility of the underlying asset
- S - PV(K) <= call premium <= asset price 
- PV(K) - S <= p <= K
- never excise Americal call early, may excise put early

#### 8.3 VALUING OPTIONS

- The philosophy of pricing models consists of replicating the payoff on the instrument by a portfolio of assets.
- The BS model can be used to derive the risk-neutral probability of exercising the option.
- For risk management, however, what matters is the actual probability of exercise, also called physical probability.

- With an option on futures, the implicit income is the risk-free rate of interest.
- the probability of ending in-the-money in a risk-neutral world is N(d2),

#### 8.4 OTHER OPTION CONTRACTS

- Binary option
- Barrier options
- Asian option: average, cheaper than regular options due to lower volatility.
- Chooser option: choose call or put
- compound option: cacall, option on option
- lookback option: extreme
#### 8.5 VALUING OPTIONS BY NUMERICAL METHODS

- American option: because Monte Carlo simulations are strictly backward-looking, and cannot take into account optimal future exercise, which a binomial tree can do.

#### 9.1 OVERVIEW OF DEBT MARKETS

- domestic bonds
- foreign bonds: by government of Sweden in dollars in the United States).
- Eurobonds: a dollar-denominated bond issued by IBM and marketed in London).

- bond markets, traditionally defined as fixed-income securities with remaining maturities beyond one year, and the shorter-term money markets, with maturities below one year.

- Floating-coupon bonds, which pay interest equal to a reference rate plus a margin, reset on a regular basis; these are usually called floating-rate notes (FRNs).

- inverse floaters: coupon - 12 % - LIBOR
- Most bonds are quoted on a clean price basis, that is, without accounting for the accrued income from the last coupon.
  - 32rd
  
- Actual payments, however, must account for the accrual of interest. This is factored into the gross price, also known as the dirty price,
  - accrued interest (AI) = coupon x (actual days since last coupon / actual days between last and next coupon)
- accrued interest in the LIBOR market is based on actual/360.
- annualized discount rate (DR) = (Face - P) / Face x(360/t)
- Just before the reset date, we know that the coupon will be set to the prevailing interest rate. The FRN is then similar to cash, or a money market instrument, which has no interest rate risk and hence is selling at par with zero duration. after the reset date, the investor is locked into a fixed coupon over the accrual period. The FRN is then economically equivalent to a zero-coupon bond with maturity equal to the time to the next reset date.
#### 9.3 PRICING OF FIXED-INCOME SECURITIES
- Fixed-income securities can be valued by, first, laying out their cash flows and, second, computing their net present value (NPV) using the appropriate discount rate.
- The yield is also the expected rate of return on the bond, provided all coupons are reinvested at the same rate.

- Movements in interest rates also create reinvestment risk. This risk can be avoided only by investing in zero-coupon bonds, which do not make intermediate payments.
- For risk management purposes, it is better to consider the spot rates as the risk factors rather than the rate of return on price.
- forward rates can be viewed as market-implied forecasts of future spot rates.
- the T-period spot rate can be written as a geometric average of the spot and consecutive one-year forward rates:
- Fx,y = yRy - xRx = Py/Px

- The par yield can be viewed as a weighted average of spot rates.
- the coupon yield cuve is an average of the spot zero coupon curve
- In an upward-sloping term structure environment, the forward curve is above the spot curve, which is above the par yield curve. According to the expectations hypothesis, this implies a forecast for rising interest rates.

#### 9.4 FIXED-INCOME RISK

- Using the duration approximation, the volatility of the rate of return in the bond price can be related to the volatility of yield changes
  - vol(R) = D* vol(yield)
- zero-coupon bond will always trade below par


#### 10.1 FORWARD CONTRACTS

- Forward rate agreements (FRAs) are over-the-counter (OTC) financial contracts that allow counterparties to lock in an interest rate starting at a future time.

- 1 × 4. The first number corresponds to the first settlement date, the second to the time to final maturity.
- Vt = (St - F) * period * Notional * PV($1)
  - PV($1) = $1 / (1 + St * period)
  - St: the prevailing spot rate during the period, settlement date
- A long FRA position benefits from an increase in rates. A short FRA position is similar to a long position in a bond. Its duration is positive and equal to the difference between the two maturities.

#### 10.2 FUTURES

- Eurodollar futures are futures contracts tied to a forward LIBOR rate.
- Pt = 10,000 * \[100 - 0.25*(100-FQt)] = 10,000 * \[100 - 0.25 * Ft]
  - FQt = 100 - Ft, FQt is the quoted Eurodollar futures price.
- because the change in the price is related to the interest rate by a factor of 0.25, this contract has a constant duration of three months. 
- It is useful to remember that the DV01 is $10,000 × 0.25 × 0.01 = $25.
- Interest rate futures contracts are designed to move like a bond, that is, to lose value when interest rates increase. 

- Future rate = forward rate + 0.5 * vol * maturitu of future * underlying rate


- T-bond futures are futures contracts tied to a pool of Treasury bonds that consists of all bonds with a remaining maturity greater than 15 years (and noncallable within 15 years).
- Cost = Price - Futrue Quote * CF(coversion factor)
- High-coupon bonds have higher CFs. Also, because the coupon is greater than 6%, the CF is greater than one.
- Note how the CF adjustment brings the cost of all bonds much closer to each other than their original prices.

- When the term structure is upward sloping, the opposite occurs, and there is a tendency for long-term bonds to be delivered.

#### 10.3 SWAPS

- absolute/comparative advantage => mutual advantage
- Swaps can be quoted in terms of spreads relative to the yield of similar-maturity Treasury notes.
  - the swap should trade at a positive credit spread to Treasuries.
  - swap rates form the basis for the swap curve, which is also called the par curve, because it is equivalent to yields on bonds selling at par.

- We can price the swap using either of two approaches: taking the difference between two bond prices or valuing a sequence of forward contracts.

- A position in a receive-fixed swap is equivalent to a long position in a bond with similar coupon characteristics and maturity offset by a short position in a floating-rate note. Its duration is close to that of the fixed-rate note.
#### 10.4 Options

- By purchasing the cap, the issuer ensures that the cost of capital will not exceed the capped rate. Such caps are really a combination of individual options, called caplets.
- The payment on each caplet is determined by CT, the notional, and an accrual factor. Payments are made in arrears, that is, at the end of the period.
- cap/floor
- collar: long cap + short floor = long pay-fixed swap
- flat/spot volatilities
- swaptions
  - 1Y × 5Y swaption. This gives the owner the right to enter in one year a long or short position in a five-year swap.
  - In practice, swaptions are traded in terms of volatilities instead of option premiums.

- options in Eurodollar future
- options on T-bond future
  - Notional multiple Max 

#### 11.1 EQUITIES

- Equity
  - residual claims
  - limited liablity
- preferred stocks
  - junior to bonds, but senior to common stocks.
  - Preferred stocks usually have no voting rights
  - offsetting tax advantage, 30%

- Gordon growth model
- Equity risk arises from potential movements in the value of stock prices.
- Concentration refers to the proportion of the index due to the biggest stocks.

#### 11.2 EQUITY DERIVATIVES

- Stock index futures
  - cash-and-carry relationship with index
    - F * exp(-rt) = S * exp(-yt)
- equity swaps are agreements to exchange cash flows tied to the return on a stock market index in exchange for a fixed or floating rate of interest.

- Because principals on currency swaps are in different currencies, they need to be exchanged. In contrast, the principal amounts for interest rate swaps are in the same currency and are not exchanged.


#### 11.56 Commodity derivatives
- Agricultural products, including grains and oilseeds (corn, wheat, soybeans), food and fiber (cocoa, coffee, sugar, orange juice) 
- Livestock and meat (cattle, hogs) 
- Base metals (aluminum, copper, nickel, zinc) Precious metals (gold, silver, platinum) 
- Energy products (natural gas, heating oil, unleaded gasoline, crude oil) 
- Weather derivatives (temperature, hurricanes, snow) Environmental products (CO2 allowances)


- Backwardation: discount forward, higher yield, demand immediate consumption
- A market is said to be in backwardation (or inverted) when forward prices trade at a discount relative to spot prices. This implies that the convenience yield is greater than the interest rate y > r. In other words, a high convenience yields puts a higher price on the cash market, as there is great demand for immediate consumption of the commodity.
- The market is said to be in a contango when the futures price trades at a premium relative to the spot price.

### Risk Models
- Modern risk management is position-based. This is more forward-looking than return-based information.

- VaR on portoflio level
- Ideally, risk should be measured at the top level of the portfolio or institution. This has led to a push toward risk measures that are comparable across different types of risk. One such summary measure is value at risk (VAR). VAR is a statistical measure of total portfolio risk, taken as the worst loss at a specified confidence level over the horizon.


1. Collect the portfolio positions and map them onto the risk factors. 
2. From market data, construct the distribution of risk factors (e.g., normal, empirical, or other). 
3. Construct the distribution of portfolio returns using one of the three methods (parametric, historical, Monte Carlo), and summarize the downside risk with VAR.


The risk manager can easily submit the current portfolio to various scenarios, which are simply predefined movements in the risk factors. Therefore, stress tests are simple extensions of VAR systems.

CVAR indicates the potential loss if the portfolio is “hit” beyond VAR. Because CVAR is an average of the tail loss, one can show that it qualifies as a subadditive risk measure.
- also called expected shortfall, tail conditional expectation, conditional loss, or expected tail loss.

- For most applications, VAR is simply a benchmark measure of downside risk. If so, what really matters is consistency of the VAR confidence level across trading desks or time.

- In practice, the horizon cannot be less than the frequency of reporting of profits and losses (P&L). Typically, banks measure P&L on a daily basis, and corporates on a longer interval (ranging from daily to monthly). This interval is the minimum horizon for VAR.

- Local valuation methods make use of the valuation of the instruments at the current point, along with the first and perhaps the second partial derivatives. 
  - Analytical method: linear/nonliear model
- Full valuation methods, in contrast, reprice the instruments over a broad range of values for the risk factors.
  - Historical, Monte Carlo
  - requires repricing the asset.
  - stress tests require full valuation.

Market Risk Charge (MRC) that is based on the bank's internal VAR measures. The original rules, as laid out in 1996, require the following parameters: A horizon of 10 trading days, or two calendar weeks A 99% confidence interval An observation period based on at least a year of historical data and updated at least once a quarter
 





















