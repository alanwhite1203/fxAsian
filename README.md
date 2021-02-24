#FX Asian Option Introduction and Valuation Practical Guide


	Overview
An FX Asian option or Asian currency option is a special type of option contract where the payoff depends on the average of the underlying exchange rates over a certain period of time. The payoff is different from the case of a European option or American option, where the payoff of the option contract depends on the underlying FX rate at exercise date. 
Asian FX options allow the buyer to purchase or sell the underlying foreign exchange rate at the average rate instead of the spot rate. Asian options are commonly seen options over the OTC markets. Average rate options are less expensive than regular options and are arguably more appropriate than regular options for meeting some of investment needs. Average can be calculated in a number of ways (daily, weekly, monthly, etc.). 
One advantage of Asian options is that they reduce the risk of market manipulation of the underlying instrument at maturity. Another advantage of Asian options involves the relative cost of Asian options compared to European or American options. Because of the averaging feature, Asian options reduce the volatility inherent in the option; therefore, Asian options are typically cheaper than European or American options.
Asian options have relatively low volatility due to the averaging mechanism. They are used by traders who are exposed to the underlying asset over a period of time. The arithmetic average rate options are generally used to smooth out the impact from high volatility periods or prevent rate manipulation near the maturity date, which makes the options less expensive.
Currency options are one of the most common ways for corporations, individuals or financial institutions to hedge against adverse movements in exchange rates. Corporations primarily use FX options to hedge uncertain future cash flows in a foreign currency. The general rule is to hedge certain foreign currency cash flows with forwards, and uncertain foreign cash flows with options. 

Options give market participants many opportunities to limit risk and increase profit. Currency market fluctuations can have a lasting impact on cash flow whether it is buying a property, paying salaries, making an investment or settling invoices. By utilizing FX Asian Options, business can protect themselves against adverse movements in exchange rates. This presentation provides an overview of FX Asian option product and valuation. 

	Asian Option Introduction
	An Asian option or average option is a special type of option contract  where the payoff depends on the average rate of the underlying asset over a certain period of time 
	The payoff is different from the case of a European option or American option, where the payoff of the option contract depends on the price of the underlying asset at exercise date.
	Asian options allow the buyer to purchase (or sell) the underlying asset at the average price instead of the spot price.
	Asian options are commonly seen options over the OTC markets.
	Average price options are less expensive than regular options and are arguably more appropriate than regular options for meeting some of the needs of corporate treasurers.
	Average can be calculated in a number of ways (daily, weekly, monthly, etc.).


	The Use of Asian Options
	One advantage of Asian options is that they reduce the risk of market manipulation of the underlying instrument at maturity. 
	Another advantage of Asian options involves the relative cost of Asian options compared to European or American options. Because of the averaging feature, Asian options reduce the volatility inherent in the option; therefore, Asian options are typically cheaper than European or American options.
	Asian options have relatively low volatility due to the averaging mechanism. They are used by traders who are exposed to the underlying asset over a period of time
	The arithmetic average rate options are generally used to smooth out the impact from high volatility periods or prevent rate manipulation near the maturity date, which makes the options less expensive.
	Currency options are one of the most common ways for corporations, individuals or financial institutions to hedge against adverse movements in exchange rates. 
	Corporations primarily use FX options to hedge uncertain future cash flows in a foreign currency. The general rule is to hedge certain foreign currency cash flows with forwards, and uncertain foreign cash flows with options. 


	Valuation
	The payoff of an average rate call is max(0, Xavg - K) and that of an average price put is max(0, K- Xavg), where Xavg  is the average rate of the underlying asset calculated over a predetermined averaging period. 
	If the underlying exchange rate, X, is assumed to be lognormally distributed and Xave is a geometric average of the X’s, analytic formulas are available for valuing European average rate options. This is because the geometric average of a set of lognormally distributed variables is also lognormal. 
	When, as is nearly always the case, Asian options are defined in terms of arithmetic averages, exact analytic pricing formulas are not available. This is because the distribution of the arithmetic average of a set of lognormal distributions does not have analytically tractable properties.
	However, the distribution of arithmetic average can be approximated to be lognormal by moment matching technical, which leads to a good analytic approximation for valuing average price options. 
	One calculates the first three moments of the probability distribution of the arithmetic average in a risk-neutral world exactly and then fit a lognormal distribution to the moments.

M_1=∑_(i=0)^(n-1)▒β_i 
M_2=∑_(i=0)^(n-1)▒〖β_i e_i (2∑_(j=i)^(n-1)▒β_j -β_i ) 〗
M_3=∑_(i=0)^(n-1)▒〖β_i e_i^2 (β_(i )^2 e_i-3β_i e_i ∑_(j=i)^(n-1)▒β_j -3∑_(j=i)^(n-1)▒〖β_j^2 e_j+6∑_(j=i)^(n-1)▒〖β_j e_j ∑_(k=j)^(n-1)▒β_k 〗〗) 〗
where
	n	the number of fixing points still available
	t_i	the i-th fixing time
	Fi	the forward rate at time t_i
	αI	the weight of Fi
	β_i=α_i F_i
	v_i	the effective volatility at time t_i where v_i^2 t_i=∫_0^(t_i)▒〖σ^2 (s)ds〗
	e_i=exp⁡(v_i^2 t_i)
	

	The sifted lognormal parameters are

y_1=(M_2-M_1^2)/(z-(M_2-M_1^2)/z)
y_11=M_2-M_1^2+y_1^2
δ=M_1-y_1
z=((μ_3+√(μ_3^2+4μ_2^3 ))/2)^(1/3)
μ_3=M_3-3M_1 (M_2-M_1^2 )-M_1^3

	By assuming that the average asset price is lognormal, you can use Black's model to price an Asian option.
	The present value of an Asian call option is given by

〖PV〗_C=(y_1 N(d_1 )-(K-ψA-δ)N(d_2))D
d_1=ln(√(y_11 )/(K-ψA-δ))/(√(ln⁡(y_11/y_1^2 )))
d_2=d_1-√(ln⁡(y_11/(y_1^2 )))
where 
D=D(0,T) 	the discount factor
N 		the cumulative standard normal distribution function
T		the maturity date
ψ		the sum of weights corresponding to spent fixing periods
A		the spent average
K		the strike

                                                            
	The present value of an Asian put option is given by

〖PV〗_p=((K-ψA-δ)N(〖-d〗_2 )-y_1 N(-d_1 ))D


	A Real World Example

Name	Value	Fixing Date	Fixing Value
Reporting Currency	USD	1/6/2017	1.2283
Average Type	Rate	1/13/2017	1.2219
Call Put	Put	1/20/2017	1.236
Buy Sell	Sell	1/27/2017	1.2554
Delivery Type	Cash	2/3/2017	1.2481
Base Currency	GBP	2/10/2017	1.2486
Base Currency Notional	9300000	2/17/2017	1.24635
Underlying Currency	USD	2/24/2017	1.24575
Underlying Currency Notional	11490150	3/3/2017	1.2298
Trade Date	1/5/2017		
Maturity Date	3/31/2017		
Settlement Date	4/4/2017		
Strike and Spot Quotation	USD/GBP		
Strike Value	1.2355		
Instrument	GBP/USD		
Fixing Date	3/3/2017		



You can find more details at
https://finpricing.com/lib/IrCurveIntroduction.html
