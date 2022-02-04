# Malliavin calculous application in a financial context

Typically in a risk management context, we would like (at present, time 0) to estimate the risk (or more globally the law of probability) of an asset (at a future time t). All portfolios underlyings are then simulated until t. When the portfolio includes some derivatives, it is necessary to use pricers for each underlying value obtained at time t, these pricers using sometimes themselves Monte-Carlo simulations from t to the maturity time T ! Thus this normal methodology uses simulations**2, which is rather time-consuming !

As an alternative, we would like to test the estimation of conditional expectations by Malliavin calculous. Malliavin's calculous is a nice theory in stochastic analysis, which allows integration by parties, weak differentiation, for some kind of random variables, including payoffs !

The idea is to perform only one set of underlyings simulations, from 0 to T, and to estimate for each simulation path i at t, the conditional expectation E_0(phi(S)/St=St(i)), with phi the payoff and S the undelying.

Following [Lions, etc.], we test in this small prototype this estimation, using a vanilla option ; it allows us to compare the obtained result to the real law.

## references
* Applications of Malliavin Calculus to Monte Carlo Methods in Finance, II, Lions, Lebuchoux, Lasry, Fournié, Finance and stochastics, 2001
* Pricing and hedging American options by MonteCarlo methods using a Malliavin calculus approach, Bally, Caramellino, Zanette, Monte Carlo Methods and Applications, 2004.
* Introduction to Malliavin calculous, Nualart and Nualart, Cambridge university press, 2018


## Installation
* python3 -m pip install pipenv
* pipenv shell
* pipenv install
* jupyter lab
