# CFA Level Two Notes

*Kaiyi Li*

*NYU Shanghai Class of 2019*

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
	- [ ] Course Notes
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
	- [ ] Course Notes
	- [ ] Quiz
	- [ ] Practice Problems

- [ ] **Financial Report Analysis** 
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

![image-20200108172146280](/Users/likaiyi/Documents/CFA_Level2//image-20200108172146280.png)

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

![image-20200209163022669](/Users/likaiyi/Documents/CFA_Level2//image-20200209163022669.png)

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

On an uncovered (unhedged) foreign currency investment should equal the return on a comparable dpmestic currency investment. 

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
>

If all international parity conditions held:

$\%\Delta S_{f/d}^e = \text{forward premium/discount} = i_f - i_d = \pi_f -\pi_e$

![image-20200225110452012](/Users/likaiyi/Documents/CFA_Level2/CFA_Level_II_MDnotes//image-20200225110452012.png)

If all conditions held, it would be impossible for a global investor to earn consistent profits on currency movements. 


























