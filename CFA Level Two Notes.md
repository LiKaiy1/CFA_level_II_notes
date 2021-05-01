# CFA Level Two Notes

*Kaiyi Li*

*NYU Stern Class of 2020*

*kaiyi.li@stern.nyu.edu*

__This note is created at *17:00, Wednesday, Janauary 1st, 2020* by Kaiyi Li. This note should contain all notes in markdown and latex format for the entire preparation of CFA level 2 by the time of exam. The preface chapter of this notebook is the corresponding study plan for CFA level 2. Contents of this notebook will be updated according to my own progress. I am not responsible for the correctness of the content in this notebook. However, discussions and suggestions are greatly appreciated. __

----------------------------------------

[TOC]

-----------------------------

# Preface:	Study Plan For CFA Level Two

- [ ] **Fixed Income**  
	- [x] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Derivatives** 
	- [x] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Alternative Investment**
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Equity Valuation** 
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Coporate Finance** 
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Quantitative Methods** 
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Economics**
	- [x] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems

- [ ] **Financial Reporting and Analysis** 
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Portfolio Management** 
	- [x] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems

- [ ] **Ethics And Professional Standards** 
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems
- [ ] **Review And Mock Exams**

------------------------------------------------------------------------------

# Fixed Income

## Spot and Forward Rates

### Spot Rate

**Rate of interest on a security that makes a single payment at a future point in time.**

#### Discount Factor

Single unit PMT matures at par.

Note that the *r* in this notation is the default risk-free rate.
$$
PV = \frac{1}{(1+r)^T}
$$
If we have spot rate, we can derive the discount factor. If we have discount rate, we can derive spot rate. 

#### Spot Curve

**A spot yield curve or a spot curve** is 

![](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/spot-interest-rate.png)

Each point on the spot curve has the following charaters:

* Default-risk-free
* Option-free
* Zero Coupon Bond.
* As maturity increase, yield also increase. The bond with the longest maturity has the highest yield.

Because **there are no coupons**, there are no reinvestment risk. The stated yield $r(T)$ is the actual realized return if held-to-maturity. 

Yield on a ZCB maturing at time T regarded as most accurate representation of the T-year interest rate.

The **market forces** would change the **market price of ZCBs**, then the yield to maturity, **r(T)**, would also move, the spot curve would therefore also move alone. Therefore, **the shape and level of curve are dynamic.** 

### Forward Rate

**Interest rate, set today, for a single-payment security to be issued at some future date.** [^1]

[1] The notation of the forward rate is 
$$
f(t_1,t_2)\\
t_1:\text{start at time } t_1\\
t_2:\text{last for time (maturity) } t_2
$$

> Forward rate Example 
>
> To calculate $f(2,1)$ , we invoke the **no arbitrage principle**:
> $$
> (f(2,1)+1)\times(1+3\%)^2 = (1+4\%)^3\\f(2,1) = 6.02\%
> $$
>
> #### 

![image-20190905030433895](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20190905030433895-7623878.png)

#### Forward Curve

If we have spot rates (spot curve), we could derive the forward rates (forward curve). **Each point on the forward curve is ** $f(T,1)$ (with only one year maturity).

![image-20190905031921187](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20190905031921187.png)

* The point on the forward curve stands for the interest rate if the loan is made at time T, each loan is for one period.

>Example
>
> The interest rate of a three year loan starting at T = 2 is 
>$$
>f(2,3) = [(1+f(2,1))\times(1+f(3,1))\times(1+f(4,1))]^\frac{1}{3}
>$$

**If the spot curve is upward sloping, the forward curve will lie above the spot curve.**

**If the spot curve is downward sloping, the downward curve will lie below the spot curve.**

**Forward Curve is the future spot curve.**

#### Forward Rate Model

$$
[1+r(T^*+T)]^{T^*+T} = [1+r(T^*)]^{T^*}[1+f(T^*,T)]^T\\
\frac{[1+r(T^*+T)]^{T^*+T}}{[1+r(T^*)]^{T^*}} = [1+f(T^*,T)]^T\\
\frac{[1+r(T^*+T)]^{T^*/T+T/T}}{[1+r(T^*)]^{T^*/T}} =[1+f(T^*,T)]\\
{[\frac{[1+r(T^*+T)]}{[1+r(T^*)]}]}^{T^*/T}[1+r(T^*+T)] =[1+f(T^*,T)]\\
$$

#### Implications

>r(3)>r(2)>r(1)-upward sloping curve
>
>implies that
>
>f(1,1)>r(2)
>
>f(1,2)>f(1,1)

### Yield to Maturity vs Spot Rate

**YTM:** **The weighted average of the spot rates used in the valuation of the bond.**

YTM = Expected return on a bond if only all following conditions meet

* Held to maturity
* All coupons/principal payments made in full
* **Coupons are reinvested at YTM rates. (Typically does not hold)**

YTM is a poor proxy for expected rate of return. 

* Interest rates are volatile. (Not reinvested at the same rate)
* Yield curve is steeply sloped up or down. (Not reinvested at the same rate)
* Significant risk of default.  (Cash Flow Differ)
* Embedded options.  (Cash Flow Differ)

###  Par-to-Spot Boostraping method

#### Par Curve

Par curve represents yields-to-maturity on coupon paying government bond priced at par.  (What the coupon paying government bonds priced at par given a series of spot rates to make PV = 100) .
$$
\frac{\frac{C}{2}}{(1+r_{0.5})^{0.5}}+\frac{\frac{C}{2}}{(1+r_{1})^{1}}+\frac{\frac{C}{2}}{(1+r_{1.5})^{1.5}}+\frac{\frac{C}{2}+100}{(1+r_{2})^{2}}  = 100
$$
The *C* we solved here is the par yield.

>Typically, on-the-run (new issued) bonds are used to create the par curve since they are typically priced ar or close to par. Therefore, their coupons could used as a proxy for par curve.

#### Example of par-to-spot

Given par curve

| Year | Par   |
| ---- | ----- |
| 1yr  | 5%    |
| 2yr  | 5.97% |
| 3yr  | 6.91% |
| 4yr  | 7.81% |

To derive spot, we have

1yr spot:
$$
1 = \frac{1.05}{1+r(1)}\\
r(1) =  5\%
$$
Then we do the 2yr spot:
$$
1 = \frac{0.0597}{1.05}+\frac{1.0597}{(1+r(2))^2}\\
r(2) = 6\%
$$
Then we do the 3yr and 4yr spot and so on.

**This method is called bootstraping because you can only calculate the spot 1 by 1**

## Riding the yield curve (Rolling down the yield curve)

Spot upward sloping $\Rarr$  forward curve lies above the spot curve

if the level/shape of the spot is not expected to change (**The spot will not elove to the forward curve**) , then **buying bond with a maturity longer than the investment horion** would provide a total return greater than the return on a maturity-matching (with the low horizon) strategy.

Wider the spread (Difference between spot curve and forward curve), longer the bond, greater the total return.

## Swap rate curve

### Definition

Price (in yield) a fixed-rate payer will pay for LIBOR flat plus or minus some points, price set so that the value of swap is always zero at inception.


$$
\text{Swap Rate} = \frac{PV(\text{Flat PMTs})}{\sum 1\times\frac{days}{360}\times df}
$$

The discount factor *df* is based on 1-period libor plus a series of forward rates derived from Eurodollar futures contract.

### Swap Curve

Swap curve is a type of par curve.  

People sometimes use swap curve instead of using government spot curve because in some market, government bond is not liquid.

Government spot curve is derived from government treasury, while swap rate is derived based on inter-bank lending. 

### Swap Spread

The spread paid by a fixed-rate payer, over the same maturity 'on-the-run' (newly issued) government security.  

>Example
>
>5-year swap rate = 2%
>
>5-year treasury = 1.7%
>
>Swap Spread = 30bps = 0.3%

$$
\text{Swap Spread} = \text{Swap Rate}-\text{Treasury rate} \\
$$

The source of swap spread comes from credit risk and liquidity risk components.

**Swap Curve**

![image-20200105172652053](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200105172652053.png) 

>What is Eurodollar Futures? (**EDF**)
>
>A **Eurodollar** future is a cash settled **futures** contract whose price moves in response to the interest rate offered on US Dollar denominated deposits held in European banks.

Because the swap curve is not engineered as the spot curve, therefore it has an expectation of risk contained in the difference between swap curve and spot curve.

If the spread increase $\Rarr$ risk aversion

If the spread decrease $\Rarr$ risk seeking

## Other Spreads

### Z-Spread

A more accurate measure of credit and liquidity risk.

>Z-spread  is a constant basis point spread that would need to be added to the implied spot yield curve so that the DCF of a bond = current price.

One could think of the Z-spread as a parrallel shift in the spot curve.
$$
\frac{PMT}{(1+r(1)+z)^1}+\frac{PMT}{(1+r(2)+z)^2}+\cdots+\frac{PMT}{(1+r(n)+z)^n} = PV
$$
Where *r* is referred as a risk-free rate.

### TED-Spread & LIBOR/OIS swap rate

TED spread is the difference between libor rate and T-bill Rate for the same maturity.

If TED spread increase $\Rarr$ Interbank risk increasing. It reflects the risk in the banking system.

LIBOR/OIS swap rate is 
$$
\text{LIBOR/OIS swap rate} = \text{LIBOR} - \text{Overnight Indexed Swap Rate}
$$
The OIS is a float interest rate of a swap calculated as 
$$
OIS = \sqrt[t]{(1+day_1)(1+day_2)(1+day_3)\cdots (1+day_t)}
$$
where $day_n$ is the overnight rate of day n in the payment period.

OIS is an indicator of risk and liqudity of the money market securities.

## Term Sturcture Theories

### Pure Expectation Theory

Foward curve is an unbiased predictor of future spot prices. Slope of the forward curve only reflects the future short-term rates.

The underlying assumpution of this theory is that **bonds of any maturity are perfect substitutes.**

### Local Expectation Theory

Local expectation has the same implication as the pure expectation. However, it restricts its range:

The exected return of all bonds is the risk free rate over the short time periods. 

>Example
>
>6 Year investment horizon
>
>The return of a 5-year bond and 12 year bond and a 30 year bond after one year is all equal.

### Reality 

The spot curve usually reflects more risk than just the risk-free rate and the forward curve is build based on the spot curve, the risk-premium will be imported to the forward curve.

The risk-premium that is contained in the spot curve is **maturity risk premium.**

Forward rate would absorb this premium and hence would then reflect a MRP in the expected future spot price. 

### Liquidity Preference Theory

**Liquidity Premium exist and increase with maturity**. Even with an expectation of unchanging short-term spot rates, the yield curve would be upward sloping. 

Even we have an upward sloping spot curve and we assume that the short-term spot rates remains unchanged, then we have a upward sloping forward curve, **but the upward sloping forward curve doesn't reflect any expectations of the future spot rate because with the existence of liquidity premium, even a flat spot curve could derive a upward sloping forward curve.**

### Segmented Market Theory

![image-20200108172146280](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200108172146280.png)

Each maturity sector can be thought of as a segmented market in which yields are determined independently from yields in other maturity segments.

**Assumption:** Market participants are unwilling/unable to invest in anything other than securities other than securities of their preferred maturity.

**Conclusion:** The forward yields are not a reflection of expected spot rates or liquidity premiums.

### Preferred Habitat Theory

Borrowers and lenders have a preference for particular maturities but that yields at different maturities are not determined independently.

**If returns are compelling in other maturities, preferences will follow.**

## Modern Term Structure Models

Quantitative descriptions of how interest rates evolve. 

* Factors
* Parameters $\Rarr$ Assumptions

### Equilibrium Term Structure Models

Describe term structure dynamics. 

Using fundamental economic variables that are assumed to affect interest rates. 

Required:

* A Drift Term
* An assumption about volatility

Can be one-factor or multi-factor. Make assumptions about the behavior of factors. And the model has to be parsimonious.

#### Cox-Ingersoll-Ross Model (CIR model)

$$
dr = a(b-r)dt +\sigma \sqrt{r}dz
$$

$dr$ means the change in rate.

$a(b-r)dt$ is the deterministic part of the model.

$\sigma \sqrt{r}dz$ is the stochastic part of the model. It captures the **volatility ** of the model.  

$r$ is observable short-term rate.

*b* is the long-run value of the short-term rate. 

$(b-r)$ we are assuming mean-reversion. 

$a$ is the speed of mean reversion. 

It appears that **in this model, the volatility is not constant**. At a high level of rate, volatility will be high, a low level of rate, volatility will be low.

#### Vasicek Model

$$
dr = a(b-r)dt +\sigma dz
$$

It has the same deterministic part of the model, but it assumes constant volatility at all levels of interest rates.

**Neither of these two models are very good at modelling observed term structure. They assumes mispricing.**

### Arbitrage-Free Model

#### Ho-Lee Model

Begin with Observed Market prices of a reference set of rates. **Assume they are priced correctly.**

The model is then calibrated so that it generates the observed reference rates. (Hence arb-free). It does not attempt to explain the observed yield curve. It takes it as given.

### Yield Curve Factor Models

#### Shaping Risk

>The sensitivity of a bonds price to the changing shape of the yield curve.
>
>For active bond management:
>
>*  Base trades on a forecasted yield curve shape. 
>
>* Hedge yield risk on a bond portfolio.

#### Factors affecting the shape of the yield curve.

>Litterman-Scheinkman 3-factor model
>
>Three Independent Factors:
>
>* Level
>* Steepness
>* Curvature

The process of LS model:

First, take 10 key rates (points along the yield curve)

Second, create a variance-covariance matrix. 

Third, try to extract *independent factors* that explain the variance-covariance matrix. 

Eventually, using PCA to creates factors that are statistically independent of each other and then interpret these factors.

##### Factors

###### Level (duration)

The move level. Responses in same direction and by similar magnitudes.

![image-20200109050614370](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200109050614370.png)

###### Steepness

Steepness lower the short yields and raises long yields.

![image-20200109050719391](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200109050719391.png)

###### Curvature (volatility)

Results display same pattern as impact of interest rate volatility on the shape of the curve.

![image-20200109051011330](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200109051011330.png)

##### Yield Curve Volatility

The term structure of interest rate volatility

![image-20200109051333310](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200109051333310.png)

The yield volatility for a zero coupon bond at each maturity. $\sigma(t,T)$

As the maturity of the bond increase, the volatility of interest rate decreases.

For the short-term bond, they are more strongly linked to uncertainty about monetary policy. For the long-term bond, they are more linked to uncertainty regarding real economy.

## Arbitrage-Free Valuation

Arbitrage is a risk less profit with zero investment. 

Pinciples of no arbitrage: Prices adjust until there are no arbitrage opportunities.

Arbitrage opportunity: The value of the whole should equal the su of the value of the parts.

Example:

>**Arbitrage-Free Valuation**
>
>Given par rates
>
>| Maturity | Par Rates |
>| -------- | --------- |
>| 1        | 2%        |
>| 2        | 3%        |
>| 3        | 4%        |
>
>A 3-year, 5% annual bond is quote at 102.77512, YTM = 4%
>
>(Estimate cash flow, select a discount rate, compute present value)
>
>First, Find the spot rates:
>$$
>100 = \frac{102}{1+r(1)}, r(1) = 2\%\\
>100 = \frac{3}{1.02}+\frac{103}{(1+r(2))^2} \ \Rarr r(2) = 3.015\% \\
>100 = \frac{4}{1.02}+\frac{4}{1.03015^2}+\frac{104}{(1+r(3))^3}\Rarr r(3) = 4.055\%
>$$
>Then, compute the present value:
>$$
>PV = \frac{5}{1.02}+\frac{5}{1.03015^2}+\frac{105}{1.04055^3}\\
>=102.8102
>$$
>Therefore, it is not an arbitrage free value. 

**It will not work with bonds with embedded options.**

### Binomial Interest Rate Tree

For option-free bonds, DCF with spot rates = arbitrage-free valuation.

Bonds with embedded options have cash flows that are interest rate dependent. 

#### lattice model

A lattice model means a tree has recombine nodes. 

![image-20200110021801810](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200110021801810.png)

#### Generate an interest rate tree

How do we move from *t=0* (root) to the node *t=1*?

We need 

* Assumpution about volatility: from historical data or implied volatility based on interest rate derivatives.
* An interest rate model: e.g- Lognormal random walk.

Higher volatility at higher rates. 

Trick: Always start with the lower nodes $i_1L$ becasuse that the lower node is always $2\sigma$ below the higher node $i_1H$. Therefore we always have $i_1H = i_1Le^{2\sigma}$ .

Then we have $i_2HL = f(2,1)$ , and $i_2LL = i_2e^{-2\sigma}$ . 

Once all the first-pass interest rates are populated, we use par yields to calibrate the tree, one time-step at a time.

Calbrate the tree (backward induction)

![image-20200111034818395](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200111034818395.png)

Example:

2-year bond, par rate is
$$
par = 1.2\%, f(1,1)  = 1.4\%, r(1) = 1\%, \sigma = 0.15
$$
Then we have
$$
1\% 0.5\cdot \frac{100.79646}{1.01}+0.5\cdot \frac{101.119}{1.01}=100.063156\begin{cases}0.5\cdot \frac{101.2}{1.4(1+\sigma)}+0.5\cdot \frac{101.2}{1.4(1+\sigma)}+1.2 = 100.79646\begin{cases}100+1.2\\100+1.2\end{cases}\\
0.5\cdot \frac{101.2}{1.4(1-\sigma)}+0.5\cdot \frac{101.2}{1.4(1-\sigma)}+1.2=101.119\begin{cases}100+1.2\end{cases}\end{cases}
$$
Since 100.063156 > 100, we need to calibrate the tree. The next iteration, we need to increase 1.19 (lower node trick). Next iteration we start the lower node at 1.192, etc.

#### Monte Carlo Simulation

Simulating a sufficiently large number of interest rate paths. Paths are generated based on some probability distribution and some assumption about volatility. 

Detail Steps:

1. Simulate numerous path
2. Generate spot rates from the simulated future.
3. Determine Cash flows along each path
4. Calculate PV for each path
5. Calculate average PV.

Add a drift term to fit the current spot curve with the average PV.

## Bond with Embedded Option

Bonds with contingency provisions that can be exercised by the holder or issuer, or automatically depending on interest rates. 

Eample. Callable bonds: 

* European Call: Issuer can only call the bond on a single date.
* American Call: Issuer can call the bond anytime within the maturity.
* Bermuda Call: Issuer can call the bond on multiple predetermined dates.

Callable bonds benefits the issuer. Putable bond benefits holder. Putable bonds typically European, sometimes Bermuda. 

Complex bonds can be bond callable and putable,  sometimes convertible. 

Extendable bonds $\Rarr$ Bond holders can extend the maturity of the bond. 

$$
\text{Value 0f Callable Bond } = \text{Value of Straight Bond} - \text{Value of Call Option}\\
\text{Value 0f Putable Bond } = \text{Value of Straight Bond} + \text{Value of Put Option}
$$

The conversion option is a convertible bond is a right held by the **bondholders**.

> Example.
>
> We have a  3-year, 4.25% annual bond. 
>
> | Par  | Spot  | Forward |
> | ---- | ----- | ------- |
> | 2.5  | 2.5   | 2.5     |
> | 3    | 3.008 | 3.518   |
> | 3.5  | 3.524 | 4.564   |
>
> The value of the bond is then
> $$
> \frac{4.25}{1.025}+\frac{4.25}{1.03008^2}+\frac{4.25}{1.03524^3} = 102.114
> $$
> But for bond with options, we shall use a better approach.
> $$
> \frac{4.25}{1.025}+\frac{4.25}{1.025\cdot1.03518}+\frac{4.25}{1.025\cdot1.03518\cdot1.04564} = 102.114
> $$
> Now the bond is callable. Assuming the $\sigma = 0$.  **Which means we can just use the forward rates given.** The bond is callable if the value of the bond is over 100.
>
> At the end of year 2, we will have 104.25. Discounted by the forward rate at that time, we would have
>
> $\frac{104.25}{1.04564} = 99.70$ and therefore the option will not be executed.
>
> At the end of year 1, we have the 
> $$
> \frac{99.70+4.25}{1.03518} = 100.417 
> $$
> At this point, the company could call the bond. 
>
> Assuming we will exercise the call at the end of year 1, for today, we have 
> $$
> \frac{100+4.25}{1.025} = 101.707
> $$
> Therefore, we have the value of the callable bond at today is 101.707. 
>
> Straight vanilla bond  is 102.114.
>
> So, the value of the call option is 102.114-101.707 = 0.407.
>
> Assuming we have a put option at the end of each year, could be executed if the value of the bond is lower than 100, assuming $\sigma = 0$. 
>
> We would have the value of the bond as 100 because 99.70<100 and thus we execute the bond. 
>
> At the end of year 1 we would have
> $$
> \frac{100+4.25}{1.03518} = 100.707
> $$
> We would have the value of the bond at today
> $$
> \frac{100.707+4.25}{1.025} = 102.397
> $$
> The value of the put is 102.397-102.114 = 0.283.

**The value of the embedded option increases with interest rate volatility.**

### Level and Shape

#### Interest rate volatility

As interest rate volatility increase, the value of a straight bond remains the same. The call option value increase, and the callable bond value decrease. The value of a put option increase.

As interest rate volatility increase, the value of a straight bond remains the same. The value of a put option increase, and the putable bond value increase. The value of a put option decrease.

#### Level (interest rate)

The value of a straight bond decrease as interest rate rises. It would be less likely to execute the call option. And therefore the value of the call option drops as interest rate increase. Vice versa: **The value of the call option increase as interest rate decrease.**

#### Yield Curve

For an upward sloping yield curve, the call option is OTM, and it has the lowest value. The put option is ITM. It has the highest value.

For a flat sloping yield curve, the call option is ATM. The put option is ATM.

For a downward sloping yield curve, the call option is ITM. Has the highest value. The put otion has the lowest value because it is OTM.

### Option-Adjusted-Spread

Extends the valuation framework to the valuation of risky bonds.

**Z-Spread: raise the one-year forward rates derived from the default-free benchmark yield curve by a fixed spread.**  

To value a risky bond, we estimate the Z-spread from the market price of suitable bonds of similar credit quality. 

>Example
>$$
>\text{Default-Free Bond:}\\
>\frac{4.25}{1.025}+\frac{4.25}{1.025\cdot 1.03158}+\frac{4.25}{1.025\cdot 1.03158\cdot 1.04564} = 102.114\\
>\text{Risky Bond:(with 100bps Z-spread)}\\
>\frac{4.25}{(1.025+0.01)}+\frac{4.25}{(1.025+0.01)(1.03158+0.01)}+\frac{4.25}{(1.025+0.01)(1.03158+0.01)(1.04564+0.01)} = 99.326\\
>$$

> The **Option Adjusted spread** is simply the **Z**- **Spread** excluding the premium to compensate for the **option** risk. Thus, the OAS is the **spread** above the treasury curve that compensates for credit and liquidity risk only. **Z**-**spread** is the all-in **spread**, meaning **spread** from the risk profile AND from the call risk.



#### OAS vs Volatility

**Option-adjusted Spread is volatility dependent. ** 

Because **the Z-Spread is constant** and 
$$
\text{Z-Spread} = \text{OAS} - \text{Option Cost}
$$
Therefore, when interest rate volatility increase, Option Value (Cost) increases, and OAS decline.

### Duration

For bonds with embedded options, only appropriate measure of duration is:
$$
D = \frac{PV_{-}-PV_{+}}{2\Delta r P_0 }
$$
**The effective duration of a callable/putable bond is always less than the effective duration of a straight bond.**
$$
D_{option\ bond} < D_{straight\ bond}
$$

#### one-side/key-rate duration

![image-20200128095311927](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200128095311927.png)

**The callable bond  is more sensitive to interest rate increases, putable bond is more sensitive to interest rate declines.**

The key rate duration is also called partial duration. The valuation of key rate duration is identical as the effective duration. But only for a given rate. 
$$
\sum_i^n \text{Key Rate Duration}_i = \text{Effective Duration}
$$

### Effective Convexity

$$
\text{Effective Convexity} = \frac{PV_-+PV_+-2PV_0}{(\Delta r)^2\cdot PV_0}
$$

> For an option-free bond and putable bond, it always has a positive convexity. 
>
> For callable bond, it has a negative convexity (at a lower rate). 

**If a bond is not a par bond, then an interest shift will affect all par rates.**   

**The effective convexity of a callable bond turns negative when the embedded option is near the money.**

### Capped/Floored Floaters

* Cap provision protects the coupon rate from increasing above a specified maximum rate. 

* $$
	\text{Value of Capped Floater} = \text{Value of Straight Bond}-\text{Value of Embedded Options}
	$$

* Floored Floaters prevents coupon from decreasing below a specified minimum.

* $$
	\text{Value of Floored Floater} = \text{Value of Straight Bond}+\text{Value of Embedded Options}
	$$

### Covertible Bonds

**Covertible bonds are hybrid security. They are straight bond plus a call option on common stock.** 

Holder has the right to convert debt to equity during a conversion period at a conversion price. 

Issuer can pay a lower coupon because if the bond is converted, no principal repayment. 

#### Components of Value

* Conversion Value (Parity Value) 
	$$
	CV = P_0 \times CR
	$$
	$P_0$ is the current share price while CR is the conversion ratio.

* Minimum Value (floor value) of  a convertible bond is
	$$
	max\{\text{Conversion Value},\text{Value of the underlying straight bond}\}
	$$

* Market Conversion Premium Per Share
	$$
	MCP/Sh = \frac{PV_0}{CR} - P_0
	$$
	Note that the $PV_0$ is the current bond price.  And $\frac{PV_0}{CR}$ is the market conversion price. 

* The MCP ratio is $\frac{MCP/Sh}{P_0}$ .

* Premium Over Straight Value 
	$$
	\text{Premium Over Straight Value} = \frac{PV_0}{\text{Straight Value} }-1
	$$

#### Risk And Return Characteristics

![image-20200128204910227](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200128204910227.png)

## Credit Analysis Models

### Terminology

Credit-spread is the difference of Corporate Bond YTM over Benchmark Bond YTM. When the benchmark is government, it is then called **G-Spread**. Assuming no liquidity or taxation differences.

**Default risk ** is the likelihood of an event of default (the probability of default). 

**Default risk premium** reflects uncertainty in timing of default. 

**Credit Risk**  is given default, how much is likely to be lost. (**Lost Given Default**). 

**Expected Expossure** the amount of money that could be lost in default without considering any recovery.

>Example of expected expossure. 
>
>1 year, 4% bond at par. The expected expossure = 104.

**Recovery Rate** is the percentage of **expected expossure** recovered in default. 

**Loss severity** = 1 $-$ Recovery Rate

### Valuation 

> Example
>
> Face Value = 100. If not default, we have 104. If default we have 41.6. Risk free rate is 3%. POD = 1%.
> $$
> 100 \begin{cases}104\\
>  41.6\end{cases}
> $$
> First, we calculate the **risk neutral** **POD**.
> $$
> 100 = \frac{104(1-POD)+41.6POD}{1.03}\\
> POD = 1.6026\%
> $$
> **The bond must be discounted by the risk-free rate.**
>
> While the actual POD = 1%.
>
> So the implied price given the actual POD is 
> $$
> 100.365 = \frac{104\times0.99+41.6 \times 0.01}{1.03}
> $$
> Therefore, the bond is under priced.

#### Credit Valuation Adjustment

> Example
>
> 5 year zero coupon corporate bond. Risk-free rate = 3%. POD = 1.25%, Recovery Rate = 0.4
>
> At year 1:
> $$
> Exposure = 0 + \frac{100}{(1+r_f)^4}= 88.8487\\
> LGD = Exposure \times (1-RR) = 88.8487 \times 0.4 = 53.3092\\
> Expected \ Loss = LGD \times POD = 53.3092 \times 1.25\% = 0.6664\\
> PV(Expected \ Loss) = \frac{Expected \ Loss}{1+r_f} = 0.6470
> $$
> At year 2, 
>
> Same thing repeating ... 
>
> The fair value of the bond is 
> $$
> Fair \ Value = \frac{100}{1.03^5} - CVA 
> $$
> Where 
> $$
> CVA = \sum_i^t PV(Expected \ Loss)_i
> $$
> Then we calculate the credit spread
>
> Given (N = 5, PMT = 0, FV = 100, PV = -83.1060), we have YTM = 3.7704%, and then the credit spread = 3.7704-3 = 0.7704%
>
> **The annual rates of return or IRR is depend on when and if any default occurs.**
>
> At year 1, if default, the IRR would be 
> $$
> 83.1060 = \frac{35.5395}{1+IRR} 
> $$
> At year 2, the IRR would be
> $$
> 83.1060 = \frac{36.6057}{(1+IRR)^2} 
> $$
> in general, IRR at year n is 
> $$
> Fair \ Value = \frac{Recovered \ Amount _n}{(1+IRR)^n}
> $$

### Models

#### Transition Matrix Model

* **Credit Scores**: Used in retail lending market for individuals and small owner operated business. Ranks a borrer credit riskness but **does not provide a POD**.
* **Credit Ratings**: Wholesale lending market. **Ranks credit risk of a company, government or ABS**. Rating Agencies: Moody, Standard & Poor's, Fitch Ratings
* Investment Grade (**IG**), non-investment grade (**HY**) for high yield.
* Transition Matrix (used for credit migration)

![](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/Screen Shot 2020-01-29 at 5.27.12 PM.png)

Transition Matrix is used to estimate a 1-year rate of return given potential migration but no default.

For example, the probability of a bond from AA to A is 1.5%.

> Example
>
> Assume an A-rated 10-year corporate bond has a modified duration at horizon end of 7. 2  .
> $$
> \Delta Price  = -ModDur \times \Delta r
> $$
> Given the transition matrix. 
>
> Migrate from A $\rarr$ AA: 
> $$
> \Delta Price = -7.2(0.009-0.011) = 1.44\%
> $$
> Migrate from A $\rarr $ BBB: 
> $$
> \cdots
> $$
> Eventually, we have the expected return as 
> $$
> E(r) = YTM - (1.5\%(A\rarr AA)+  2.5\%(A\rarr BBB)+\cdots)
> $$

#### Structural Models 

A company  defaults on its debt if the value of its assets falls below the amount of its liabilities, and the probability of that event happens has the features of an option. 

Because
$$
A_t = D_t +E_t\\
E_t = max(A_t - K,0)\\
D_t = A_t - max(A_t - K, 0)
$$
Where K is the default barrier.

#### Reduced Form Model

*Default is an exogeneous variable that occurs randomly. This model seeks to explain when default occurs, not why.*

Default time modeled using a poisson stochastic process. 

Inputs are observable. Default model is estimated using regression analysis on company.

### Interpretations

#### Macroeconomic Factors (benchmark yield)

* Expected inflation rate
* Expected real rate of return
* Risk Aversion: Conpensation for uncertainty regarding expected inflation
* Affect All debt sceurities

#### Microeconomic Factors (Spread over benchmark yield)

* Expected loss from default
* Liquidity
* Taxation
* Risk Aversion: Compensation for uncertainty regarding expected loss from default.
* Specific to the issuer.

## Credit Default Swap

Credit default swap is a credit derivative whose underlying is the borrower;s credit quality. 

The sellers of CDS are betting on improving of credit quality. 

The buyers of CDS are deteriorating of credit quality. 

**CDS provides protection against default, but also protects against changes in credit quality long before a default.**

 >Hedge the credit risk
 >
 >If a bond's credit downgraded, 
 >
 >Long a bond, the bond loses value. 
 >
 >Long a CDS, CDS gains value.

Protection Buyer $\rarr$ Periodic Payments $\rarr$ Protection Seller

​                               $\larr$ Payment if default $\larr$ 

Payoff of a CDS is determined by the cheapest-to-deliever (**CTD**) obligation. 

The contract will specifies a reference obligation. 

> Example
>
> Assume that a company with several debt issues trading in the market files for bankruptcy. What is the CTD obligation for a senior CDS contract?
>
> A. A subordinated unsecured bond trading at 20% of par. 
>
> B. A 5 year senior unsecured bond trading at 50% of par.
>
> C. A 2 year seniro unsecured bond trading at 45% of par.
>
> Because it is a senior CDS, so it can't be A. (Subordinated)
>
> We are looking at the cheapest to deliever option, so 45% of par is cheaper then 50% of par. Therefore C.

#### Terminologies

* Index CDS: A combination of borrowers.It inroduces Credit corelation. (Defaults by certain companies may be connected to defaults by other companies) The more correlated the defaults the more costly it is to purchase protection. 
* CDS contracts specifies a **notional amount.** Total amount of CDS notional can exceed the amount of debt outstanding.  CDS buyer **does not need to be a debtholder**.
* CDS has an expiration date. 
* Buyer pays a periodic premium (Credit Spread) to seller. 
* CDS rates are now standarized . 
* To correct for the standarized rate being high or too low, an upfront payment/premium is required. Seller could have to pay the upfront payment as well if the spread should be lower.
* Value of CDS to buyers increases if reference entity's credit quality drops. Increase to seller if reference entity's credit quality improves.

#### Credit Events

* **Bankruptcy**. The filing of the bankruptcy is the credit event. Even the bankruptcy may not lead to liquidation. 

* **Failure to pay** . Scheduled interest or principal on any outstanding obligation. 

* **Restructuring**. Change in seniority, change in currency of payment, reduction of principal coupon. (Must be involuntary, it's forced on borrower). **Restructuring is not considered as a credit event in the US.**

* **Succession Event** a change in the corporate structure of the reference entity (merge, spinoff, etc) in which for the det in question becomes unclear. 

* **Settlement Protocols**. Once an event is decleared, both parties have the right but not an obligation to settle. 

* **Settlement**:

	* Physical Settlement: Holder sells bond CDS seller at par

	* Cash Settlement: Seller pays holder for losses.

		Payout Ratio = 1 - Recovery Rate

		Payment Amount = Payout Ratio $\times $ Notional

>Example
>
>A company is filing for bankruptcy. 
>
>Two senior bonds: A trades at 30% of par B Trades at 40% of par. 
>
>Investor X owns 10M of bond A and 10 M of CDS protection. 
>
>Investor Y owns 10M of bond B and 10M of CDS protection. 
>
>Recovery rate is the cheapest to deliever option. 
>
>Answer:
>
>Recovery Rate is same as Bond A because 30% < 40%. So CTD recovery rate for both bond = 30%.
>
>Investor X receives 7M, sells or holds the bond for 3M.  (no preference to settlement.) 
>
>Investor Y receives 7M, sells or holds the bond for 4M. (prefers cash settement because the company is only going to recover 30%. (CTD))

#### CDS Index Products

Typically used to protect against/take positions on the credit risk of sectors (bond portfolios that are similar to the index)

> Example
>
> Sell 500M of protection on CDX IG
>
> Buy 3M of protection on component A. (single CDS)
>
> Investor longs 1/125 *500  = 4M on A's credit while short 3M on A's credit. Hedged 75% exposure to A.
>
> Net exposure = long 1M
>
> Remaining notional on CDX IG = 496M
>
> 1/124 = 4M for each CDS remained 

$$
\text{Upfront Premium} = (\text{Credit Spread} - \text{Fixed Coupon})\times \text{Duration}
$$

--------------------------------------------

# Portfolio Management

## Exchange-Traded Funds

Mutual funds sells units  creates and redeems all units at closing NAV.

ETF shares trade intraday on an exchange. 

### Primary Market (OTC)

Authorized participants will  buy the types of shares the ETF holds, and trasfer these securities (**Creation Basket**) to ETF sponsor,  while the ETF sponsors will transfer ETF shares (**Creation Unit**). These activities are done and **delievered after the market close.** 

#### Bid-Ask Spread

The dealer (authorized participants) bid-ask spread on the ETF is determined by the **cost of arbitrage, risk premium for volatility and liquidity risk.** 

*Different from mutual funds, non-transacting ETF holders are shielded from negative impact of these transaction costs.* 

ETFs operates at lower costs, greater tax efficiency and the prices are kept in-line with NAV. 

### Secondary Market

Investor to investor on an exchange, settlement  is the same as other listed stocks. 

### Expense Ratios

Compared to MFs, ETF is 

* Much lower than MFs
* No Shareholder recordkeepping
* No communication costs
* No Active research

Broad-based, cap-weighted indexes. 

### Tracking Error

ETF managers attempt to track an index (evaluate by daily return difference, standard deviation of difference series referred as **tracking error**) as closely as possible. 

An index fund would usually underperform its benchmark on an annual basis by the amount of expense ratio. 

Sources of tracking error are

* Fees and expenses
* Reprentative sampling and optimization-full replication may not be optimal and possible for large indexes. 
* Can Enhance or detract from ETF returns depending on whethere holdings over/under-perform those in the index. 
* Depository Recipts and ETFs ETFs may hold shares that are different than those in the index. 
* Index changes: ETFs may add/eliminate consitutes at different times/prices than the index. 
* Fund accounting practice: valuation times each day may differ from the index. 
* Regulartory and tax requirements. e.g: Foreign dividend withholding tax.
* Asset manager operations. Securities lending, foreign dividend recapture. 
* Tax Issue:
	* Capital gains distribution
	* Funds must distribute any capital gains realized during the year. 

### ETF Trading Cost

ETF acquire/redeem anytime exchange is open. Closing price may include a premium or discount compared to the closing NAV. 

Commissions + trading cost reflect in the bid-ask spread and market impact. Most of bid-ask spread comes from market structure and liquidity of underlying. The higher market maker competition also contribute less bid-ask spread. 

Bond may use modeling price instead of closing price because closing price is not avaliable.  

### Cost Comparison

| Fund Cost Factor                  | Function Of Holding Period | Explicit/Implicit | ETFs                                          | MF               |
| --------------------------------- | -------------------------- | ----------------- | --------------------------------------------- | ---------------- |
| Management Fee                    | Y                          | E                 | Often Less                                    | Yes              |
| Tracking Error                    | Y                          | I                 | Often Less than comparable index mutual funds | Index Funds Only |
| Commissions                       | N                          | E                 | Some free                                     |                  |
| Bid-Ask Spread                    | N                          | I                 | Yes                                           |                  |
| Premium/Discount TO NAV           | N                          | I                 | Yes                                           |                  |
| Portfolio Turnover                | Y                          | I                 | Often Less                                    | Yes              |
| Taxable Gains/Losses to Investors | Y                          | E                 | Often Less                                    | Yes              |
| Security Lending                  | Y                          | I                 | Often More                                    | Yes              |

### Risks

* Counterparty Risk: Some ETF structures involve reliance on a counterparty. Example: ETNs. 
	* Settlement Risk: when an ETF uses OTC derivatives. 
	* Securities lending: Cash collateral minimizes this risk.
* Fund Closure: Can trigger capital gains and a need to find replacement investment. Due to
	* Regulation
	* Competition
	* Corporate Actions (M&A)
	* Creation Halts (Mostly ETNs)
	* Change in Investment Strategy
* Investor-related risk.
	* Lack of understanding of underlying arbitrage breaks down.

### ETFs in Portfolio Management

| Portfolio Application                                        | Role in Portfolio                                            | Examples of ETFs by Benchmark Type                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Cash Equitization                                            | Minimize cash drag by staying fully invested to benchmark exposure, transact small cash flows. | Liquid ETFs benchmarked to asset category                    |
| Portfolio Rebalancing                                        | Maintain Exposure to target weights                          | Domestic Equity, international equity, domestic fixed income |
| Portfolio Completion                                         | Fill Gaps in Strategic Exposure (Countries, Sectors, Industries, themes, factors) | International Small cap, Canada, bank loans, real assets, health care, ESG, etc |
| Manager Transition Activity                                  | Maintain Interim benchmark exposure during manager transitions | ETFs benchmarked to new manager's target benchmark.          |
| Core asset class or market                                   | Strategic or tactical role. Strategic weighting and tactical tilt to enhance returns or modify risks. | Domestic Equity, international equity, domestic fixed income |
| Equity Style, Country, or Sector, fixed income or commodity segement | Strategic or tactical. Tactical tilet to enhance returns or modify risk depending on short-term views hedge index exposure of active stocks or bond strategy. | Value, growth, Canadian Equities, Corporate or HY debt       |
| Equity Sector, Investment theme                              | Dynamic or tactical . Efficient implementation of a thematic industry vs Single-stock view. Capture performance on an emerging theme or innovation not reflected in industry categories. | Technology financials, oil and gas, biotech, infrastructure, rebotics. |
| Factor Exposure                                              | Capture risk premium for one or more factors driving returns on risk overweight or underweight depening on factor return or risk outlook. Seek to capture alpha from rules based screening and rebalancing. | Quality, dividend growth, value, momentum, multi-factor.     |
| Risk Management                                              | Adjust equity beta, duration, credit or currency risk.       | Currency-Hedged, low-volatility, or downside-risk manageed ETFs. |
| Leveraged And inverse Exposure                               | Access or short exposure for short-term tilts or risk management limit losses. | ETFs representing asset classes, countires or industries with leveraged or inverse daily return targets. |
| Alternative Weighting                                        | Seek Outperformance from weighting based on one or more fundamental factors. . Balance or manage risk of security holdings. | ETFs weighted by fundamentals, dividends, or risk, equal-weighted ETFs. |
| Active strategies within an asset class                      | Access discretionary active management in an ETF structure.  | ETFs from reputable fixed income or equity managers          |
| Dynamic Asset allocation and multi-asset strategies          | Seek returns from active allocation across asset classes or factors based on return or risk outlook. Invest in a multi-asset-class strategy in single product | ETFs that allocate across asset categories or investment themes based on quantitative or fundamental factors. |

## Using Multifactor Models

### Arbitrage Pricing Theory

#### CAPM: A single factor model

$$
E(R_p) = R_f + \beta(Rm-R_f)
$$

Where $\beta$ is the sensitivity of the portfolio to the market risk factor.

$R_m - R_f $ is the equity risk premium.

#### Multifactor Model

Therefore, for a multifactor model, we could have multiple risk factors.  
$$
E(R_P) = R_f + \beta_1 F_1 +\beta_2F_2 + \cdots +\beta_k F_k
$$

#####   Assumptions 

* A factor model describes asset returns.
* There are many assets so investors can form well-diversified portfolios that eliminate asset specific risk.
* No arbitrage opportunities exist among well-diversified portfolios. 

If these three assumption holds, if two models has same sensitivities to the same factors, their return should be the same. 

> **$E(R_p)$ is linearly related to the factor sensitivities of that portfolio.** 

### Common Multi-factor model

#### Carhart 4-factor model

$$
R_p - R_f = a_p+b_{p_1}RMRF+b_{p_2}SMB+b_{p_3}HML+b_{p_4}WML+\epsilon_p
$$

* RMRF is the return on a value weighted index minus one month  T-bill rate
* SMB: Small minus big (Market Cap factor). Average return on 3 small cap portfolios minus average return on 3 large cap portfolios. 
* HML: High minus low: Average return on 2 low BV/MV portfolios. 
* WML: Winners minus Losers. (Momentum Factor) Return on a portfolio of last year's winners minus return on a portfolio of last year's losers. 

### Types of Factors

#### Macroeconomic

Factors are **surprises** in macro variables that significantly explains returns. Such as interest rates, inflation risk, business cycle risk, etc. 

Assumes return are correlated with only the surprises in some aggregate economy factors. 

Predicted values should already be reflected in prices. Therefore in their expected return. 
$$
R_i = a_i+b_{i1}F_1+b_{i2}F_2+\cdots + b_{ik}F_k+\epsilon_i
$$
Where $a_i$ reflects the effect of predicted values. 

So 
$$
R_i = \text{Predicted Value}+\text{Surprises}+\text{Asset-specific risk}
$$

##### Example

$$
R_i = a_i +b_{i1}INFL+b_{i2}GDP+\epsilon_i
$$

inflation risk premium typically negative. If $b_{infl}$ is positve, it will has a leverage effect on inflation risk, $b_{infl}$ is negative, it will has a hedging ability. 

#### Fundamental Factors

$$
R_i = a_i +b_{i1}F_1 +b_{i2}F_2+\ldots +b_{ik}F_k+\epsilon_i
$$

In the fundamental models, $a_i$ is not expected return. Factors are the properties of the asset. 

##### Standarize betas

$$
b_{ik}= \frac{\text{Value of attribute k for assset i}-\text{Average value of attribute K}}{\sigma_{\text{Value of attribute k}}}
$$

####  Statistical Factors

Statistical methods applied to historical returns of a group of securities to extract factors. Factor analysis and principal components analysis. 

Basically instead of named factors attempting to explain return, we have explanations of return looking for a name.

### Applications of multifactor models

#### Return attribution

Typically fundamental models used. 

Benchmark $R_B = R_F + \beta_B ERP+\epsilon$

Active Portfolio $R_p = R_F +\beta_P ERP +\epsilon$

where ERP is the equity risk premium. 

Then we have $(R_B-R_p) = (\beta_B-\beta_P)ERP + \epsilon$

##### Example

Given $R_p-R_B = 2.0741\%$ 

![image-20200206183223251](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200206183223251.png)

The **Absolute return contribute by the factor**  = Difference between factor sensitivity in the portfolio and factor sensitivity in the benchmark $\times $ Factor return.

**Return from factor tilts** = $\sum$ All absolute return contribute by the factor.

**Active return** is the performance over benchmark.  $R_p-R_B = 2.0741\%$ 

The return from **security selection** = Active return $-$ Benchmark return.

### Risk Attribution

**Active risk** = $\sigma$(Active Returns). Also known as **Tracking Error**.

>As an approximation assuming returns are serially uncorrelated, to annualize a daily TE based on daily returns, we multiply daily TE by (250) 1/2 based on 250 trading days in a year; to annualize a monthly TE based on monthly returns, we multiply monthly TE by (12) 1/2 .

**Information Ratio** is
$$
IR = \frac{\bar R_p-\bar R_B}{\sigma_{(R_p-R_B)}}
$$
IR stands for every unit of risk above the benchmark level of risk returned IR.

#### Decomposition Of Active Risk

Active risk is make up by the **active factor risk** and **security selection ** risk. 

**Use variances instead of s.d because variances of uncorrelated variables are additive.** 
$$
\text{Tracking Error}^2 = \sigma^2_{(R_p-R_B)}
$$
**Active Factor risk is the difference froom benchmark exposures.** 

**Security Selection Risk** is also the residual risk, it is
$$
=\sum_{i=1}^{n} (w_i^a)^2\sigma_{w_i}^2
$$
$w_i^a$ is the active asset weight in the portfolio. Calculated as $w_p-w_B$ 

### Portfolio Construction

For passive managed portfolio, may need to select a sample of securities from the index. 

For active managed portfolio, it can be used to establish desired risk profiles/exposures.

Rules-based active management introduces intentional factor and style bias. (Instead of picking securities, you could picking factors (style)).

It can be used to help investor to ensure that active risk/return outcomes are commensurate with active fees.

## Measuring and Managing Market Risk

### Value at Risk (VaR)

The **minimum loss** that would be expected, **a certain percentage at the time** over **a certain time period**. Given the assumed market conditions. 

Expressed in either currency units or in percentage terms. The 5% VaR of a portfolio is 2.2M over a one-day period. 

>* €2.2 million is the minimum loss we would expect 5% of the time; or
>* 5% of the time, losses would be at least €2.2 million; or
>* we would expect a loss of no more than €2.2 million 95% of the time.

#### Example

> The 5% VaR of a portfolio is 2.2M over a one-day period. 
>
> Which means a loss of at least 2.2M is expected to occur once every 20 days. (5% of the time)

![image-20200207104953816](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200207104953816.png)

1% VaR implies a downward move of 2.33 $ \sigma$

5% VaR implies a downward move of 1.65 $ \sigma$

#### Estimating VaR

First, convert the set of holdings in the portfolio into a set of exposures to risk factors. (Risk Decomposition)

Second, gather a data history for each of the risk factors in the VaR model. 

Then estimate VaR. 

* Parametric method.
* Historical Simulation method.
* Monte Carlo Simulation method. 

> Example
>
> 2 Asset portfolio, PV = 150M, (SPY ETF: $w_s = 80\% $ Corporate Bond ETF: LWC  $w_L = 20\% $ )
>
> |      | Annualized Return | Daily Sigma |
> | ---- | ----------------- | ----------- |
> | SPY  | 10.5%             | 20%         |
> | LWC  | 6%                | 8.5         |

##### Parametric Method

First, we would need to calculate the expected return of the portfolio and the standard deviation of the portfolio's return. 
$$
E(R_p) = w_sE(R_S)+w_L(R_L)=0.8(0.105)+0.2(0.06) = 0.096\\
\sigma_p = \sqrt{w_s^2\sigma_s^2+w_l^2\sigma_l^2+2w_sw_l\rho_{SL}\sigma_s\sigma_l}=0.157483
$$
Given that our inputs are based on annual returns, but we want to measure VaR on a daily basis, we need to convert them by
$$
E(R_p) = \frac{0.096}{250} = 0.000384\\
\sigma_p = \frac{0.157483}{\sqrt{250}} = 0.009960
$$
Then we can caluclate the 5% VaR.
$$
5\% VaR = -(E(R_P)-1.65\sigma_p)PV = 2407500
$$
Parametric method **generallly assumes distribution of returns on risk factors is normal. **

##### Historical Simulation Method

Calculate the daily portfolio return $R_p = 0.8SPY+0.2LWC$ in the lookback period for the past two years. Rank them, and use the percentile.  5% VaR is the 5% percentile of the return. 

##### Monte Carlo Simulation Method

Not Constrained by any distribution. Avoids the complexity of the parametric method when the portfolio has many risk factors. 

Run the monte carlo simulation for each asset, ranked the output return and take its percentile. 

#### Advantages & Limitations Regarding VaR

##### Advantages

* Simple & Easily comunicated Concept
* Provides a basis for risk comparison 
* Facilitates capital allocation decision
* Can be used for performance calculation
* Reliability can be verified
* Widely accepted by regulators

##### Limitations

* Subjectivity: VaR cutoff, time period, estimation method
* Understanding the frequency of extreme events
* Failure to take into account liquidity
* Sensitivity to correlation risk: in times of market stress, correlations among all assets tend to rise
* Vulnerability to trending or volatility regimes: A portfolio may remain under its VaR limit every day, but just under it. 
* Misunderstanding the meaning of VaR
* Oversimplification
* Disregard of right-tail events. (Ignore the greater return opportunity)

#### Extension of VaR

##### Conditional VaR:  CVaR

$$
CVaR = [\text{Avg Loss|VaR >Cufoff}]
$$

Avg Loss referred as the amount of loss I can expect if VaR is exceeded. 

> It is the average loss conditional on exceeding the VaR cutoff. So, although VaR answers the question of “what is the minimum loss I can expect at a certain confidence,” CVaR answers the question of “how much can I expect to lose if VaR is exceeded.” CVaR is also sometimes referred to as the expected tail loss or expected shortfall.

Typically obtained using historical simulation.

##### Incremental VaR: IVaR

Incremental value at risk. How VaR will change if a position size is changed relative to the remaining positions. 

##### Marginal VaR: MVaR

Conceptually same as IVaR but reflects the effect of a very small change in the position. 

##### Relative VaR: Ex-ante tracking error

A measure of the degree to which the performance of a given investment portfolio might deviate from its benchmark.

It is computed using any of the stan-dard VaR models, described earlier, but the portfolio to which VaR is applied contains the portfolio’s holdings minus the holdings in the specified benchmark.

### Sensitivity and Scenario Measures

#### Sensitivity Measures

Sensitivity Risk Measures examines how performance responds to a single change in an underlying risk factor.

* Equity exposure measures: $\beta$ 
* Fixed Income exposure measures: duration & convexity
* Option exposure measures: $\Delta, \Gamma,\kappa$

#### Scenario Measures

* Historical Scenarios: Repriced portfolio holdings in chosen extreme market dislocations. Use models as proxies for equities or bonds that are not exists. **Stress Test**
* Hypothetical Scenarios: Imagined but not yet been experienced. Identify portfolios most significant exposures. **Reverse stress test.**
* For stress test, we first looking for an event in the history, identify the factor risks, then we consider its effect on portfolio. For reverse stress test, first looking for our factor risk, then we have an imagined event.

### Applications of Risk Measures

* Liquidity gap: Extend of any liquidity and asset/liability mismatch. 
* VaR: For the held and sale/trading portion.
* Leverage: Weight assets by risk, riskier assets assigned greater weight, then divide by equity. 
* Sensitivities: Hled for sale. 
* Economic Capital: applied to full balance sheet, blends market, credit, and operational risks. 
* Scenario analysis: stress applied to whole balance sheet  to assess capital sufficiency. 
* Asset Management: Focused on volatility, probability of loss or underperforming a benchmark. 

## Economics & Investment Markets

### Real Risk-Free Rate

Production $\larr$Investment = Savings $\rarr$ Consumption

Savings are deferred consumption, which requires compensation. Compensention can then decomposed into $l, \theta, \rho$. 

$l_{t,s}$ stands for the real risk-free rate today t for one unit of currency in future s. 

$\theta_{t,s}$  is expected inflation.

$\rho$  is the risk preium associated with $\tilde{CF}$

$\tilde{CF}$ is uncertain cash flows in the future. 

$E[\tilde{CF}]$ is the expectation of CF conditional on information avaliable today.

All financial instruments essentially represent claims on an underlying economy. 
$$
P_t^i = \sum_{s=1}^{N}\frac{E_t(\tilde{CF}_{t+s})}{(1+l_{t,s}+\theta_{t,s}+\rho_{t,s})^s}
$$
**All financial Instruments essentially represent claims on an underlying economy.**

$P_t^i$ is the value of asset i today (t). It depends on future expected cash flows conditioned on current information. Reflects all expected/anticipated information.

Economy affects both the cash flow and compensations. 

$(1+l_{t,s}+\theta_{t,s}+\rho_{t,s})$ values vary over time as expectations regarding economic growth, inflation, and cash flow risk change.

>Defination of real risk-free rate
>
>Define $u_t$ as the utility of cosuming today and $u_{t+s}$ is defined as the utility of consuming in the future. 
>
>Then we have
>$$
>\tilde{m}_{t,s}  = \frac{u_{t+s}}{u_t} 
>$$
>where $\tilde{m}_{t,s}$  as the **intertemporal rate of substitution**. Given that the utility of spending now is always greater then spending in the future. 
>
>Deflation is the only motivation of deferring consumption.
>
>If the expectation of the future condition is good, then $u_{t+s} \darr, \tilde{m}_{t,s} \darr$ .   
>
>The interest rate is 
>$$
>I = \frac{1}{\tilde{m}_{t,s}}-1
>$$
>**Therefore, if the expectation of the future economic condition is good, then the interest rate will be high. Vice versa.**

 

|                             | Low Income | High Income |
| --------------------------- | ---------- | ----------- |
| Absolute Risk Aversion      | High       | Low         |
| Investments In Risky Assets | Low        | High        |
| Premium for a given risk    | High       | Low         |

$$
P_t^i = \frac{E[P_{t+1}^i]}{1+I{t,s}}-\text{risk premium}
$$

Risk free rate increases as time-to-maturity increases. Because the uncertainty regarding the expected marginal utility rises. **The yield curve should be upward sloping.**

* Expectations of future affect savings
* Savings affect prices of financial assets: Good times ahead, higher current consumptions, leads to higher return. Requied to induce saving: lower price for risk-free assets, higher prices for risky asset. Sell bonds, buy stock. 

### Business Cycle

#### Inflation

$I_{t,s}+\theta_{t,s}+\pi_{t,s}$ is the nominal interest rate

$\pi_{t,s}$ is the uncertainty in expected inflation

>Over very short periods of time, $\pi_{t,s} = 0$ 

#### T-bill rates & the business cycle

T-bills are often used to implement monetary policy (Open market operations)

Cut policy rates when business activty or inflation judged to be too low. 

Raising rates when the opposite is the case.

Using Taylor expansion: we have
$$
\text{Policy Rate} = I+\theta+0.5(\theta-\theta^*)+0.5(y-y^*)
$$
Where *I* is the real rate, $\theta$ is the inflation, the $\theta-\theta^*$ is the inflation gap, and $y-y^*$ output gap. 

#### Longer-term bonds & the business cycle

The greater the uncertainty about the real value of the payoff,( lower confidence to form views about the future inflation ) will cause investors to demand a premium.  ($\pi$ )

**Breakeven Inflation rate (BEI)** = yield on a zero nominal bond $-$ on a zero real default free bond.

Evolution of I over time driven mainly by $\tilde{m}_{t,s}$ . Evolution of r over time will also be driven by

* Changing expectations about inflation
* Changing perceptions about the uncertainty of the future inflation environment.

#### Default-Free yield curve & the business cycle

In the short-end $\Rarr$ Policy Impact

Full curve $\Rarr$ Expected impact of growth and levels of expected future inflation.

#### Credit Risk

Introduce credit premium.
$$
P_t^i = \sum_{s=1}^{N}\frac{E_t(\tilde{CF}_{t+s})}{(1+l_{t,s}+\theta_{t,s}+\rho_{t,s}+\gamma_{t,s}^i)^s}
$$
where $\gamma_{t,s}$ is the credit spread. 

Tends to widen in times of economic weakness.

Spreads of lower-rated bonds more volatile versus IG.

Some sectors are more sensitive to the business cycle than others. (clclical vs non-cyclical.)

#### Equities

$$
P_t^i = \sum_{s=1}^{N}\frac{E_t(\tilde{CF}_{t+s})}{(1+l_{t,s}+\theta_{t,s}+\rho_{t,s}+\gamma_{t,s}^i+\kappa_{t,s}^i)^s}
$$

Where we have

$\gamma_{t,s}^i+\kappa_{t,s}^i = \lambda_{t,s}^i$ as the equity risk premium.

In the bad economy times, it has low or no payoff in bad times. 

#### Earnings Growth & the business cycle

Declines associated with sharp declines in real earnings. Sharp increase in profit growth occur at the end of a period of recession. 

#### Commercial Real Estate & the business cycle

$$
P_t^i = \sum_{s=1}^{N}\frac{E_t(\tilde{CF}_{t+s})}{(1+l_{t,s}+\theta_{t,s}+\rho_{t,s}+\gamma_{t,s}^i+\kappa_{t,s}^i+\phi_{t,s}^i)^s}
$$

Where $\phi$ is the illiquidity. 

## Analysis of Active Portfolio Management

The objective of active management is to add value by doing better than a benchmark portfolio. 

### Choice of Benchmark

1. Representative of the assets from which the investor will select
2. Positions in the benchmark can actually be replicated at low cost
3. Benchmark weights are verifiable ex ante (we can look at the benchmark weights before we replicated), and return data are timely ex post (Should be able to see the weights after the market close). 

### Return Metrices

* Active Return

$$
R_A =\sum_{i=1}^{N}w_{P_i}R_i-\sum_{i=1}^{N}w_{B_i}R_i\\
=\sum_{i=1}^{N}(w_{P_i}-w_{B_i})R_i
$$

* Alpha (risk adjusted active return)

$$
\alpha_P = R_P -\beta R_B
$$

* Another form of active return

$$
Given\\
\sum{w_P} =  \sum{w_B} = 1\\
So\\
\text{active weights} = \sum_{i=1}^N (w_{P_i}-w_{B_i}) = 0\\
R_A =\sum_{i=1}^{N}(w_{P_i}-w_{B_i})R_i\\
=\sum_{i=1}^{N}\Delta w_iR_i-0\\
=\sum_{i=1}^{N}\Delta w_iR_i-\sum_{i=1}^{N}\Delta w_iR_B\\
=\sum_{i=1}^{N}\Delta w_iR_{A_i}\\
\text{Which is the dot product of the active weights and active security returns}
$$

#### Decomposition of Value Added

Two sources of active value: Due to asset allocation and due to security selection.
$$
R_A = \sum_{i=1}^{N} \Delta w_i R_{B_i}+\sum_{i=1}^N w_{P_i}R_{A_i}\\
=\text{Asset Allocation}+\text{Security Selection}
$$

### Risk-Adjusted Ratios

#### Sharpe Ratio

$$
Sharpe_P = \frac{R_P-R_F}{\sigma_{R_P}}
$$

**The sharpe ratio is unaffected by the addition of cash or leverage.**

$w_P$ weight on actively managed portfolio, while $1-w_P$ is the weight on cash.
$$
R_c = w_PR_P+(1-w_P)R_F\\
SR_C = \frac{R_C-R_F}{\sigma_{R_c}}\\
=\frac{w_PR_P+(1-w_P)R_F-R_F}{w_P\sigma_{R_P}}\\
=\frac{R_P-R_F}{\sigma_{R_P}}\\=SR_P
$$

####  Information Ratio

$$
IR = \frac{R_P-R_B}{\sigma_{(R_P-R_B)}}\\
=\frac{\text{Active Return}}{\text{Active Risk}}
$$

For a benchmark replicated ETF, the IR = 0.

For an all active fund ($\beta= 0$) , it will have sharpe ratio same as IR ratio.

**IR is not affected by the aggressiveness of active weights.**

![CAL](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/CAL.png)

The sharpe ratio is the slope of the Capital Allocation line. 

**Adjusting active risk may involve investing in both the actively managed portfolio the benchmark, portfolio, but morelikely modifying active weights.**

![image-20200209143445899](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200209143445899.png)

>The property of active management theory
>
>$SR_P^2 = SR_B^2+IR^2$
>
>**This is what is used to achieve optimal information ratio.**
>
>Implies that the active portfolio with the highest IR will also have the highest SR.

By combining optimal portfolio with cetain amount of cash, we could achieve a portfolio which has a higher sharpe ratio compared to the benchmark, but it will lower the information ratio.
$$
\sigma_{R_A} = \frac{IR}{SR_B}\sigma_{R_B}
$$
**Investor is concerned about maximizing the managed portfolio's active return, subject to a limit on active risk.(Benchmark Tracking Risk)** 

### The Fundamental Law

Let $u_i $ as the investors' subjective expectation of the active return on asset i.  

![image-20200209163022669](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200209163022669.png)

* $u_i$ is the forcasted active returns.
* $R_{A_i}$ is the realized active returns.
* The correlation between $u_i$ and $R_{A_i}$ is called **information Coefficient (IC).** The higher the IC, the better the manager. IC is a measure of signal quality. 
* **Transfer coefficient (TC)** reflects how manangers forcasted returns are transferred into active weights.

The **mean-variance optimal active security weights** $\Delta w_i^*$ for uncorrelated active returns, subject to a limit on active risk. 
$$
\Delta w_i^* = \frac{\mu_i}{\sigma_i^2}\cdot \frac{\sigma_A}{\sqrt{\sum_{i=1}^{N}\frac{\mu_i^2}{\sigma_i^2}}}\\
\text{Where}\\
\mu_i = IC \sigma_iS_i\\
S_i \text{is the standarized forecasts of} \ E(R_i)\\
\sigma_A \text{is that limit of active risk}
$$
 After simplifying, we have
$$
\Delta w_i^* = \frac{\mu_i}{\sigma_i^2}\cdot \frac{\sigma_A}{IC\sqrt{BR}}
$$
*BR,* stands for breath. Under certain conditions, $BR = N$, but more accurately, it is the independent decisions made in a year to construct the portfolio. 

> The sum of active weights should equal to 0.
>
> $\sum_{i=1}^N \Delta w_i^* = 0$

The basic fundamental law:

>The optimal expected active return is 
>
>$E(R_A)^* = IC\sqrt{BR}\sigma_A$
>
>Then we have the optimal information ratio
>
>$IR^* = \frac{IC\sqrt{BR}\sigma_A}{\sigma_A} = IC\sqrt{BR}$
>
>Therefore,
>
>$E(R_A^*) = IR^* \sigma_A$

The transfer coefficient TC is calculated as 
$$
TC = corr(\frac{\mu_i}{\sigma_i},\Delta w_i \sigma_i)\\
\text{OR}\\
TC = corr(\Delta w_i^* \sigma_i,\Delta w_i \sigma_i)
$$
Note that $\Delta w_i^* $ is the optimal active weight.

Then we have 

> The optimal expected actvie return is
>
> $E(R_A) = TC \cdot IC \sqrt{BR} \sigma_A$
>
> With all the formulas above, we then would also have 
>
> $IR = TC \cdot IC \cdot \sqrt{BR}$
>
> Therefore we have
>
> $SR_P^2 = SR_B^2+TC^2({IR^*})^2$

We could adjust active risk and return by investing in both the actively managed and benchmark portfolios. 

> The Optimal amount of active risk
>
> $\sigma_{R_A} = TC \frac{IR^*}{SR_B}\sigma_{R_B}$
>
> For non-constraint portfolios, TC =1.
>
> Then we can also calculate the sharpe ratio of the portfolio as
>
> $SR_P^2 = SR_B^2+TC^2(IR^*)^2 $
>
> Therefore, the active portfolio with the highest IR will also ave the highest sharpe ratio. 
>
> **The IR is the single best criterion for accessing active performance among actively managed funds with the same benchmark.**

#### Ex-Post Performance

Because $E(R_A|IC_R) = (TC)(IC_R)\sqrt{BR}\sigma_A$ , where $IC_R$ stands for the realized IC. The realized active return came from expected return $E(R_A|IC_R)$ and noise. Which means skill plus constraints. 

#### Active Management Strategy

One can either managed their portfolio cross-sectional with N securities. where $BR = N$ or one can do market-timing on one security where $BR=T$ , or one can do it both: which means $BR = N\cdot T$   

#### Limitation of the fundamental law

Investors tend to overestimate their skill, forcasting ability differes among different asset segments over time.

Non-independence can result in very large BR however, for regular BR or time-series decision, it is very hard to have independent decisions. 

## Trading Costs & Electronic Markets

### Costs of Trading

* Fixed Costs: Traders, office, space, trading tools.
* Variable Costs: 
	* Explicit: Commissions, taxes exchange fees
	* Implicit: bid-ask spread, market impact, delay cost(slippage arises from the inability to complete a trade immediately) , opportunity costs

#### Spread

Bid price: A dealer is willing to buy

Ask price: A dealer is willing to sell

Spread = difference between bid and ask.

The smallest spread (**inside spread**) is calculated by the lowest ask price (**inside ask**) and the highest bid (**inside bid**).

To estimate transaction costs, trade price is compared to a benchmark price. 

> Example
>
> | Trade | Price | Size | Bid   | Ask   |
> | ----- | ----- | ---- | ----- | ----- |
> | 1     | 10.21 | 4k   | 10.19 | 10.21 |
> | 2     | 10.22 | 6k   | 10.20 | 10.22 |

If the benchmark price is the midquote at time of trade, we use **effective spread.** It is OK when single orders. Not very effective when a large order is split into many trades. 

The effective spread is calculated as 
$$
10.21-\frac{10.19-10.21}{2} = 0.01\\
10.22-\frac{10.20+10.22}{2} = 0.01
$$
But it will not take the market impact cost into consideration. Because our  trade 1 pushed the price to 10.22, we lost $0.01 \times 6k = 60$ for trade 2. 

If the benchmark price is the midquote at time of order submission, we use **implementation shortfall.**
$$
[\text{Desired Size}\times \text{Closing Price} - \text{Desired Size}\times \text{Decision Price}]-[\text{Actual Size}\times \text{Closing Price} - \text{Total Purchase Cost}]
$$
If the benchmark price is volume weighted average price, we use **VWAP**.
$$
VWAP = \frac{\sum_i\text{Volume}_i\times \text{Quote}_i}{\text{Total Volume}}
$$

### Electronic Markets

#### Advantages 

* Lower costs for both traders and exchanges
* Execute with perfect discipline
* Keep perfect records
* Support/enhance anonymity/privacy
* 24 hour capabilit
* No need for actual location
* Liquidation aggregation

#### Types of traders

* Eletronical news traders
* Electronic Dealers.
* Electronic Arbitragers
* Electronic Front Runners
* Electronic Quote Matchers

#### Characteristics

* Fast Communications
* Fast Computations

#### Uses

* Advanced order types (e.g: Dynamic limit orders)
* Trading tactics (Sweeping the market)
* Algorithms (reduce the effect  of large orders)

#### Risks and Solutions

* Entry costs may limit access to a few.
* Systematic risk ( Solved by testing of code)
* Pinging (Try to discover hidden orders)
* Leapfrog
* Flicerking 

# Economics

##  Currency Exchange Rate

### Bid-Ask Spread

**Bid is highest price buyer willing to pay.**

**Ask is the lowest price seller willing to offer.**

The quoting conventions is B.P (base.price) or $\frac{Price}{Base}$.

For example, USD.CAD = 1.3410.  In this case, the base currency is always one unit, price currency is how much foreign currency you can get with 1 base. In this case, it means 1 USD = 1.3410 CAD. In the other notation, it is CAD/USD = 1.3410.

**Long** means buy the base by paying the price.

**Short** means sell the base and receive the price.

Settlement on spot transactions is usually T+2. 

#### Interbank Market

  ![image-20200211111822506](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes/image-20200211111822506.png)

#### Spread

The spread depends on a few things:

* Currency pair involved
	* Major pair: EUR.USD (EUR/USD), USD.JPY, GBP.USD. Very liquid, very tight spreads.
	* Cross pair:  CHF.MXN, MXN.JPY, etc. Wdier spreads.
* Times of Day
	* 3 Big markets: Japanese (Tokyo) Opening, European (London) Opening, N.America (New York) Opening
* Volatility
	* Right in front of the major data release. 
* Dealer
	* Some will pass on the inter-bank bid/ask spreads but charge commission
	* Soe will spread the interbank bid/ask but charge no commission

### Arbitrage

A dealer's bid-ask quote must respect 2 arbitrage constraints:

* Dealer bid<Interbank Offer 
* Dealer Offer > Interbank bid

> Example
>
> |           | Bid    | Offer  |
> | --------- | ------ | ------ |
> | Interbank | 1.0522 | 1.0524 |
> | Dealer    | 1.0525 | 1.0524 |
>
> In this case, dealer bid > IB offer, therefore exists an arbitrage opportunity.
>
> One could buy from IB at 1.0524 and sell to Dealer at 1.0525.

#### Triangular arbitrage 

> Dealer Crossrate Bid < Implied Interbank Crossrate Offer

For example:

If we have USD/EUR and JPY/USD, we can imply JPY/EUR.

|             | Bid                  | Offer                |
| ----------- | -------------------- | -------------------- |
| USD/EUR     | 1.0522               | 1.0524               |
| JPY/USD     | 118.10               | 118.15               |
| **JPY/EUR** | 1.0522$\times$118.10 | 1.0524$\times$118.15 |

## Spot & Forward Rate

Forward exchange rates must satify an arbitrage relationship. 

Price/Base now becomes foreign/domestic.

For 1 unit of domestic, we can invest the domestic at domestic risk-free rate $i_d$ At the end of year we would have a payoff as $(1+i_d)$ . 

We can also convert the 1 unit domestic currency to foreign currency at the spot price $S_{f/d}$  and invest at a foreign risk-free rate $i_f$. At the end of the ear, we would have $S_{f/d}(1+i_f)$ amount of foreign currency. 

Then we converted this amount of foreign currency to domestic currency at the **spot rate then, thus the forward spot rate now** $F_{f/d}$ . We can then get 
$$
S_{f/d}(1+i_f)(\frac{1}{F_{f/d}})
$$
amount of domestic. It must be equal to the alternative way before.

So, we have
$$
S_{f/d}(1+i_f)(\frac{1}{F_{f/d}}) = 1+i_d
$$
Risk-free rates quoted using libor. Lets introduce the day-count convention.
$$
(1+i_d\frac{Actual}{360}) = S_{f/d}(1+i_f\frac{Actual}{360})(\frac{1}{F_{f/d}})
$$
Then we have the forward rate as 
$$
F_{f/d} = S_{f/d}(\frac{1+i_f[Actual/360]}{1+i_d[Actual/360]})
$$
This equation is called **covered interest rate parity.**

The other form of this equation is 
$$
F_{f/d}- S_{f/d}=S_{f/d}(\frac{Act/360}{1+i_d[Act/360]})(i_f-i_d)\\
Or
\\
F_{P/B}- S_{P/B}=S_{P/B}(\frac{Act/360}{1+i_B[Act/360]})(i_P-i_B)
$$
Because we can see that 
$$
S_{P/B}>0 \\
and\\
\frac{Act/360}{1+i_B[Act/360]}>0
$$
So $(i_P-i_B)$ soley determines whether it is a premium or discount forward rate.

### Quoting Covention

| Maturity    | Spot Rate Or Forward Points |
| ----------- | --------------------------- |
| Spot        | 1.3549  \| 1.3651           |
| One Month   | -5.6\|-5.1                  |
| Three Month | -15.9\|-15.3                |
| Six Month   | -37\|-36.3                  |
| One Year    | -94.3\|-91.8                |

Forward foreign exchange rate is quoted in term of points. So, the one month forward bid and ask price is calculated as $1.3549-0.00056 = 1.3493$

$1.3549\\ \ \ \ \ \  -5.6\\-----\\=1.3493$

The longer the term, the wider the bid-offer spread, because 

* Liquidity declines
* Counterparty credit risk increases
* Interest rate risk increases

Clients can select any time period (i.e non-standard aka **broken**). Rates will be interpolated based on standard settlement dates.

## Mark-To-Market Value

**Value of contract at initiation is zero.** Mark-to-Market value changes as the spot exchange rate changes or the interest rate changes. (Foreign or domestic)

> Example
>
> At time 0, we enter into a six-month forward.
>
> Bought 10M GBP at an exchange rate AUD/GBP = 1.6100 (will pay 16.1 AUD in 6 months)
>
> After three month, we want to close our position. At that time, the spot rate bid ask spread is 1.6210/1.6215. 
>
> (To close our position, we have to sell 10M GBP 3 months forward at a spot today)
>
> The 3-month  forward is 130/140. 
>
> First, we determine our bid. 
>
> 1.6210+0.0130 = 1. 6340
>
> Then we calculate value in AUD
>
> (1.6340-1.6100)$\times$ 10M = 240,000 AUD
>
> Which means we will have 240,000 AUD at the end of six month, we will have to discounted it back by three months using the 3 month libor rate.

## Parity Relations

A framework for developing a view about future exchange rate movements. 

**Parity relations** describe the  inter-relationships that jointly determine long-run movements in foreign exchange rate,  interest rates and inflation. 

It shows how:

* Expected inflation differentials 
* Interest rate differentials
* Forward foreign exchange rates
* Spot foreign exchange rates
* expected future spot foreign exchange rates

would be linked in an ideal world.

### Covered interest rate parity

Covered interest rate parity describes a riskless arbitrage relationship. 

> Under this parity condition, an investment in a foreign money market instrument that is completely hedged against exchange rate risk should yield exactly the same return as an otherwise identical domestic money market investment.

Supported where capital is permitted to flow freely.  Spot and forward foreign exchange rates are liquid, financial market conditions are basically stress-free.

However, the covered interest rate parity condition usually does not hold in short or medium term. Also the forward exchange rate is a poor predictior for the future exchange rate.

### Uncovered interest rate parity

On an uncovered (unhedged) foreign currency investment should equal the return on a comparable domestic currency investment. 

> Example
>
> $1+i_d = 1.05$ and $1+i_f = 1.10$ .
>
>  UIRP would then imply that 
>
> $(1+i_f)(1-\Delta S_{f/d}) -1 = i_d$

However, even when UIRP holds, the s.d of returns on $i_d$ is zero while the s.d of $i_f-\Delta S_{f/d} \ne 0$.  **UIRP** assumes risk-neutral.

If UIRP hold, no excess return could be gained by going long a high-yielding currency and short a low yielding one. No incentive to shift capital from one currency to anot

Empirical studies fails to hold over short and medium terms. Interest rate differentials are generally a poor predictor 

### Purchasing Power Parity

**Law of one price** stated that identical goods should trade at the same price across countries when valued in terms at a common currency. 

Foreign price of a good $P_f^x$ and the domestic price of a good $P_d^x$ . It should have 
$$
P_f^x = S_{f/d} P_d^x
$$
The absolute version of PPP extends the above formula to the general price levels. Assumes that all domestic and foreign goods are tradeable that price indices (d&f) are identical. 

Highly unlikely to hold. Because of transaction costs, trade impediments.

The relevant version of PPP assumes these costs are constant over time. We then have the formula
$$
\%\Delta S_{f/d} \approx \pi_f-\pi_d
$$
Where $\pi$ is the inflation rate. **Basically, the currency of the high inflation country should depreciate relative to the currency of the low inflation country.**

The concept of **real fix exchange rates** captures real purchasing power at a currency, defined in terms of the amount of real goods it can purchase internationally. 
$$
q_{f/d} = \frac{S_{f/d}P_d}{P_f} = S_{f/d}(\frac{P_d}{P_f}) - S_{f/d} \frac{CPI_d}{CPI_f}
$$
where $q_{f/d}$ is the real foreign exchange rates. 

**Empirical studies shows that real foriegn exchange *mean revert* in the long-run**. e.g: Nominal foreign exchange rates gradually gravitate towards their PPP-based values. 

### Fisher Effect and Real Interest Rate Parity

Combines both interest rate differentials and inflation differentials.

Given that the nominal rate = real rate + expected inflation. ($i = r+E(\pi)$)

Therefore, we have
$$
i_f - i_d = r_f - r_d +\pi_f-\pi_d
$$
Where $r_f-r_d$ is the **real** yield spread between  domestic risk free rate and foreign risk free rate and $\pi_f-\pi_d$ is the inflation differential. 

Since we observe the nominal rates $i_d,i_f$, and not real rates, we can then have
$$
r_f-r_d = (i_f-i_d) - (\pi_f-\pi_d)
$$
Note that from UIRP, we have $i_f-i_d = \%\Delta S_{f/d}$, and from PPP we have $\pi_f-\pi_d = \%\Delta S_{f/d}$. 

The fisher effect or real interest rate parity implies that

 $i_f-i_d = \pi_f-\pi_d$ 

which is the **International Fisher Effect.**

Empirical studies: there exists an interaction between nominal interest rates, exchange rates and inflation rates across countries. (Over longer time periods.)

International  Parity conditions serve as an anchor for longer-term exchange movements. 

### Example

> Given
>
> Australia's 1-year deposit rates are 5% while Japan's are 1%. The Australian dollar is estimated to be roughly 10% overvalued relative to the yen based on PPP. (Australia based)
>
> All else equal, which of the following events would restorn the Australian dollar to its PPP value?
>
> A. Japanese inflation rate increases by 4%.
>
> Wrong. Because the PPP value is $\pi_f-\pi_d $ . Since $\pi_f \uarr$ by 4%,  the difference between PPP and its current value will be widen. 
>
> B. The Australian inflation rate decrease by 10%
>
> Wrong. Same as above. This time, the $\pi_d \darr $ by 10%. The difference between PPP and its current value will be widen as well.
>
> C. The JPY/AUD exchange rate declines by 10%. 
>
> Correct. $\pi_f-\pi_d = \%\Delta S_{f/d}$ and $\%\Delta S_{f/d} = -10 \%$ . It will restore to its PPP value.  
>
> Given 
>
> If both the Australian and Japanese CPI price levels increased by 5%, all else equal, then the change in the real exchange rate qJPY/AUD would be closest to 
>
> A. 0% B. 5% C. 10%
> $$
> q_{f/d} = S_{f/d}(\frac{CPI_d}{CPI_f})
> $$
> Threfore the change would be close to 0%. A.
>
> If the real interest rates in  Japan and Australia were equal, then under the international Fisher effect, the inflation rate differential between Japan and Australia would be closest to A.0%  B. 4%  C.10%
>
> Fisher effect stated that $i_f-i_d = \pi_f-\pi_d$ and we are given $r_f-r_d = 0$
>
> Therefore, it should be equal to 4%. 

If all international parity conditions held:

$\%\Delta S_{f/d}^e = \text{forward premium/discount} = i_f - i_d = \pi_f -\pi_e$

![image-20200225110452012](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20200225110452012.png)

If all conditions held, it would be impossible for a global investor to earn consistent profits on currency movements. 

## Assessing Equilibrium

3 approaches to derive long-run equilibrium exchange rate assessments. 

**Learned from Level 1: The balance of current account and capital account must sum to zero.**

### Macroeconomic Balance Approach

Estimates how much foreign exhcange rates need to adjust in order to close the gap between the medium-term expectation for a country's current account balance and the country's normal or sustainable current account imbalance. 

### External Sustainablility approach

Focuses on stocks of outstanding assets or debt: how much foriegn exchange rates need to adjust to ensure that a country's net foreign asset/GDP ratio or net foreign liability/GDP ratio stability. 

### A reduced form econometric model

Seeks to estimate the equilibrium path that a currency should take on the basis of the trends in several key macro variables. 

Empirical observations: Predict Direction but poor on magnitude. Also tend to over predict. 

**International parity relations specify relationships, these 3 approaches attempt to explain some of the mechanisms taht help realogn foreign exchange rates.**

### With PPP

|                       | PPP Overvaluation                      | PPP Undervaluation                      |
| --------------------- | -------------------------------------- | --------------------------------------- |
| Current Asset Surplus | Overvalued Currency, trade surplus (1) | Undervalued Currency, Trade surplus (3) |
| Current Asset Deficit | Overvalued currency, trade deficit (2) | Overvalued Surplus, trade deficit (4)   |

For situation (2), encourage depreciation to bring foreign exhcange rate closer to long-run fair vale. For situation (3), encourage appreciation. 

## Carry Trade

The **UIRP**, states that

* High-yield currencies are expected to depreciate
* Low-yield currencies are expected to apprecate

However, there are significant evidence that UIRP does not hold short and medium term time periods. Which opens up a trading strategy called the **Carry Trade.**

Take long positions in high yield currencies and short positions in low yield currencies (Funding currencies). Earns positive excess returns in most market conditions. 

However, volatility and perceived risk can cause these positions to unwind fast. Referred as **crash risk.**

Carry trades use considerable leverage, usually 50 to 200 times. 

> Use of a volatility filter: 
>
> If an average level foreign exchange volatility falls below some threshold, open carry trade positions.
>
> If  volatility rise above some threshold, close carry trade positions.

Use of PPP:

Avoid the risk of depreciation: Set an upper PPP band for long position in high yield currency. 

Avoid the risk of appreciation: Lower PPP band for short position in low yield currency.

Policy perspective: Concern that carry trade activities may be generating foreign exchange rate misalignments. 

Unwinding a large carry trade could cause a financial crisis. 

### Example

|      | 1-yr Libor | Pair            | 1-yr later |
| ---- | ---------- | --------------- | ---------- |
| JPY  | 0.1%       | JPY/USD =81.30  | 80         |
| AUD  | 4.5%       | USD/AUD = 1.075 | 1.0803     |

From the table, we know that AUD is depreciating and JPY is appreciating. 

Borrow in Yen, invest in 1-year AUD Libor

After 1 year, the all-in return is 
$$
JPY/AUD = JPY/USD \times USD/AUD \\
Originally: 81.3\times 1.0750 = 87.4\\
One-year-later: 80\times 1.0803 = 86.42
$$
The all-in return is then calculated as 

The one AUD we invest, at the end of the year will be $1+4.5\% = 1.045$

The return is 
$$
\frac{86.42}{87.4} \times 1.0450 - 0.001
$$
Where can be generalized as
$$
\frac{\text{original exchange rate}}{\text{end exchange rate}}\times(1+\text{invested currency risk free yield})\\-\text{borrowed currency risk free rate}
$$

## Balance of Payments Impacts

Sum of all recorded transactions in the traded goods, services, income and net transfer payments, is called the  **current account.**

Assuming a country has a free exchange rate:

Persistent current account deficits $\Rarr$ Currency Depreciation Over time

Persisitent current account surplus $\Rarr$ Currency Appreciation Over time

$|\text{Capital Account}| = |\text{Current Account}|$  

**Financial flows, investment or financing decisions are usually the dominant factor in determining exchange rate movements in the short to intermediate term.** 

Why?

* Prices of real goods/services tend to adjust much more slowly while financial asset adjust quickly. 

* Production of real good and services takes time while liquid financial markets instaneous redirection of fiancial flows. 

* Current spending/production decisions reflect only purchases/sales of current production while investment/financing decisions reflect not only the financing of current expenditures but also reallocatioon of existing portfolios. 

* Expected exchange rate movements can induce very large short-term capital flows. Actual foreign exchange rate very sensitive to the currency views held by the owners/managers of liquid assets. 

### Real interest rate differentials, capital flows and the foreign exchange rate

$$
q_{f/d} =\bar{q}_{f/d}  +[(r_d-r_f)-(\phi_d-\phi_f)]
$$

Where $q_{f/d}$ is the real foreign exchange rate, $\bar{q}_{f/d}$ is the real long-run equilibrium rate. $r_d -r_f$ is the real interest rate differential while $\phi_d-\phi_f$ as the perceived sustainability of the country's external balances. 

In short, capital responds to the interest rate differentials, risk premia and expectations which is the foreign exchange rate movements. 

Interest rate differentials, carry trades, and foreign exchange rates. 

The above formula can be further break into
$$
q_{f/d} =\bar{q}_{f/d}  +[(i_d-i_f)-(\pi_H^e-\pi^e_L)-(\phi_H-\phi_L)]
$$

Where the $i_d-i_f$ is the yield spreadwidens and $\pi_H-\pi_L$ is the inflation expectations spread tightens, and $\phi_H-\phi_L$   is the risk premia Spread Tightens. 

 Howerver, inflation tightens and risk premia spread tightens are not observable.

Combat inflation by raisiong interest rates (Monetary Policy)

Policies of lower government debt, financial market liberalization, removal of capital flow restrictions, attraction of FDI. 

Carry trade profitability  = f(monetory, fiscal, economic policies).

Euqity market trends has no stable relationship with foreign exchange rates.

## Monetary and Fiscal Policies

### Mudell-Fleming Model

Expansionary (increase aggregate demand and output)

* Monetary Policy:
	* Reduce Interest rates
	* Increase investment and consumption spending.
	* Leads to capital outflows, downward pressure on foreign exchange rate.
	* For a fixed foreign exchange rate:
		* Central banks will have to buy its own currency to deplete foreign exchange reserves. (To support currency)
		* This will tightens domestic credit conditions, while offsets intended excpansionary policy. 
* Fiscal Policy
	* Increase spending and lower taxes.
	* Exerts upward pressure on interest rates (larger deficits need to be financed)
	* Leads to capital inflows, upward pressure on foreign exchange rates. 
	* For a fixed exchange rate:
		* Central bank will have to sell its currency and build reserves. 
		* This expands domestic money supply. Reinforces expansionary policy.

The more responsive capital flows are to interest rate differentials, the larger foreign exchange depreciation. 

If a domestic policymakers try to 

a) Pursue independent monetary policy

b) Permit capital to flow freely across national borders

c) Defend foreign exchange rates

**All 3 cannot be satisfied at same time**. Low capital mobility effects primarily through trade flows. **Capital control would be required for a) and c) to be satisified.**

Expansionary Fiscal Policy: Government is spending more money. Upward pressure on interest rate.

Restrictive Monetary Policy: Central bank is raising interest rate. 

#### For a high capital mobility

|                            | Expansionary Monetary Policy  | Restrictive Monetary Policy                            |
| -------------------------- | ----------------------------- | ------------------------------------------------------ |
| Expansionary Fiscal Policy |                               | Interest rate going up. Domestic Currency Appreciates. |
| Restrictive Fiscal Policy  | Domestic currency depreciates |                                                        |

#### For a low capital mobility

|                            | Expansionary Monetary Policy                                 | Restrictive Monetary Policy                                  |
| -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Expansionary Fiscal Policy | Domestic currency depreciates. Trade balance depreciate because import increase. |                                                              |
| Restrictive Fiscal Policy  |                                                              | Interest rate going up. Domestic Currency Appreciates. Trade blance appreciate because import decrease. |

### The monetary approach

Mundell Fleming approach:

Monetary policy $\rarr$ interest rates $\rarr$ foreign exchange rates

Monetary approach:

Monetary policy $\rarr$ price level rate of inflation $\rarr$ foreign exchange rate.

As per quantity theory of money $\Rarr$ money supply changes are the primary determinant of price level changes.  

It assumes PPP holds $\Rarr$ a money supply induced increase in domestic price 

Shortcoming assumption of PPP holding of all times. Monetary approach may not realistically explain policy effects on foreign exchange rates.

### Dornbush overshooting model

Prices exhibit limited flexibility in the short run, fully flexible in the long run. 

In the short run, real money supply goes up, interest rate goes down, capital outflow, and then foreign exchange rate goes down but overshoots on a very short basis. 

### Interventions

There are interventions to push capitals outside domestic economy, and there might be interventions to pull capitals to the foreign economy.

#### Push

* Take a greater global allocation (Portfolio approach)
* Low interest rates

#### Pull

* Flexible currency exchange rates.
* Low debt levels.
* High interest rate
* Low debt levels

**There are certain risks associate with pull interventions. To avoid excessive surges of capital inflows, typically followed by huge outflows. Use of a) Capital controls b) foreign exchange market intervention.**

### Currency Crises-Warning Signs

1. $q_{f/d} $ (real exchange rate) substantially higher than its mean level during peachful periods.
2. Forexign exchange reserves decline peciptiously as the crisis approaches.
3. Some deterioration in terms of trade
4. CPI significantly higher pre-crisis vs tranquil periods.
5. $M_2/Bank$ reserves tends to rise in the 24-month period lead up to a crisis. 
6. Broad money growth (nominal and real) rises sharply in the 2 years leading up to a crisis.
7. Nonmial private credit growth sharply pre-crisis. 
8. Typically some form of equity market boom. 

## Growth Factors

Factors $\Rarr$ economic growth $\Rarr$  earnings expectations $\Rarr $ equity prices.

Factors $\Rarr$ economic growth$\Rarr$Growth rate of real incomes $ \Rarr$  real interest rate $\Rarr $  real returns. 

Economic growth $\Rarr $ Actual $-$ Potential (Long-run aggregate output, growth rate of potential GDP).

### Comparing Economic Performance

The percentage change in real GDP, measures how rapidly the economy is expanding.

The percentage change of real GDP per capita, reflects the anverage standard of living. 

To compare and convert each country's real GDP to a common currency, typically USD at a **PPP exchange rate**. 

Why not use market foreign exchange rates?

* Too volatile
* Foreign exchange rates reflect **traded** goods and services and financial flows, while some goods and services are not traded.

Developed (High GDP/Capita) vs Developing (Low GDP/Capita)

#### Savings and Investment

Low Savings $\Rarr $ Low investment $\Rarr $ Slow GDP growth $\Rarr $ persistently low incomes. 

A low income will feedback to low savings. To break this circle, is to increase investment even with low savings. 

#### Financial Markets and Intermediaries 

Promote growth by 

* Allocating capital to projects. 
* Encouraging savings by creating investment products. 
* Overcoming credit constraints.

Countries with better functioning financial markets and intermediaries grow at a faster rate. 

#### Other growth factors

Political stability, rule of law, and property rights, education and health care systems,  tax and regulatory system, free trade, and unrestricted capital flows.

## Stock Market and Economy

**Potential GDP places a limit on how fast an economy can grow.** 

Question: Is earnings growth also limited by growth rate of potential GDP?

For earnings growth > Potential GDP growth,  

the ratio of  $\frac{\text{Corporate Profit}}{GDP}$ must be increasing.
$$
P = GDP(E/GDP)(P/E)
$$
Where we have

$P$ is the aggregate value of stock market. *E* is aggregate earnings.

$E/GDP$ is expressed as log rates of change over time horizon T. 
$$
(1/T)\%\Delta P =(1/T)\%\Delta  GDP+ (1/T)\%\Delta (E/GDP)+ (1/T)\%\Delta (P/E)
$$
In the long run, the same factors that limit economic growth, also limit aggregate earnings growth.  

Growth rate of potential GDP is the determinant of level of real interest rates. 

For $(y-y^*)$ , as $y^* \uarr$, inflationary pressure decrease even as y increases. Thus higher incomes require higher rates to induce savings. 

Also, higher g in $y^*$ improves the general credit quality of issuers. 

($y^*$ is the potential GDP).

## Determinants of Economic Growth

### Simple Production Function

$$
y = A\cdot F(K,L)
$$

Where K is the capital and L is labor, and A is a scale factor known as the **total factor productivity.**

#### Cobb-Douglos Production Function

$$
F(K,L) = K^{\alpha}L^{1-\alpha} , 0 < \alpha <1
$$

Factors of production are paid their marginal product. 

Profit max requires: MPK = rental price of capital, and MPL = real wage rate. 

#### Derivation

$$
MPK = \frac{\delta y}{\delta K} = \alpha AK^{\alpha-1}L^{1-\alpha}=r\\
MPL = \frac{\delta y}{\delta L} = (1-\alpha) AK^{\alpha}L^{-\alpha}=w_r\\
$$

where $w_r$ is the real wage rate. 

In other words, $\alpha$ is the share of GDP paid out to the suppliers of capital. 

#### Properties

* Constant return to scale: Double input, double output.
* Capital-to-labor ratio: $y/L = AF(K/L, L/L) = AF(K/L,1)$ . The amount of goods a worker can produce depends on the amount of capital for each worker (K/L), TFP (A) and the share of capital in GDP. 
* Diminishing marginal productivity: The extra output obtained from each additional unit of input will decline. A $\alpha$  close to zero means diminishing marginal returns to capital is very significant. 
* An increase in K/L reflects rising investment stops when MPK = r.
* Capital Deepenings:  the capital per worker is increasing in the economy.

#### Example

>Country A
>
>K/L = $100,000
>
>Country B
>
>K/L = $5000
>
>What effect on growth rate of potential GDP of 
>
>* Increase Investment in both countries. Capital deepenings:
>	* A smaller effect for A. 
>	* And a larger effect for B. 
>* Increase University reasearch in both countries. 
>	* Likely impact on TFP: A-raise potential GDP, B-raise potential GDP
>* Eliminate restrictions on foreign investment for country B
>	* I increase, raise potential GDP for country B.

### Growth Accounting

Growth accounting equation is used to measure potential GDP. 
$$
\frac{\Delta y}{y} = \frac{\Delta A}{A} +\alpha \frac{\Delta K}{K}+(1-\alpha)\frac{\Delta L}{L}
$$
Where we can state that 

the growth rate of output = rate of technological change+ growth rate of capital + growth rate of labour. 

Increase in growth rate of labor will have a larger impact than capital. 

y, L and K: data are avaliable from GDP accounts. A must be estimated.

To estimate potential GDP, we need 

trend estimate for labor and capital. A is treated as exogeneous. 

Alternative method: 

growth rate in potential GDP = long-term growth rate of labour force + long-term in labour growth rate in labour productivity

Growth rate  in potential GDP: long-term growth rate of labor force, and a long-term growth rate in labor productivity. 

Further extension:
$$
y = A \cdot F(N,L,H,K_{IT},K_{NT},K_P)
$$
where N is natural resources, L is labour, quality of labour, $K_{ICT}$ is ICT capital (Information and Communication Technology). $K_{NT}$ is non-ICT capital, and $K_P$ is the public capital. 

Access to resources is important. 

**For natural resources, access to these resources, such as trade, is more important than the ownership or production of natural resources**. 

> The Curse of Natural Resource:
>
> Simply fail to develope the economic institutions to support growth.
>
> Strong export demand for their resources may drive up the currency and make other sectors uncompetitive. 

Labor supply: Labour force = working age population that is either employed or avaliable for work. 

Depends on: 

* Population growth
* Labor force participation
* Average hours worked
* Net immigration: Boost potential GDP. However, if a country is running a persistent output gap, increased immigration will make it worse and increase unemployment. 

Issues: 

Techonological advancement and net immigration increases potential GDP but may also potentially increase unemployment. 

###  Growth Theories

#### Classical  Model

$y = F(L,land)$

Growing population, limited resources, leads to the growing population. 

When income/per capita > subsistence level: technological progress (labour productivity) + land expansion = higher population growth. 

But this is **temporary. **

Diminishing marginal returns + higher populations $\Rarr$ incom / per capita falls back o subsitence level. 

The failurre of the classical model:

* as income/per capita increases, population growth slows, not accelerates.
* growth rate of techonological progress > rate of diminishing returns

#### Neo-classical growth model (Solow growth model)

$$
y = AF(K,L) = AK^\alpha L^{1-\alpha}
$$

GDP gowth rate per capita is related to three factors:

* Rate of tech change
* pop growth
* Savings/Investment rate

Equilibrium state = steady state rate of growth

Output per worker: y = Y/L

Capital per worker: k = K/L

Rate of change of k: $\frac{\Delta k}{k} = \frac{\Delta K}{K} - \frac{\Delta L}{L}$ 

Rate of change of y:  $\frac{\Delta y}{y} = \frac{\Delta Y}{Y} - \frac{\Delta L}{L}$

What is $\Delta K$:

$K_{t+1} = K_t +I- \delta$ 

K increases by I and Decreases by depreciation
$$
I = sy - \delta K
$$
where s is the saving rate and $\delta$ is the depreciation rate. 

And therefore 
$$
\Delta K - sY - \delta K
$$
Then we have
$$
\frac{\Delta k}{k} = \frac{\Delta K}{K} - \frac{\Delta L}{L}\\
  = \frac{sy}{K} - \delta - \frac{\Delta L}{L}
$$
**In the steady state: growth rate of capital per worker = growth rate of output per worker**
$$
\frac{\Delta k}{k} =  \frac{\Delta y}{y} = \frac{\Delta A}{A} +\alpha\frac{\delta k }{k}\\
\frac{\Delta k}{k} - \alpha \frac{\Delta k}{k} = \frac{\Delta A}{A}\\
\frac{\Delta y}{y} = \frac{\Delta k}{k} = \frac{\Delta A}{A}\cdot \frac{1}{1-\alpha}
$$
Let $\theta$ be the growth rate of total factor production. $\theta = \frac{\Delta A}{A}$

Then we have 
$$
\frac{\Delta y}{y} = \frac{\theta}{1-\alpha}
$$


which is **the growth rate of  output per capita. **

The last step is to substitute $\frac{\theta}{1-\alpha}$ into  $\frac{\Delta k}{k} = \frac{sY}{K} - \delta  - \frac{\Delta L}{L}$

Then we would have 
$$
\frac{Y}{K} = \frac{1}{S} [(\frac{\theta 
}{1-\alpha})+\delta+\frac{\Delta L}{L}]
$$
So in a steady state, $\frac{Y}{K} $ is constant. k and  y are both growing at the same speed $\frac{\theta}{1-\alpha}$



In the steady state, savings = investment, and therefore
$$
S_y = [(\frac{\theta}{1-\alpha})+\delta +n ]k
$$
where $S_y$ is savings per worker. 

$[(\frac{\theta}{1-\alpha})+\delta +n ]$  is the invesntment required to keep K constant. 

$n$ is the work force. 

#### Implications

1. Capital Accumulation
	* affects level of output, not growth rate
	* economies move towards a steady state
	* does not depend on a capital accumulation
2. Deepening vs Technology
	* growth slows as capital is added
	* capital deepenng limits out
	* without increase in TFP, growth of y will slow. 
3. Convergence
	* Growth rate of developing countries should exceed that of developed countries
	* Per capita incomes should converge
4. Effect of S(Savings) on growth 
	* S increases growth rate until a steady state is reached
	* in steady state, growth does not depend on S
	* countries with higher saving rates, have  higher y, k and Total Factor Production. 

#### Endogenous Growth Theory

* Technological progress is not exogenous 
* Economy does not necessarily converge to a steady state of growth. 
* No diminishing marginal returns to capital for the economy as a whole. 
* Increasing savings permanently increase rate of economc growth. Definition of capital is broadened o include knowledge and research and development ideas. 
* The model is 

$$
y_c = f(k_c)=Ck_c
$$

$y_c$ output per woker is proportional to capital per worker. 

C is the constant marginal production per capital (MPK). 

If private sector under-invest in research and development, direct government spending and or research development tax breaks and subsidies may correct the situation. 

#### Convergnce

* Absolute convergnce:developing countries will eventually catch up with developed countries. 
* Conditional convergence: convergence is conditional on instituions and certain input fators being similar
* Route to convergence: 
	* Capital accumulation and capital deepening
	* imitation and adoption of technology

## Economics of Regulation 

### Economic Rationale

Regulations are necessary since market solutions are not adequate for all situations. (Market Failure)

### Fundamental theorem of welfare economics 

**A competitive equilibrium alloctaions are pareto optimal.** 

Which means **Everyone is as well off as they can get for a given allocation. ** 

Also called **Economics efficiency. **

But because there are **information frictions** and **externalities** disrupts economic efficiency. 

**Externalities can be both positive and negative. **

Also need regulation to prevent weak competition and provide social objectives.

### Regulations of Financial Markets

* Protection of investors
* Creating confidence in markets
* Enhancing capital formation
* Ensuring safety and soundness of financial institutions
* Securities registration requirenments 
* Disclosure requiremnents

### Regulation of Commerce

* Role of government is to promoting comerce locally, nationally and globally. 
* Trade agreements
* Establishing the legal framework for contracting 
* Labour markets 
* Immigration 
* Safety(drugs, etc)
* Recognition and protection of intellectual property. 
* Technical standards. 

### Regulators 

There are public regulators and private regulators. Public regulator is government and private regulators are industry regulators. 

**SRO, self-regulatory organizations has been given the authority and enforcement power by the government. While industry self-regulatory bodies do not have the force of law.**

Regulatory tools: should be consistent with maintaing a stable regulatory environment. 

* Price mechanism: taxes, subsidies, floor and ceiling prices. 
* Regulatory  mandates, restrictions on behaviour
* Support private entity

#### Benefit and cost 

Regulatory Burden referes to the costs of regulation for the regulated entity. 

**Net regulatory burden = private costs of regulation - private benefits of regulation.**

Impact on revenues, impact on costs and higher business risk. 

# Derivatives

## Forward and Futures Prices

### Arbitrage Free Pricing Valuation 

> Assumptions for arbitrage-free pricing valution
>
> * Replicating instruments are identifiable and investable 
>
> * Market frictions are ignored, short selling is allowed. 
> * Borrowing and lending are available at a known risk-free rate. 

S rerpresenting underlying 

F representing forward and f representing futures. 

V is the value of forward and v is the value of futures 

***At the contract initiation is the value of a futures or fowards contract = 0.***

#### Future value

Because futures are marked to market, therefore 

$v_t = f_t - f_{t-1}$ This is before everyday settlement. 

After settlement, $v_t = 0$

Assuming no underlying cash flows, 

$F_0 = S_0e^{rt} $  continous compounding. 

$F_0 = S_0(1+r)^t$ periodic compounding. 

Example:

>$S_0 = 100$
>
>$r_f = 5%$
>
>T = 1 yr
>$$
>1. \text{Borrow \$100 for one year.}\\
>2. \text{Buy} S_0\\
>3. \text{Sell} F_0\\
>4. \text{Payback loan of } S_0e^{rt} \text{ at Time T}
>$$

**The quoted forward price does not directly reflect expectations of future underlying prices, only the cost of carry.** 

The value of the **Forward** contract is
$$
V_t = \frac{F_t - F_0}{(1+r)^{T-t}}\\
or \\
V_t = S_t - \frac{F_0}{(1+r)^{T-t}}
$$


When there are underlying cash flows.

Let $\gamma$ be the benefit of carrying and $\theta$ be the cost of carry. 
$$
F_0 = [S_0 + PV(\theta) - PV(\gamma)](1+r)^T
$$
When the underlying with known yield

 Assuming continuous yield 
$$
F_0 = S_0e^{(r_e + \theta - \gamma)T}
$$
**Note it is plus cost minus benefit.** 

#### Equities Forward

> Example
>
> The continuously compounded dividend yield on the EURO STOXX 50 is 3%, and the current stock index level is 3,500. The continuously compounded annual interest rate is 0.15%. Based on the carry arbitrage model, the three-month futures price will be *closest* to:
>
> Solution:
>
> Continuosly compounded dividend yield  3%
>
> $\gamma = 3\% $ 
>
> Current stock index is at 3500 
>
> $S_0 = 3500$ 
>
> Continously compounded annual inter interest rate is 0.15%
>
> $r_c = 0.15\% $
>
> Three month future contract 
>
> T = 0.25
>
> So 
>
> $F_0 = S_0 e^{(r_c-\gamma)T} = 3500e^{(0.0015-0.03)0.25} = 3475.15$
>
> Suppose Nestle common stock is trading for CHF70 and pays a CHF2.20 dividend in one month. Further, assume the Swiss one-month risk-free rate is 1.0%, quoted on an annual compounding basis. Assume that the stock goes ex-dividend the same day the single stock forward contract expires. Thus, the single stock forward contract expires in one month.
>
> 2.20 is already the dividend in one month. 
>
> $F_0 = S_0 (1+r)^T - \gamma = 70(1.01)-2.02 = 67.858 $



Another example about forward:

>Suppose we bought a one-year forward contract at 102 and there are now three months to expiration. The underlying is currently trading for 110, and interest rates are 5% on an annual compounding basis. If there are no other carry cash flows, the forward value of the existing contract will be closest to:
>
>First, let's bring the forward contract to three month later, 
>
>$F_t = 110(1.05)^{0.25}  = 111.3499$
>
> Subtract the contract price we have $111.3499-102 = 9.3499$
>
>Then we discount it back three month to the current foward value of exisiting contract is $\frac{9.3499}{1.05^{0.25}} = 9.2365$
>
>Another way to deal with it is to bring the contract three month back
>
>$110-\frac{102}{1.05^{0.25}} = 9.2365$ 
>
>If a dividend payment is announced between the forward’s valuation and expiration dates, assuming the news announcement does not change the current underlying price, the forward value will most likely:
>
>**Decrease.**
>
>$S_0 + Cost - Benefit = F_0$

#### Interest rate forward

Underlying is a forward interest rate on a deposit. 

Pay fixed received floating is a long position on a forward contract.

Pay floating received fixed is a short position on a forward contract. 

No exchange of the notional amount. 

FRA is the fixed interest rate that eliminates arbitrage. 

A $3 \times 9$ FRA is the rate on a deposit that begins in 3 months and lasts for 6 months. 

That implies the forward rate of $f(3,6)$ . 

Receiving Floating
$$
\frac{Notional \ Amount(\text{Float rate} - \text{fixed rate})(days/360)}{1+\text{float rate(days/360)}}
$$
Receiving Fixed 
$$
\frac{Notional \ Amount(\text{Fixed rate} - \text{Floating rate})(days/360)}{1+\text{float rate(days/360)}}
$$
Example

>In 30 days, a UK company expects to make a bank deposit of £10,000,000 for a period of 90 days at 90-day Libor set 30 days from today. The company is concerned about a possible decrease in interest rates. Its financial adviser suggests that it negotiates today, at Time 0, a 1 × 4 FRA, and instrument that expires in 30 days and is based on 90-day Libor. The company enters into a £10,000,000 notional amount 1 × 4 receive-fixed FRA that is advanced set, advanced settled. The appropriate discount rate for the FRA settlement cash flows is 0.40%. After 30 days, 90-day Libor in British pounds is 0.55%.
>
>Because we know that a 90-day libor is 0.55% after 30 days. 
>
>![image-20200927102258682](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20200927102258682.png)
>
>The interest actually paid at maturity on the UK company's bank deposit will be closest to?
>
>10,000,000 is going to deposit. And the cost of deposit (interest) is $10M(0.0055(90/360)) = 13750.$
>
>If the FRA is initially priced at 0.60%, the payment received to settle it will be closest to :
>
>Because we are receiving fixed and payfloating:
>
>The payment we need to settle it will be closest to :
>$$
>\frac{NA(fxrate-flrate)(90/360)}{1+0.004(90/360)} = 1248.75
>$$
>If the FRA was initially priced at 0.5%, the payment received to settle it will be closest to 
>$$
>\frac{10M(0.005-0055)(90/360) }{1+0.004(90/360)}
>$$
>If we know L(180) = 1.5% and L(270) = 1.75%, what is the FRA $3\times9$ ? 
>
>[1+0.175(270/260)] = [1+0.015(180/360)]*[1+x(90/360)]
>
>x = 2.233%



Example

>Suppose we entered a receive-floating 6x9 FRA at a rate of 0.86%, with
> notional amount of C\$10,000,000 at Time 0. The six-month spot Canadian dollar (C​\$) Libor was 0.628%, and the nine-month C\$ Libor was 0.712%.
> Also, assume the 6 x 9 FRA rate is quoted in the market at 0.86%. After 90 days have passed, the three-month C\$ Libor is 1.25% and the six-month C$ Libor is 1.35%.
>
>Assuming the appropriate discount rate is C$ Libor, the value of the original receive-floating 6 x 9 FRA will be closes to:
>
>First, we calculate the implied forward rate at t = 90
>
>L(90) = 1.25% while L(120) = 1.35%
>$$
>[\frac{1+0.0135(180/360)}{1+0.0125(90/360)}-1]\times4 = 0.0145
>$$
>Then we calculate the difference between implied rate and contract rate multiply the nontonal amount, which is the value of the contract.
>$$
>\frac{10M(0.0145-0.0086)90/360}{1+0.0135(180/360)} = 14651.10
>$$

#### Fixed income forwards

Full Price = Net Price + accrued interest

Fixed income futures contracts are based on a generic bond.

**Fixed income futures contracts are based ona generic bond. And therefore underlying may not equal to deliverable.**

The price to be paid to the short side on delivery is (quoted price $\times$ Conversion Factor+Accrued Interest)

##### The cheapest-to-deliever bond 

Example

>Future contract closed at 93.25
>
>| PV(net price) | Conversion Factor |
>| ------------- | ----------------- |
>| 99.50         | 1.0382            |
>| 143.5         | 1.5188            |
>| 119.75        | 1.2615            |
>
>For the fist bond:
>Cost to deliever is $99.5-93.25\times1.0382 = 2.69$
>
>For the second bond:
>
>Cost to deliever is $143.50-93.25\times1.5188 = 1.87$
>
>For the third bond:
>
>Cost to deliever is $119.75-93.25\times 1.2615 = 2.12$ 



On day 0, we borrow money. 

![image-20201002083805303](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201002083805303.png)



So on day 0, we owed
$$
[(S_0+AI)-\frac{I}{(1+r)^T}](1+r)^T
$$
Sell our bond at
$$
S_T = ?\\
AI \text{Known Amount}
$$
So the future price is 
$$
F_0 =[(S_0+AI)-\frac{I}{(1+r)^T}](1+r)^T - AI
$$
Then we have the quoted future price is 
$$
QF_0 =  \frac{F_0}{CF}
$$
Example

>![image-20201002105136956](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201002105136956.png)
>
>Known: CTD = 12% Bond  Coupon is semi-annually
>
>PV = 120, CF = 1.4
>
>---------------------------------------
>
>We have 
>$$
>F_0 =[(S_0 +AI)-\frac{I}{(1+r)^t}](1+r)^T\\
> = [(120+6 (60/182))- 6/(1.1)^{122/365}](1.1)^{270/365} = 124.651885\\
> QF = F_0 / CF
>$$

#### Currency Fowards and Future

If the $r_f = r$ then we have $F_0 = S_0$  if $r_f >r$ Then $F_{f/d} > S_{f/d}$

Because 
$$
F_{f/d} = S_{f/d} \frac{(1+r_f)^T}{(1+r_d)^T}
$$
Example 

Given 
$$
S_{GBP/EUR} = 0.792 \\
r_{GBP} = 1\% \\
r_{EUR} = 0.3\%\\
T = 1yr
$$
We have 
$$
F_{GBP/EUR} = S_{GBP/EUR}\cdot \frac{(1+r_{GBP})^1}{(1+r_{EUR})^1}
$$


Example

>A corporation sold €10,000,000 against a British pound forward at a forward rate of £0.8000 for €1 at Time 0. The current spot market at Time t is such that €1 is worth £0.7500, and the annually compounded risk-free rates are 0.80% for the British pound and 0.40% for the euro. Assume at Time t there are three months until the forward contract expiration.
>
>![image-20201002125813101](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201002125813101.png)
>
>The spot rate at time t :
>
>$S_{GBP/EUR} = 0.75$
>
>Then we have the forward exchange rate at:
>
>$F_{GBP/EUR} = 0.75\frac{(1+0.008)^{3/12}}{(1+0.004)^{3/12}} = 0.7507$
>
>Value of the contract is 
>$$
>\frac{10M(0.8 - 0.7507)}{(1+0.008)^{3/12}}
>$$



## Swaps

### Interest rate swaps 

Since the $B_{fl} = 100$ at a reset date, solve for PMT to find the fixed rate. 
$$
1  = \frac{PMT}{1+r_1}+\frac{PMT}{(1+r_2)^2}+\cdots+\frac{PMT+1}{(1+r_n)^n}
$$
Zero rates for maturities. Let $DF_t = \frac{1}{(1+r)^T}$

Since that 
$$
1 = PMT\cdot DF_1 + PMT \cdot DF_2+\cdots +PMT \cdot DF_n 
$$
Therefore 
$$
PMT = \frac{1-DT_n}{\sum DF}
$$
To assess the value of the swap contract, just calculate the value of its offset:

A received fx pay float contract at time 0 has the same value of a receive floating pay fixed swap at time t. 

The value of the swap contract at time t is 
$$
V_{Swap} = (r_{fixed_0} -r_{fixed_t}\sum DF \cdot NA )
$$
Given current libor we have 
$$
V_{swap}  = V_{fix_0} - V_{fix_t}\\
 = (PMT_0 \cdot DF_1 + PMT_0 \cdot DF_2 + PMT_0 \cdot DF_3 + \cdots PMT_0 \cdot DF_n +DF_n)\\
 - (PMT_1 \cdot DF_1 + PMT_1 \cdot DF_2 + PMT_1 \cdot DF_3 + \cdots PMT_1 \cdot DF_n +DF_n)\\
 
$$
Example

>Two years ago, we entered into a swap for \$100M, 7 years receive fx, pay libor with annual resets, swap rate was 2%. And the swap rate at t = 2 is 1.2968
>
>| Maturity | Discount Factor |
>| -------- | --------------- |
>| 1        | 0.99099         |
>| 2        | 0.977876        |
>| 3        | 0.965136        |
>| 4        | 0.951529        |
>| 5        | 0.937467        |
>
>$V_{swap} = (r_{fx0} - r_{fxt})\sum DF \cdot NA$

### Currency Swap

The value of a currency swap is calculated as $V_{SWAP} = V_D - S_0V_F = 0$

And at time t, $V_{SWAP} = V_D - S_t V_F$

Example

>US company wants \$100M AUD for 1 year. 
>
>Used 1 year currency swap with quarterly resets 
>
>AUD/USD  = 1.14 
>
>![image-20201002210106455](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201002210106455.png)
>
>![image-20201002210144132](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201002210144132.png)
>
>Because it is quartely settled
>
>Each quarter, US company gives $\frac{0.02769\cdot 100M}{4}$  \$AUDto Austrilia company. While AUD company pays $\frac{0.002497(100M/1.14)}{4}$  USD

### Equity Swap

Three types of equity returns

* Pay fixed  $NA  (R_e - r_{fixed})$
* Pay floating $NA(R_e - r_{floating})$
* Pay equity $NA(R_{ea} - R_{eb})$

## Valuation of Contingent Claims

### Binomial Option Valuation Model

#### Delta

Delta is the change in option price to the change in stock price. 
$$
\Delta = \frac{C^+-C^-}{S^+-S^-}
$$
$\Delta $ is the number of shares. 

Make up a portfolio that is same as a bond

![image-20201003233953952](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201003233953952.png)

|                   | Payoffs             | Loan PMTs           |
| ----------------- | ------------------- | ------------------- |
| u(stock px go up) | $\Delta S^+ - C^+ $ | $-\Delta S^+ - C^+$ |
| d                 | $\Delta S^- - C^-$  | $-\Delta S^- + C^-$ |

Therefore, we have 
$$
PV(-\Delta S^+ + C^+ ) = \Delta S- C
$$
Then we have the no-arbitrage price of a call option
$$
C = \Delta S + PV (- \Delta S ^+ + C^+)
$$


e.g

![image-20201003235232244](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201003235232244.png)


$$
\text{Payoff}^+  = \text{Payoff}^-\\
\Delta S^+ - C^- = \Delta S^- - C^-\\
\Delta = \frac{C^+ - C^-}{S^+ - S^-} = \frac{1}{4}
$$
Then we have the payoff as $\text{Payoff} = 4.5$

So we have the value of the call option as 
$$
C = \Delta S - PV(\text{Payoff})=0.755
$$
![image-20201004000340729](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004000340729.png)



Now, for put. 

Because we have a hedged position, and the put is benefit from stock px going down. So $\Delta <0$ .So that $\Delta S $ benefit from px going up. 

The payoff would then be 
$$
\text{Payoff}^ - =  - \Delta S^+ + p^+\\
\text{Payoff}^+ =  - \Delta S^- + p^-
$$
We would have a negative delta as 
$$
\Delta = \frac{p^+ - p ^-}{S^+ - S^-}
$$

#### Pi

$\pi$ is risk neutral probability.  **The probability of the underlying px goes up. **
$$
\pi = \frac{1+ r - d}{u - d}
$$
Where the 
$$
c = PV[\pi c^+ + (1-\pi)c^-]\\
P = PV[\pi p^+ + (1-\pi)p^-]
$$
e.g

![image-20201004001752224](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004001752224.png)











Solution:
$$
\Delta = \frac{C^+ - C^-}{S^+ - S^- } = \frac{35 - 0 }{135 - 74} \approx 0.574
$$
Then we have c as 
$$
c = \Delta S + PV(-\Delta S^+ + C^+) = 16.9975
$$
Another solution:
$$
\pi = \frac{1+r - d}{u - d} = \frac{1.0515 - 0.74}{1.35 - 0.74} = 0.510656\\
c = \frac{\pi c^+ + (1-\pi)c^-}{1+r} = 16.9975
$$


### Put-Call Parity

$$
S + p = PV(X) + c
$$

### American Style Options

American calls can be exercise eariler. But an early exercise results in loss of time value. Therefore it would be better to sell than exercise. 

American puts can be exercise earlier. Early exercise results in a premium over European Style options. 

e.g

$S_0 = 26, X = 25, u = 1.466, d = 0.656, r = 2.05\%$

![image-20201004011134116](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004011134116.png)

Solution:

First, we have $\pi$
$$
\pi= \frac{1.0205 - 0.656}{1.466 - 0.656} = 0.45
$$
Then we have $p^-$
$$
p^ - = \frac{\pi p^{+-} + (1-\pi)p^{--}}{1+r} = 7.4436
$$
**But American options can exercised eariler, we can simply exercise and get 25 - 17.056 = 7.944 > 7.4436 **

So $p^- = 7.944$

### Adjust for stock dividends

![image-20201004100309199](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004100309199.png)

**Instead of justy using Su, use (S-PV(Div))u as up price. **

But because american style call can be exercised before ex-div. So the american call value is 
$$
C_{\text{American}} = max(0, S_t - X)
$$

### BSM Assumptions

* Percentage changes in stock prices in a short period of time are approximately normally distributed. 
* Changes in successive time periods are independent

Therefore, we have 
$$
ln(S_t)\sim N(ln(S_0)+[\mu-\frac{\sigma^2}{2}]T,\sigma \sqrt{T})
$$

* No transaction costs
* No arbitrage opportunities 
* Trading is continuous 
* Borrowing / Lending at risk free rate and it's constant. 
* European Options
* Constant and known volatility of the underlying 
* Liquid underlying divisible 
* Short selling with full use of proceeds. 
* Geometric Brown Movement describes prices movements : continous and smooth

#### Interpretation of the model 

$$
c = SN(d_1) - e^{-rT}XN(d_2)\\
p =  e^{-rT}XN(-d_2)-SN(-d_1)
$$

The $N(d_2)$ captures the probability that the call can be finished in the money. 
$$
d_1  = \frac{ln(\frac{S}{X})+(r+\frac{\sigma^2}{2})T}{\sigma \sqrt{T}}\\
d_2 = d_1 - \sigma \sqrt{T}
$$


#### Modification for carry benefit 

$$
d_1  = \frac{ln(\frac{S}{X})+(r-\gamma+\frac{\sigma^2}{2})T}{\sigma \sqrt{T}}\\
d_2 = d_1 - \sigma \sqrt{T}
$$

Where $\gamma$  is the benefit of carrying. 

The stock part of the call and put price would then changes. 
$$
c = Se^{-\gamma T}N(d_1) - e^{-rT}XN(d_2)\\
p =  e^{-rT}XN(-d_2)-Se^{-\gamma T}N(-d_1)
$$

### Black Model (Options on Futures)

$$
C = [F_0(T)\cdot N(d_1) - X \cdot N(d_2)]e^{-rT}\\
P = [-F_0(T)\cdot N(-d_1) + X \cdot N(-d_2)]e^{-rT}
$$

Call and put are the present value of expected payoff. 

#### Black model on interest rate

![image-20201004172632431](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004172632431.png)
$$
C = AP[FRA_{T_1,T_2} \cdot N(d_1) - X_R \cdot N(d_2)]e^{-rT_2}\\
P = AP[X_R \cdot N(-d_2)-FRA_{T_1,T_2} \cdot N(-d_1) ]e^{-rT_2}\\
d_1 = \frac{ln(\frac{FRA_{T_1,T_2}}{X_R}) - \frac{\sigma^2 }{2}T_1}{\sigma \sqrt{T_1}}\\
d_2 = d_1 - \sigma\sqrt{T_1}
$$
**If we long call and short put, we created a received floating pay fixed swap.**

#### Cap & Floors

cap example:

![image-20201004173810736](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201004173810736.png)





**Long floor short cap  ** $\Rarr$  **(Long floor)Received  Fixed (Short Cap)Pay Floating  Swap**

If $X_R = \text{Swap rate}$ then $V_{Cap} = V_{Floor}, cost=0$

#### Swaptions

Option on a swap. Holder have the right to enter a swap at a pre-agreed swap rate. 

Payer Swaptions: Pay fixed, get floating

Receiver Swaptions: Get fixed, pay floating. 

Consider a new discount factor: 
$$
PV_A = \sum_{j=1}^{n} (r_{fixed} - X_R)\cdot NA
$$
Then we have 
$$
Pay_{swp} = [R_{fix}\cdot N(d_1) - X_R N(d_2)]\cdot PV_A\\
Rec_{swp} = [X_R N(-d_2)-R_{fix}\cdot N(-d_1) ]\cdot PV_A\\
d_1 = \frac{ln(\frac{R_{fix}}{X_R})+\frac{\sigma^2}{2}T}{\sigma \sqrt{T}}\\
d_2 = d_1 - \sigma\sqrt{T}
$$


### Greeks 

#### Delta 

$$
\Delta_C = e^{-\delta T}N(d_1)\\
\Delta_P = e^{-\delta T}N(-d_1)
$$

For a given X
$$
\Delta_C + \Delta_P = 1
$$
**For small changes, delta is good. For larger changes, delta loses accuracy. **

Being delta neutral implies 
$$
\Delta_{Portfolio} + N_H \Delta_H = 0
$$

> Example 
>
> S = 100
>
> X = 100
>
> r = 5% 
>
> T = 1
>
> $\sigma = 30\%$
>
> $\delta = 5\%$
>
> Position: Short puts on 10000 shares. 
> $$
> \Delta_C = 0.532\\
> \Delta_P = -0.419
> $$
> Our position delta is 
> $$
> - (-0.419)*10000 = 4190
> $$
> Therefore, we can short 4190 shares to be delta neutral. 
>
> Or we can  $\frac{-4190}{0.532} = -7876$ , means that we can short 7876 calls to be delta neutral.



#### Gamma

The change in an option's delta for a change in $S_0$ 

Also, $\Gamma_c = \Gamma_p$

e.g

> $$
> S_0 = 50\\
> X = 50\\
> \Delta = 0.5\\
> \Gamma = 0.03
> $$
>
> So when $S_t = 51$, 
>
> The call px goes up by $\Delta = 0.5$
>
> But as $S_t = 52$, c = 0.53

#### Theta

A change in px of call and put for a change in time to expiration. 

**Long options have negative theta: time is your enemy.**

**Short options have positive theta: time is your friend.**

Theta cannot be adjusted by positions in the underlying. 

Theta is the rate of option decay. 

#### Vega

Change in call and put for a change in volatility. 

**Vega is based on future volatility.**

#### Rho

A change in call and put for a change in the risk-free rate. 

**Calls have positive rho.**

**Puts have negative rho.**

### Implied Volatility

* Volatility can be estimated from historical data. 
* Volatility can be inferred from prices. 
* Options can be quoted by implied volatility. 



# Financial Reporting And Analysis

## Analysis of Financial Institutions

### Systemic Importance 

Their smooth functioning is essential to the overall health of an economy.  

Systemic risk: A risk of disruption to the financial services that is caused by 

* An impairment of all or parts of the financial system. 
* Has the potential to have serious negative consequences for the economy as a whole. 

### The nature of the liabilities and assets

Liabilities of most banks are made up primarily of deposits. And failure to honor its deposits could have negative consequences. 

Fiancial assets creat direct exposure to risks: interest rate risks, credit risks, market risks, liqudity risks. 

**The goal of regulation is to minimize systemic risk.**

### BASEL III 

#### Minimum Capital requirements

The minimum percentage of risk-weighted assets that a bank must fund with equity capital.

#### Minimum liquidity

A bank must hold enough high-quality assets to cover its liquidity needs in a 30-day liquidity stress scenario. 

#### Stable funding

Minimum amount of stable funding relative to the liquidity needs over a one-year horizon.

### CAMELS

#### Capital Adequacy

Capital Adequacy: defined in terms of the proportion of the banks assets funded with capital. **Assets are adjusted based on their risk. Riskier assets require a higher weighting. ** For example: Cash 0%, Corporate Loans: 100% , Non-Performing Loans> 100%

**Common Equity  Tier 1 Capital must be at least 4.5% of risk-weighted assets. **

**Total Tier 1 equity must be at least 6% of risk-weighted assets.**

Tier 2 capital: capital instruments that are subordinate to depositors and to general creditors and original minimum maturity of five years. 

**Total capital must be at least 8% of risk-weighted assets.**

#### Asset Quality

Asset Quality: Capital are classified into hierarchical tiers. Pretains to the amount of credit risk associateed with the assets. 

Loans, Investment in securities

#### Management Capabilities

Identifying profit opportunities while managing risk. 

Strong goverance structure, sound internal controls, and financial reporting quality. 

#### Earnings 

High quality and trending upward. 

**Estimate of fair value: similiar or identical instruments in active markets, if not obersevable then use a model to estimate FV.**

#### Liquidity Position

There are two minimum liquidity standards from BASEL 3:

* Liquidity Coverage Ratio (LCR): Highly liquid assets / One Month Liquidity Needs in A stress Scenario > 100%
* Net Stable funding ratio: The minimum % of a banks required stable funding that must sourced from, avaliable / required > 100%

( avaliable is the capital and liabilities multiply by available stable funding factor)

#### Sensitivity

Sensitivity to market risk.

### Other Factors

#### Banking Factors

* Government Support: Too big to fail, systemic important financial institution
* Regional vs National vs Global, $\Rarr$ divwersification vs concentration of loan expressure.
* Coporate culture

#### Non-Banking Factors

* Competitive environment
* Off-balance sheet items
	* Variable interest entities 
	* Pension and Benefit plans
	* Assets under management

### Insurance Companies

**Insurance companies can be categorized as property and casualty (less predictable)  vs  life and health.(More predictable) **

#### Property & Casualty 

Business profile is full of buildings , autos, etc. 

Earnings are cyclical, price sensitive. 

##### Profitability ratios

Combined ratio = underwriting loss ratio + expense ration = total insurance expense / net premiums earned

Underwriting Loss ratio = losses/ net premiums earned

Expense ratio = underwriting expenses / net premiums written

Loss and loss adjustment expense ratio = (loss expense + loss adjustment expense )/ net premium earned

#### Life & Health

for all profitability ratio, add deposits into the denominator. 

## Intercoporate Investments

Intercorporate investments means investments in other companies. 

It can 

* Diversify their asset base
* Enter new market
* Obtain competitive advantage
* achieve additional profitability

Basic coporate investment categories includes 

* Investments in financial assets(no significant influence or control, equity interest < 20%)
* investments in associates: significant nfluence but no control(equity interest<50%)
* Joint ventures: Control is shared by 2 or more entities.
* Business Combinations: equity interest > 50%, have control

### Investments in Financial Assets

* Amortized Cost: The fiancial assets are being held to collect contractual cash flows while cash flows are solely principal interest. **Only debt falls into this category.** 
* Fair Value through profit or loss (FVPL). Applied to all equity and some bonds.
* Fair Value through OCI(**Other Comprehensive Income**).
* **All measured at fair value when initially acquired.**
* **All interest and dividends are recognized as income in profit and loss.**

![image-20201007010130757](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201007010130757.png)

> Summary
>
> Evaluate company performance seperately for operating and investing activities
>
> Analysis of operations should exclued
>
> * Interest Income
> * Dividend Income
> * Gains and losses on investmenst
>
> Exclude non-operating assets

### Associates and Joint Venture

#### Equity Method

Investment initially recorded at the cost of acquired shares. 

**Each subsequent period adjusted for proportionate share of the changes in investee's net assets.**

Proportion of shares of earnings is on Income statement. 

Proportion of shares dividends is only on **balance sheet.**

**Classified as non-current asset.** 

E.g

> ABC purchases 20% interest in XYZ for 480k at Jan 2/13 (48,000 shares @ $10 per share)
>
> For Balance Sheet 
>
> |                         | Debit | Credit |
> | ----------------------- | ----- | ------ |
> | Investment in Associate | 480k  |        |
> | Cash                    |       | 480k   |
>
> XYZ reports NI = 200k for 2013
>
> BS
>
> |                         | Debit          | Credit |
> | ----------------------- | -------------- | ------ |
> | Investment in Associate | 40k = 200k*0.2 |        |
> | Investment Income       |                | 40k    |
>
> IS
>
> | Income Statement        |      |
> | ----------------------- | ---- |
> | Investmen Income (loss) | 40k  |
>
> On Dec 30, Fair value per share is $12. 
>
> NO CHANGES!
>
> Jan 28/14, Cash Dividend $100k
>
> | Balance Sheet            | Debit | Credit |
> | ------------------------ | ----- | ------ |
> | Cash                     | 20k   |        |
> | Investment in Associates |       | 20k    |

![image-20201007012634829](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201007012634829.png)



##### issues

> The acqusition cost $\ne$ Book Value. 
>
> Bought 25% of  Y corp for $8.5 Mio, but the book value of the corporation = \$30 mio 
>
> * First, locate the difference
> * Allocate to specific assets
>
> Assume the dep assets are undervalued by 2.4 mio
>
> 25% of this 2.4 mio is 600k (take 75000 a year from inv in assoc account each year and reduces inv income as well assuming  this asset has 8 years of life.)
>
> Total access is 1 mio, so another 400k goes into good will.(impairment annually)
>
> In 2014, Y Corp reports 
>
> NI = 2.8M
>
> Includes loss on discountiouned Operations for $400k
>
> Dividends declared and paid Dec 31/2014 is $1.4M
>
> Jan 1/14
>
> | Balance Sheet     | Debit | Credit |
> | ----------------- | ----- | ------ |
> | Inv in Associates | $8.5M​ |        |
> | Cash              |       | $8.5M  |
>
> Dec 31/2014
>
> | Balace Sheet              | Debit                               | Credit |
> | ------------------------- | ----------------------------------- | ------ |
> | Investment in associates  | $700k                               |        |
> | Loss from disc operations | $100k                               |        |
> | Investment Income (loss)  |                                     | $800k  |
> | Cash                      | $350k (For div)                     |        |
> | Inv in associates         |                                     | $350k  |
> | Investment income         | $75k (amort of identifiable excess) |        |
> | Inv in associates         |                                     | $75k   |

![image-20201007152011039](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201007152011039.png)

#### Fair Value Method

**For fair value method, IFRS is strongly restricted to VC, MF, and trusts. While GAAP allow all entities.**

Investment reported at fair value:

* Unrealized +/- gains goes into net income
* interest and dividends goes into Net Income
* Excess over Book Value not amortized

#### Impairment 

IFRS and GAAP periodic reviews of equity method investments for impairment

Entire Carrying amount is tested.

If so, written down to recoverable amount. 

#### Transactions with associates

![image-20201007153045564](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201007153045564.png)

**Profits from such transactions cannot be realized until confirmed either through 1) Use 2) A third party sales.**

Otherwised they are all just unrealized profit. Proportionate amount must be taken out of investors income from investment until confirmed. 

E.g

20200101, W acquires 25% of F for $1M. 

Given that 

* BV = \$ 3.8M
* FV = \$3.84 M ( Extra \$40 k for a building of 20-yr life )
* Div = \$3200 
* NI = \$20,000 (Include a \$8000 from an upstream sale of inventory)

Sol:

Our excess is 
$$
1M - 0.25 \times BV = 50k
$$
Given \$40 k is coming from the building, Because we only have 25% of interest, there are $0.25 \times 40k = 10k$ extra from it. 

Therefore. the goodwill is accounted for 
$$
50k - 10k = 40k
$$
Note that the excess from the building which is 10k, is depreciated over 20-year of the buildings life. 

So for each year, there will be a depreciation expense of $\frac{10k}{20} = 500$

Because there is 8000 among that 20000 comes from the upstream sale of inventory. Therefore it is unrealized profit as 0.25 $\times$ 80000 = 

Therefore, at 2021, the investment income would be 
$$
25\% NI = 0.25 \times 20000 = 5000
$$
Amortization expense ( from the building) is 500 and unrealized profit is 2000. The final income would be $5000-500-2000 = 2500$

In the cash flow statement, none of these line items would appear, 2500 will be shown as cash flow from investment activities. 

Another example:![image-20201101105438580](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201101105438580.png)



#### Disclosure

* Classified as non-current assets
* Income Recorded as earned. 
	* Net Income Before Discontiued Operations
	* Discontiuned Operations
	* Other Comprehensive Income

#### Issues For Analysts 

Is the equity method appropriate?

For example: 19% of share but have significant influence vs 25% of shares with no influence

#### Acquisition Method

##### The Identifiable Assets and liabilities 

This includes tangible and intangible assets and liabilities at FV as of date of acquisition. 

Must also recognize assets and liabilities not previously recognized. 

**As for the contingent liabilities, it is a present obligation arising from past events and can be measured reliably.**

Expected costs not included.

##### Financial Assets

Will be reclassified from acquiree to acquirer's business model. 

##### Goodwill

Recognition and measurement of goodwill has **partial** and **full**

while GAAP only allows full and IFRS allows partial and full

Example:

>  800k for 80% of a target,  and the FV of the net assets = 900k

This implies the FV of the entity is 1M

Partial:

 Given the FV of the acquisition is 800k. 80% of the $FV_{net\ assets} = 80\% 900k = 720k$

Therefore, the goodwill we can recognized is 800k-720k = 80k.

Full:

Given the FV of the entity is 1M, and the fair value of the net assets is 900k, the goodwill need to be recognized is 100k for **full**

*If acquisition price < FV, which is called a bargain acquisition*

The FV of net assets less acquisition = gain on the income statement. 

**Example: Goodwill impairment(IFRS)**

Cash-generating unit

Carrying Value = 1.4M includes 300k goodwill 

![image-20201220204025902](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201220204025902.png)

**GAAP**

![image-20201220204629575](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20201220204629575.png)

## Employee Compensation: Post-Employment And Share Based

### Defined Contribution

A specific, agreed upon, contributions are made to an employee's pension plan. 

Employer's contributions arte defined, employee's benefit's are not. 

Employer's Contribution = Pension expense. No Further obligation. 

Generally in the period in which the employee provides service. 

Amounts paid usually attributed to specific individuals. 

### Defined Benefit 

Specifies the benefit the employee receives. 

Employer's contribution is not fixed. 

Creates a future obligation based on current service. 

The entitlement to the benefits increase with the length of the employee. 

**The difference between defined contribution and defined benefit is that :**

* DB : Employer is the beneficiary. 
* DC: Employee is the beneficiary. 

If the plan assets > current obligtion, the plan is overfunded. May be possible for the employer to recapture by reduced future funding or reversion of funds. 

The expense to be recognized each period is not the same as the employer's cash funding contribution 

**Rely on actuaries to determine level of obligation funding each period. **

Use of acturial assumptions: Motality rates, employee turnover, interest rates, earning rates, etc. 

### Other Post employment Benefits

Health, life insurance premiums. Typically classified as DB plans. 

Example:

**Pension Obligation**  is the PV of future benefits earned by employee's for service provided to date.  

#### One-Person Plan Example

**The pension obligation** is the present value of the future benefits earned by employee's for service provided to date. 

The assumption is that 

![image-20210118230229533](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210118230229533.png)

**Actuarial gains and losses: ** Result from 

* change in assumptions
* an experience gain/loss.

#### Component Cost

The Defined Contribution: Reported as expense on IS, no BS effect.  It is folded in the cost of good sold. 

Defined Benefit: On the balance sheet.

Take the end of period **pension obligation** and subtract FV(plan assets) is the fund satus. 

If PO > FV, we have the net pension liability. 

If PO < FV, we have net pension asset. **It is subject to a ceiling. (no need to understand)**

##### Periodic Pension Cost

* Service Costs: Current and past. Include retroactive benefits pr returoactive curtailments. Recognized in P/L
* Net Interest Income/Expense: Net Pension liability / Assets * discount rate.
* Remeasurement: actuarial gains/losses, difference between actual return on plan assets and expected return. **Recognized in OCI.**

**For GAAP, we use amortized some of these OCI to P/L over average service lives of affected employees. **

![image-20210221221618235](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210221221618235.png)



#### Actuarial Assumptions

An increase\decrease in Pension Obligation from a change in assumptions: actuarial gains\losses

When pension obligation changes, interest expense changes. ![image-20210222234906852](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210222234906852.png)

The assumptions built in:

* Employee turnover
* life expectancy
* future inflation
* interest rates
* future compensation levels
* rate of increase in compensation. 
* long term equity growth rate

#### Disclosures

Comparability can be affected by 

* Differences in key assumputions 
* Periodic pension costs recognized in P/L may not be comparable 
* Reporting differences between GAAP/IFRS IFRS requires immediate recognition vs GAAP allows defer & amortize
* Reporting differences between GAAP/IFRS: affects where on statements specific line items appear.
* Cash flow reporting differences: IFRS sees as financing/operating activities while GAAP sees as operating activities

##### Assumptions

Assumptions are disclosed: discount rates, expected compensation, increases, medical exp, inflation, expected return on asssets for GAAP.

**Other post-employment benefits: increase in health care costs, future inflation rate, is known as the ultimate health care trend rate.**

##### Net Pension Liability/Assets 

 IFRS and GAAP requires the amount on Balance sheet is net. 

The plan is not consolidated since the plan is a separate legal entity. 

##### Total Periodic Pension Costs

Net pension liability/asset before considering employer contributions. 

Periodic pension costy = ending funded status - employer contribution - beginning funded status

##### Costs recognized in P/L vs OCI.

![image-20210227213856541](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210227213856541.png)

##### Classification 

Pension expense generally treated as operating expenses. 

Interest expense/income may be better treated as non-operating expenses. 

##### Cash Flow Disclosures

Cash flow impact: employer's contribution to the fund. 

If contributions to a plan in a given year are in excess of current pension expenses. 

##### Share-based compensation

Main issues: recognition and measurement. 

Problem is that Stock Options issued by the company are not traded on exchanges. 

**Equity stock option plan are charged in equity accounts. **

**Compensation rewarsds depend on future events are chared to operating income on IS.**

## Multinational Operations

### Currency Termininology

Records are kept in host country currency. (**Local Currency**)

Parent company based in US, has to presented in USD (**Functional Currency**)

**The presentation currency: The currency of financial statement**

**The Funtional Currency: the currency of the primary economic environment**

**The Local Currency:Currency where the company operates.**

### Currency Transactions

By Definition, **a foreign currency is any currency other than a company's functional currency**

If  everyting was settled on the day transation happend, there will be no issue.

But sometimes there are transactions that leads to asset/liability in a duration. 

The accounting method:

![image-20210228224425063](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210228224425063.png)

**Any currency translation, unrealized gain/loss goes to the income statement. Belongs to the the non-operating income/expense.**

The gross profit margin and net income should not be affected.

**Since standards specify no placement on the IS, companies can choose.**

Unrealized gains/losses are included in NI on BS date. 

IFRS requires disclosure of the "amount of exchange differences recognized in P/L." Neither requires disclosure of the line item in which gains/losses are located.  

**If immaterial, not disclosed.**

* Limited transactions. 
* Forex pegged/fixed/stable 
* offsetting transactions.
* Hedging practice using forwards/options. 

When consildate a foreign children's report, **what is the appropriate exchange rate with respect to each FS account? How should the translate adjustment be reflected in the consolidated FS?**

There are two approaches for translation. 

* All A/L are translated at spot rates.  (The current method)
* Only monetary rates are translate at spot rate, while non-monetary A/L translated @ historical rates (The monetary method). (The rate at the time of purchasing.)

Then there will be difference between last report date and current because of difference of spot rates: **Net Foreign currency translatiuon gain/loss.**

**Translate adjustment on balance sheet is cumulative.**

Which method is appropriate?

Depends on the foreigh entity's functional currency.

If the the subsidary is same as parent, use the temporal method( monetary method.)

Otherwise use current method. 

**The key to determine the functional currency:**

* The currency that mainly influences sales prices for g/s. 
* The currency of the country whose competitive forces and regulations mainly determine the salse price of its g/s. 

##### Hyperinflation

If the entity is in a highly inflationary environment, functional currency is not very relevant.

IFRS: Foreign entity's first restated for changes in the local general price level and then translated at current rates.

GAAP: Must use temporal method. 

**Hyperinflation: $(1+i)^3 - 1 > 1, i \approx 26\%$**

For GAAP: just use temporal method.

For IFRS,

On balance sheet: monetary asset/liability are not restated for inflation. Exposed to +/- in P.P. 

Non-monetrary A/L restated for inflation. Restated from the date of balance sheet valuation or from revaluation date.

Equity accounts: all components restated for inflation from the begining of the period. 

As for the income statement, all IS items restated by applying $\Delta CPI$ from dates when the item was originally recorded on BS.

##### Effective Tax rate

If home tax rate > foreign tax rate, 

incremental tax rate = home rate - foreign rate. 

##### Financial Results

Parent may have subs using temporal method and others using current rate. 

**Current rate method disclosed translation adjustment** 

## Quality Framework

![image-20210320191137199](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210320191137199.png)

The motivation is typically to bias NI. 

New Management may be aggressive to bias NI.

Mergeres and Acqusitions dilute CFO problems conceal past accounting misstatements. 

Stock deals acquirer may manage earnings up prior to the acquisition to raish share price. 

Target may do the same, get a more favourable price. 

Maximize Goodwill understate value of amortizable intangibles.

Potential problems also includes 

revisions to estimates ( useful lives)

sudden increase to allowances/reserves (past NI overstated)

Large accruals for losses.

Unrecognized / unreported A/L

### General steps 

1. Understand the company / industry
2. Management 
3. Significant accounting areas
4. Make comparisons. ( YOY, Major differences, Acct. Policies, Ratios)
5. Warning Signs: Declining AR turnover, Days inventory building, NI > CFO

#### Beneish model

Attempts to capture the probability of manipulatuion. 

M-Score ~ N(0,1) , Cut-off z score is -1.78. If larger than that, there will be probability of manipulation. 

### Sustainable Earnings

Sustainabnle: ROIC > WACC
$$
E_{t+1} = \alpha + \beta_1 E_t +\epsilon
$$
Higher Beta, Stronger persistence. 

For the accrualed measurement,
$$
E_{t+1} = \alpha + \beta_1 CF + \beta_2 Accruals + \epsilon
$$
Earnings with a higher accruals component would be less persistent. 

Can Further breaking down the accruals components. 

Accruals can be classified as normal transactions and discretionary accruals. 
$$
Acc = \alpha + \beta_1 \text{Growth in credit sales} + \beta_2 (Depreciation) + \epsilon
$$
Looking for outliers in the error terms. 

### Earnings Mean Reversion

Extreme levels of earnings, high & low, tend to revert to normal levels. 

Low: Shut down operations, change management

High: Attracts competition.

Cannot extrapolate L/H earnings into the future, must normalize. 

**The higher the accruals component, the faster the mean reversion may be .**

### Revenue Recognition

Fully understand revenue recognition policies: Shipping terms, rights of return, rebates, multiple deliverables. 

Receivables do not improve with age. 

Cash Vs Accrual" AR/Sales over time. 

Pay attention to nonfinancial data. 

revenue trends: Kinds of revenue recognized, growth in revenue vs growth in AR. 

### Bankruptcy Prediction Models

Attempt to quantify the likelihood that a company will default on its debt/ declare bankruptcy.

![image-20210322202008170](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210322202008170.png)

### Cash Flow Quality

#### Indicators of Cash Flow quality

* Positive Operating Cash Flow
* OCF from sustainable sources. 
* OCF > (CAPEX+ Div + Debt Repayment)

But it depends on life cycle statge and industry. 

Operating Cash flow is less easily manipulated than Operating Income/ Net Income. 

But Can still be 

* Selling AR
* Delaying AP
* Shift CFF/CFI to CFO.

But They would leave BS footprints. 

### Balance Sheet Quality

#### Results Quality

* Optimal Amount of leverage
* adequate liquidity
* economically successful asset allocation
* ratio analysis
* common size statements

#### Reporting Quality

1. Completeness: Relevant items on balance sheet, off-balance sheet items may understate leverage, unconsolidated joint venture or equity method investees(Parent reports share of NI but not shares of sales: profitability ratios overstated)
2. Unbiased measurement: particularly when subjective valuation is involved.
3. Clear presentation: Seperate vs aggregate line items

### Risk Disclosures

* Auditor 
* Notes to Financial Statement
* MD&A 
	* Nature of Business
	* Objectives and strategies
	* Resources, risks and relationships
	* Results and prospects
	* Performance measures and indicators

## Financial Statement Analysis

![image-20210324201804083](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20210324201804083.png)

# Equity Valuation

## Valuation and Intrinsic Value

The goal of valuation is to identify mispriced securities/assets.

Equity valuation based on the following asssumptions:

* The undertaking valuation efforts assumes mispricing exists. ($P \ne V$)
* Price and value will converge
* Going Concern Value: a company will continue business activities. 
* Liquidation Value: Immediate vs Orderly liquidation value. (Immediate vs Orderly Liquidation Value)

###  Value 

#### Intrinsic Value

Typically the relavant concept of value for valuing public equities.

#### Fair Market Value

Value at which an asset/liability would change hands between a willing buyer/seller when they are not under any compulsion to buy/sell.

#### Investment Value

An asset may be worth more to a particular buyer.

## Industry/ Competitive Analysis

### Valuation Process

* Understanding the business
* Forecasting Company Performance
* Selecting The appriate valution Model
* Convertiung forecasts to a valuation 
* Applying the valuation conclusions.

### Absolute vs Relative 

An absolute valuation model specifies an assets intrinsic value

Cash Flows have two levels: Shareholder level (Dividends) and Company Level( Free Cash Flow, Residual Income)

While a relative valuation models (methods of comparables)

Estimate of value relative to another 

Law of one price: similar assets should sell for similar prices. 

Price multiples or enterprises multiples. 

> Conglomerate Discount
>
> Market Typicaklly applies a discount to the stock of a company operating in multople unrelated businesses. 
>
> Explanations: Inefficiency in capital allocation
>
> Capital allocation Accross segements may not maximize shareholder value. 
>
> Poorly Performing companies tend to expand by diversifying the earnings base. 



## Return Concept

The Holding Period Return

$$
R_H = \frac{D_H+P_H}{P_0} -1
$$
The realized Holding Period Return is history, while the expected holding periode return is forward looking. 

Required Return is the minimum level of expeced return for a specified time period given an assets risk. 

**The discount Rate** can be subjectively modified. IRR is the discount rate such taht $P_0 = PV(CF_i)$ 

Example:

> Given: $P_0 = 127.97, r = 6.3\%, V_0 = 176.3$  where $r = r_f \beta \cdot ERP$
>
> Find $E(R_\tau)$ if expected Convergence:($\tau$) where $\tau$ is the time of convergence. 
>
> If $\tau = 1yr$, We have 
> $$
> E(r_\tau) = r_\tau + \frac{V_0-P_0}{P_0} =6.3 + \frac{176.3 - 127.97}{127.97} = 6.3 + 37.77 = 44.07\%
> $$
>   If $\tau = 9mo$, we have 
> $$
> [1.063^0.75 - 1] + 37.77\% = 42.66\%
> $$
> Portential Risk:
>
> * No mispricing exists
> * No convergence over holding period



Example:

> Given :
>
> $P_0 = 33.31, D = 0.96, r = 7\%$ and one year price target is 37.5. 
>
> What is the $E(\alpha)$?
>
> Solution:
> $$
> E(\alpha) = E(R_\tau) - r_{\tau} \\
>  = \frac{37.5 - 33.31 + 0.96}{33.31} - 0.07
> $$



### Equity Risk Premium

The incremental return required for holding equities over a risk-free asset depends strictly on expectations for the future. 

The  purpose of estimating equity risk premium is to estimate an input to a model to estimate r. 
$$
ERP = \frac{\sum_{i = 1}^{N}{(R_{M_i} - r_{f_i})}}{N}
$$

* Typically Estimated for a national equity market.
* Broad Based, market value weighted indexes. 
* Assumed Stationarity, constant parameters over time and into the future. Usually a longer time period would help stationarity. 
* Can use arithmetic or geometric. But preferred geometric.
* Use T-bill (90 days monemarket rate) or T-Bond (long term bond) as proxy for risk-free rate.

The geometric mean appears to be appropriate in a multi-period context. (Even when using a single-period context), even when using a single period required return model.  **Therefore, geometric mean is preferred in estimating equity risk premium.**

A longer time period can increase the precision of estimated ERP, but the assumption of stationarity becomes less viable. 

> Adjusted Historical Estimates
>
> Historical ERP may be adjested to neutralize the effects of bias in market return series.
>
> Survivorship bias: Inflates historical estimates of ERP
>
> Event History: A string of positive events not balanced out by negative events and which are not likely to reocur. 

#### Foward Looking Estimates

##### Gordon Growth Model Estimates 

$$
ERP(GGM) = \frac{D_t}{P_0} + g - r_f
$$

Where the $D_t$ is the year ahead aggregate forecasted dividends,  where $P_0$ is the current index price.

$g$ is the consensus long-term earnings growth rate. While $r_f$ is the current Longterm goverment bond yield.

###### If the assumption of a stable g does not hold, use a 2 or 3 stage GGM 

$$
ERP  = IRR - r_f
$$

To solve this, we have 
$$
P_0 = PV_{fast} (r) + PV_{transition}(r) + PV_{growth}(r)
$$
To get r.

**The GGM assumes a constant dividend pay out ratio and efficient markets. **

##### Macroeconomic Model Estimates

For example 
$$
\{[1+E(I)][1+E(g_{EPS})][1+E(g_{P/E})]-1 + E(inc)\} -E(r_f)
$$
While the expected inflation $E(I)$ is the 
$$
\frac{1+ YTM(20-yr \ T-bond)}{1+ YTM( \ YTM 20-yr\ TIPS)} - 1
$$
The expected growth rate of Earnings Per share, we should track the real GDP growth.

Then we have the expected growth rate of $P/E$

with Baseline as 0. 

If index is overvalued, then $E(g_{P/E}) < 0$ , otherwise vice versa. 

### Beta Estimation

Typically OLS regression, unadjusted raw beta. 

Since the betas tend to be mean reverting  and because valuation is forward looking, raw beta is adjusted. 

#### Blume adjustment

$$
\text{Adjusted Beta } = \frac{2}{3} \text{Raw Beta} + \frac{1}{3}
$$

Because the **beta of the market is 1.**

### Required Return 

#### CAPM

CAPM assumes 

* Investors are risk averse
* Investment decisions are based on mean return and variance of returns of their total portfolio

#### Multi Factor Models

$R_{MRF} = R_m - R_f$ Return on market over the one-month T-Bill rate. 

$SMB$ the averagte R on 3 small-cap portfolios minus average R on 3 large-cap portfolios

$HML$ is the average R on 2 high book-to-market portfolios minus the average R on 2 low book-to-market portfolios

> Pastor-Stambaugh Model
>
> In addition to the fama-french three factor model, it creates another factor: liquidity

### WACC

$$
WACC = \frac{MVD}{MVD+MVCE}E(YTM)(1-t) + \frac{MVCE}{MVD+MVCE}E(R_e )
$$

R(e) can be capm, multifactor model, etc.

## Industry Analysis

### Top Down / Bottom Up

#### Revenue

##### Segment Disclosures

IFRS/GAAP: Separate financial info must be provided for any segment whose revenue/ operating income and assets is larger than 10% of The combined company's revenue. operating income, and assets. 

The most common ways to divide segements

* Geogrphy
* Business segment
* Product Lines

（Product lines are smaller than Business segement)

Top Down: Economy: Sector: Industry: Market: Company

Bottom Up: Product Lines: Segements/Locations: Company

### Economies of Scale

#### Cost Analysis

Fixed Costs more directly tied to CAPEX and to total capacity. 

Determination of Economies of scale including gross margins and operating margins. 

**Gross margins captures scale economies with suppliers.**

**Operating margins capture scale economies of operators.**

### Forecasting Costs

#### COGS

COGS is the largest cost item for merchandising and manufacturing companies. 

**For companies has a long history, the historical relationship provide a good starting point.**

Cost drivers:

* Size 
* Competitive forces constrain margins. 
* Strategy choice: Cost/differentiation /focus
* Fluctuating input costs. Passtru vs Hedge

**Hedging information usually found in the footnotes. **

Can also compare with competitors: isolate diffeerences with the key drivers. Size / operations. business model, execution.

#### SG&A 

SG&A are less directly tied to revenue. 

Often broken out based on whether fixed or variable costs.

For example: Selling expense are more variable and can be estimated using % of revenue, general and administration and R&D are more fixed. 

#### Non-Operating Costs

Financing Expenses = maturity structure + interest rates found in the notes.

#### Coporate Income Tax

Statutory Tax Rate: Tax Rate applicable to company's domestic tax base. 

After adjusted for tax credits, non-deductible expenses, Div withholdings, adjustments to previous years

we then have effective tax rate. 

And the **effective tax rate ** are used to forecast tax expense. 	

After adjusted for **deferred tax assets and deferred tax liabilities, we would then have the Cash Tax Rate used to forecast Cash Flows.**

## Balance Sheet modeling

### Working Capital Account

Efficiency Ratios: 

* Inventory Turnover
* Days of Inventory on Hand
* Receivables Turnover
* Days Sales Outstanding
* Days of Payables outstanding 
* Working Capital Turnover

### Non Current Assets

Less directly tied to income statement. Net PPE primarily driven by CAPEX and depreciation. Based on historical depreciation  schedules. 

### Capital Structure

Leverage ratio:

* Debt to Capital
* Debt to Equity
* Debt to EBITDA

to see how they deviating from the current capital structure.

#### Scenario Analysis

Change multipe assumtions at a time to see the on intrinsic value.

#### Sensitivity Analysis

Change one assumption at a time to see the effect on intrinsic value.

### ROIC (return on invested capital)

$$
\text{ROIC} = \frac{\text{Net Operating Profit Less adjusted taxes}}{\text{Operating Assets - Operating Liabilities}}
$$

#### ROCE (Return on Capital Employed)

$$
ROCE = \frac{\text{NOP}}{\text{Emp. Cap}} = \frac{\text{Earnings before Interest and Tax}}{\text{Debt Equity}}
$$

### Forces-Prices-Costs

#### Downward Price Pressure

* Low entry barriers
* Substitutes
* Buyer Power
* Intense Rivalry

#### Upward Pressure

* Higher Quality of Service
* Supplier Power
* Rivarly

Current Industry Structure is in current margins.

Future margins will be affected by future structural pressures on prices and costs.

### Inflation / Deflation

**Companies with pricing power can pass on inflation, others can't.**

####  Effect  on Cost Projection

* Cost Drivers
* Hedging
* Competitive Environment

### Technological Change

Technology usually leads to a lowering of costs. 

Prices depends on the nature of the technology. 

* Proprietary: Sustainable cost advantage. Leads to a higher operating margins. 
* Non-proprietary: short-run cost advantage to early adopters.

#### Impacts on costs of lower volumes

**Requires Estimate of variable vs fixed costs**
$$
\%\text{Variable Costs} = \frac{\%\Delta\text{Cost of Revenue + Operating Expenses}}{\% \Delta\text{ Revenue}}
$$

> Cannibalization
>
> The new ipad will substitute part of the old ipad user.

### Forecast Horizon

Choice of horizon influenced by

* Investment Strategy: Forecast horizon should match the average holding period
* Cyclicality: Forecast periood should be long enough for the business to reach an expected mid-cycle level of sales/profitability.

> **Mid-cycle:** Typically longest phase of the business cycle 
>
> Positive but more moderate rate of growth than during early cycle phase 

* Company-specific factors: acquisitions, restructuring, forecast horizon should allow for digestion. 
* Analysts employers preference: Longer-term forecasts provide a better representation of the normalized earnings, potential of the businese/

> **Normalized Earnings**: Expected mid-cycle earnings for a company in thge absence of unusual/temporary factors that mnight impact profit.

> **Inflection Points**: Future departs from the recent past. Technological changhe regulation. 



## Cash Flow Types

There are 4 steps in applying DCF analysis

1. Select a definition of cash flow
2. Forecast those cash flows
3. Choose a discount rate methodology
4. Estimate the discount rate

We can use **dividends, residual income and free cash flow for "Cash flow"**

### Use dividends as cash flows

* Less Volatile Than Earnings
* Less sensitive to short-term fluctutions
* Reflects long-term intrinsic value.
* Companies usually reluctant to reduce dividends

**DDM can be applied to non-div paying companies as well with key assumptions:**

* Company is dividend paying
* Established dividend policy that bears an understandable and consistent relationship to the company's profitablity
* the invstor takes a non-control perspective.

### Use Free Cash Flow

Assumptions:

* Company is non-div paying
* Company is div paying but div is significantly exceed or fall short of  Free-Cash Flow
* Company's FCF aligns withe the company's profitablity within the forecast horizon
* The investor takes a control perspective

### Use Residual Income 

Suitable when 

* Company is not paying dividends
* Expected FCFs are negative within the forecast horizon

### Discount Dividend Model

#### Single Period Model 

$$
V_0 = \frac{D_1}{1+r} + \frac{P_1}{1+r}
$$

#### Multiple Period Model 

$$
V_0 = \sum_{t=1}^n \frac{D_t}{(1+r)^t} + \frac{P_n}{(1+r)^n}
$$

#### Gordon Growth Model

**Assumes dividends grow indefinitely at a constant rate.**
$$
V_0 = \frac{D_0 (1+g)}{(r-g)} = \frac{D_1}{r-g}
$$
r should be much larger than g.

> Example
>
> $D_0 = 0.74, g = 3.8\%. \beta_{raw} = 0.7, \beta_{adj} = 0.8, r_d = 5.6\% r_e = 7\%, P_0=20.50, RP = 2.5\%$
>
> 1. Find $V_0$:
> 	$$
> 	V_0 = \frac{D_1}{r-g} =\frac{D_0(1+g)}{r_e - g} =  \frac{0.74(1.035)}{0.07 - 0.035}
> 	$$
>
> 2. Under/Over Valued
>
> 	$\frac{21.88 - 20.5}{20.5} = 6.77\%$  It is 6.77% lower than valuation. (Undervaluing)
>
> 3. Calculate R using CAPM or BYRP
>
> 	With $r_f = 3\%, ER = 4.5\%$. 
>
> 	Using CAPM we have: $R = 0.03 + 0.80(0.045) = 6.6\%$ If we use 6.6% as return on equity, we then have a valuation of 24.71.
>
> 	Using BYRP we have:  $R = r_d + rp = 0.056 +  0.025$

##### Implied Growth Rate 

We have $V_0$ to solve g. 

#### Present Value of Growth Opportunity (PVGO)

Assume a company has a 100% dividend pay out ratio. Assume D = 4 and r = 10%

Let $g = 0$ Then we have $V = \frac{D_1}{r}$

Now assume a company can earn 15% on its own reinvested earnings. 

Reduce the OPR to 50% or 2, g = 15%*50% = 7.5% V = 80. 
$$
P = \frac{E_1}{r} + PVGO
$$
The $E/r $ is the value of a company without earnings reinvestment. 





















