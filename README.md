# Overview
Glad to see you here! :) \
This is the final course project of Stochastic Modelling in Finance. This project focused on option pricing and the nature of options. 
## Data Description
>The research objects were six options whoes underlying asset is **SPX and SPY index** with three different maturity dates (2020-12-18, 2021-01-15, 2021-02-19).\
>Assume the initial prices of two underlying assets are $3662.45 and $366.02 respectively on 2020-12-01.
## PART I Analytical Option Formulae
Introduce four different option pricing methods in this part to calculate the price of vanilla call/put option and two kinds of exotic options (Cash-or-Nothing and Asset-or-Nothing):
* Black-Scholes Model
* Bachelier Model
* Black 76 Model
* Displaced Diffusion Model
## PART II Model Calibration
Implied volatility is a vital indicator in option research. Visualize implied volatility of these six options through volatility smile curve. The bottom of the volatility smile is at-the-money options, which means for all kinds of options in the market, in-the-money options, and out-of-the-money options have higher implied volatility than at-the-money options. 
* For Different Maturities
  > Shorter expiries will have higher implied volatility, and volatility smile is steeper for options with shorter maturities and flatter for options with longer maturities.
* Displaced-Diffusion Model and SABR model Calibration 
  > In the Displaced-Diffusion model, the parameter β assumes a pivotal role in tailoring the implied volatility skew, facilitating a nuanced calibration of the observed market dynamics. A β close to zero implies a negligible displacement effect, rendering the model akin to the Bachelier Model, yielding a straight line on implied volatility. Conversely, a β nearing one aligns the model more closely with the Black-Scholes Model, and produces a volatility smile, capturing varying implied volatility with strike prices and potential fat tails. \
  > In SABR model, The ρ parameter signifies the correlation between an asset's volatility and the forward rate. When ρ is negative, it results in heightened volatility during declines in stock prices, expanding the left tail of the probability density. This leads to a fat left tail and a thin right tail in the return distribution. Conversely, a positive ρ produces the opposite effect. Because of this characteristic, determining ρ allows financial institutions to enhance their understanding and management of risks associated with interest rate derivative positions, given its sensitivity to volatility changes. ν is a key factor in capturing the market's perception of volatility dynamics. Financial markets experience varying levels of volatility over time, and the inclusion of ν allows the SABR model to accurately represent these fluctuations. This parameter is particularly significant in assessing the tails of return distributions. Higher values of ν contribute to fatter tails, indicating an increased probability of extreme market events, while lower values suggest a reduced likelihood of such occurrences.
## PART III Static Replication
* Static Replication\
  When static replication returns the same price across different models, it implies that the replication portfolio, composed of simpler instruments, has been constructed in such a way that its value matches the value of the more complex instrument consistently across different pricing models.
* “Model Free” Integrated Variance\
  The SABR model exhibits higher volatility and variance than the Black-Scholes and Bachelier models, mainly due to its more complex approach to volatility. Unlike Black-Scholes, which assumes constant volatility, and Bachelier, based on normal distribution, SABR introduces stochastic volatility, where volatility itself is a dynamic, random process. This allows SABR to reflect market realities more accurately, particularly in accommodating the volatility smile—a variation of implied volatility with strike price and maturity. The model's beta parameter provides flexibility in mimicking various asset price distributions, ranging from geometric Brownian motion to normal processes. Additionally, the inclusion of a correlation factor (rho) between asset price and volatility can lead to higher variances, especially in volatile market conditions.
## PART IV Dynamic Hedging
Reference: [QUANTITATIVE STRATEGIES RESEARCH NOTES from GS](http://pricing.free.fr/docs/when_you_cannot_hedge.pdf)\
In this part, simulate stock price processes under the Black-Scholes dynamic Delta hedging, ensuring that the portfolio is Delta neutral, and consequently hedging the exposure of call position using the underlying stock and the risk-free bond over time until maturity. Suppose S0 = $100, σ = 0.2, r = 5%, T = 1/12 and K = $100. 








  
