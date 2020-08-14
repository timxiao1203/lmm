AN EFFICIENT LATTICE ALGORITHM FOR THE LIBOR MARKET MODEL


ABSTRACT
The LIBOR Market Model has become one of the most popular models for pricing interest rate products. It is commonly believed that Monte-Carlo simulation is the only viable method available for the LIBOR Market Model. In this article, however, we propose a lattice approach to price interest rate products within the LIBOR Market Model by introducing a shifted forward measure and several novel fast drift approximation methods. This model should achieve the best performance without losing much accuracy. Moreover, the calibration is almost automatic and it is simple and easy to implement. Adding this model to the valuation toolkit is actually quite useful; especially for risk management or in the case there is a need for a quick turnaround.

V.	CONCLUSION
In this paper, we proposed a lattice model in the LMM to price interest rate products. Conclusions can be drawn, supported by the previous sections. First, the model is quite stable. The fast convergence behavior requires fewer discretization nodes. Second, this model has almost equivalent accuracy to the current pricing models in the market. Third, the implementation of the model is relatively easy. The calibration is very simple and straightforward. Finally, the performance of the model is probably the best among all known approaches at the time of writing.
We use the following techniques in our model: shifted forward measure, drift approximation, probability distribution structure exploitation, long jump, numerical integration, incomplete information handling, and calibration. Combining these techniques, the model achieves sufficient accuracy in relatively few time steps and discrete nodes, which makes it a very efficient method.
For ease of illustration, we present the lattice model based on the Trapezoidal Rule integration. A better but slightly more complicated solution is to spline the payoff functions. The cubic spline of the option payoffs can achieve higher accuracy, especially for Greeks calculations, and higher speed. Although cubic spline takes some time, the lattice will require much fewer nodes (23 ~ 28 nodes are good enough) and can perform a much faster integration. In general, the spline method can provide a speedup factor around 3 ~ 5 times.
We have implemented the lattice model to price a variety of interest rate exotics. The algorithm can always achieve a fast convergence rate. The accuracy, however, is a bit trickier, depending on many factors: drift approximation approaches, numerical integration schemes, volatility selections, and calibration, etc. Some work, such as calibration, is more of an art than a science.

REFERENCE
Amin, K. “Jump diffusion option valuation in discrete time.” Journal of Finance, Vol. 48, No. 5 (1993), pp. 1833-1863.

Brace, A., D. Gatarek, and M. Musiela. “The market model of interest rate dynamics.” Mathematical Finance, Vol. 7, No. 4 (1997), pp. 127-155.

Brigo, D., and F. Mercurio. “Interest Rate Models – Theory and Practice with Smiles, Inflation and Credit.” Second Edition, Springer Finance, 2006.

Das, S. “Random lattices for option pricing problems in finance.” Journal of Investment Management, Vol. 9, No.2 (2011), pp. 134-152.

FinPricing, Capital market solution, https://finpricing.com/lib/FxVolIntroduction.html

Gandhi, S. and P. Hunt. “Numerical option pricing using conditioned diffusions,” Mathematics of Derivative Securities, Cambridge University Press, Cambridge, 1997.

Hagan, P. “Accrual swaps and range notes.” Bloomberg Technical Report, 2005.

Hull. J., and A. White. “Forward rate volatilities, swap rate volatilities and the implementation of the Libor Market Model.” Journal of Fixed Income, Vol. 10, No. 2 (2000), 46-62.

Martzoukos, H., and L. Trigeorgis. “Real (investment) options with multiple sources of rare events.” European Journal of Operational Research, 136 (2002), 696-706.

Piterbarg, V. “A Practitioner’s guide to pricing and hedging callable LIBOR exotics in LIBOR Market Models.” SSRN Working paper, 2003.

Rebonato, R. “Calibrating the BGM model.” RISK, March (1999), 74-79.
