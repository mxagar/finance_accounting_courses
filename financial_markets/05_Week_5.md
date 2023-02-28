# Financial Markets

Coursera, Yale.
Prof. Robert Shiller.

## Lesson 12: Futures

### Student Loans
- Student loans work as regular loans nowadays, but they could have an equity model: students pay back depending on their salary after the graduation
- Is there a student loan bubble?
    - Shiller thinks that studies have become like a kind of aristocracy or classes in the US and probably somewhere else
    - So young people thinks they need to study and connect to important people; that drives prices up
    - Even state universities are getting expensive because they are not subsidized
    - It might be a bubble

### Forwards and Futures Markets
- Not that many people use them, people even misstrust them
- They are a particular type of derivatives
- The usual market is the the spot market: you deal with the object immediately
    - The prices in it are called spot prices
- In forward and futures markets, we have contracts for future prices and deliveries in the future
- However, these markets have a function!
    - Grain traders, for instance, trade in those markets
    - Grains need to be stored
    - Grain trading is the origin of forward and futures markets
- Which assets end up in future markets?
    - It's difficult to answer that -- it's a trial and error
    - How do we know that a party will be great? It's similar
    - Shiller started a home prices futures market, it is running, but it's not been a success as expected

### Forward Contracts
- Two individuals make a contract to deliver in a certain date at a price: maturity date
    - Example: rice farmer sells grain to a warehouse
- Both sides are locked to the contract: they have no liquidity
    - What if the farmer gets drunk and doesn't produce grain?
    - For that reason, we have futures markets: the risk of not knowing the farmer vanishes
- Forward contracts are traded Over-The-Counter (OTC): not in a centralized exchange, but through a network of dealers

### Futures Contracts
- Like a forward contract, but both parties deal with an exchange rather than with each other
- Futures contracts rely on margin calls
    - Margin calls happen when an investor borrows part of the money from a broker to invest in a portfolio; when the value of the portfolio decreases below a price, the investor receives a margin call from the broker -- the investir needs to either sell some assets or put more funds in the portfolio
    - The futures contract works like that
        - Future price is set
        - Present price is monitored
        - The buyer has a margin account with the settled money in it and can exit whenever he wants
        - If price goes down, the margin account is decreased with the difference: the broker takes money from the account
            - The buyer can be called if no money is in the margin account to be asked to put money in the margin account
            - If there is no money, they sell
        - If price goes up, the buyer is credited with the difference

### Rice Futures
- First Futures in the World: 1860 in Japan, Osaka - Dojima
- Japan had been isolated from the rest of the world, except with the Dutch, who had been already in Japan in the 1670s
    - Futures markets are not due to the Dutch, but the Dutch were very sophisticated already in 1600s.
- Rice needed to be stored somehow
- The futures market was quite sophisticated
    - Quality, type, delivery date: everything considered in the contract
    - Quality control experts were also in Dojima
- CBOT / CME: Chicago Market
    - Most of the futures are concentrated thee nowadays
    - Rice futures are also there now
    - The genious of futures contracts is that they predict the price
    - Most futures contracts are closed without delivery!
        - When the delivery date is arriving, the arbitrage guys decide to accept delivery

### Wheat Futures
- Speculators are not necessarily bad
    - The speculators are the ones who think on what's going to happen
    - Speculators have a broad perspective and wisdom; they decide on experience and many information
    - Speculators are regarded as gamblers; however, speculators are not mere gamblers, they are intellectuals; additionally, gambling is in the entertainment industry!
- Usual price curves
    - Usually, before the usual crop/delivery dates, prices go up because the storages are empty
    - After the crop has been collected, prices are expected to fall, bacause there is wheat or any other good available
    - The farmers could even drop a lot of wheat, so the prices fall a lot
    - The key idea is that future markets make shotages less severe, bacause we have already a price prediction, which abstracts what's going to happen

### Buying, Selling, and Settlement
- Hand signals are used in the market, because there's so much noise
    - That comes from Dojima
    - However, most of the trading happens electronically
- There's a daily settlement
    - The buyer puts money in the margin account and margin is taken from it
    - The futures contract is an agreement of a daily settlement of the margin
    - Importantly, it is rare that on the final day the contract there is an exchange of goods; futures markets are usually closed beforehand
        - With margin difference, the seller gets money from the buyer or the other way around!
        - If no contract has not been cancelled, trucks full of goods should be exchanged
    - The settling is done by the arbitrage role in the market
        - The abiter makes sure the margins contract and account are in order, and goods are delivered if needed
- What about indexed goods, for instance the SP500 index future - what is the role of arbitrage?
    - Recall in futures contracts everything is about the margins account: we don't pay the settled price, but transfer money between margin accounts depending on the variation of the price in the futures market
    - With indexed goods it's the same idea, but there is no exchange of goods at the end
- Cash settled future markets are a great invention in finance

### Fair Value in Futures Contract
- What should the futures price be? P_future = P_spot(1+r+s)
    - r: interest rate
    - s: storage cost
    - r+s: cost of carry
    - Futures price is usually above cash price (contango), otherwise "backwardation"
        - In harvest time, storage cost becomes negative, so the futures price decreases

### Oil Futures

- Futures are a way of predicting price
- Oil, when corrected with inflation, has not changed that much; stocks, on the contrary have gone up much
- Most people think that there not that much oil; but in reality, we keep on discovering new oil reserves
- Oil prices were constant in the USA between 1945 and 1970 aprox, because the government controlled its price
- OPEC: Organization of Petroleum Exporting Countries
    - 1960, iran, Iraq, Kuwait, Saudi Arabia, Venezuela
    - More countries followed later
    - OPEC is weak today because th emidle east is unstable
    - They wanted to keep prices up
    - It's a cartel
- Typically oil is controlled by non-democratic countries
- First oil crisis: 1973
- Second oild crisis: 1979 - Iranian Revolution
- The USA has oil reserves in case of war
- 2008 crisis
    - Prices fell from 113 USD / barrel to 30 USD aprox
    - This time the price variation was not caused by any wars in the middle east
    - Fracking was discovered
    - The price has been very volatile since

### Financial Futures: SP500 Index & FFR Futures
- Stock Price Index Futures
    - Cash settlement rather than physical delivery
    - Settlement: 250*(Index_t - Futures_(t-1))
    - Fair value
        - F = P + P*(r-y)
        - F: fair value futures price
        - P: stock price index
        - r: financing cost (interest rate)
        - y: dividend yield: it's like a negative storage cost
- Federal Funds Rate Futures Market (FFR)
    - Use to manage / observe expectations of interest rates
    - That market is watched a lot
    - They want to predict the Fed's rate months in the future
    - It's a good indicator

## Lesson 13: Options

### Options: Overview
- Option: it is a contract between 2 parties; one buys a choice in the future
    - Call option: you buy the right to buy something
    - Put option: you buy the right to sell something
- The choice is linked to the underlying asset price
- Options are truncated claims on assets
    - Call: claim on price if it rises above the contract option price
        - Then, we can sell the object and make a profit
- Terms of options contract
    - Exercise date and price
    - Definition of underlying number of shares
        - That is not limited to shares
- Options are actually quite old
    - It is often a way of convincing a selling part who is not willing to sell: we give him/her money to have an option

### Reading Options Pricing
- Option prices reading seems a bit confusing
- Strike field: contains a name with the price appended to it, eg: 27, 30, 32, 35
- Then, we have the last sport market price for the option, eg: 7.05, 4.8, 3.31, 2.36
- And finally, the spot market price of the real share: 31.63 USD

### Why Options Exist
- Theoretical reason: market inefficiency is alleviated with options market because risk is reduced
- Behavioral perspective:
    - Salience and attention: people pay attention to relevant or salient things
    - Put option is like an insurance: I buy the right to sell something at a price; even if the market price falls a lot, I can always sell it for the option price
    - Silver lining theory: people don't look at the bottom line or total outcome, but the look at smaller soothing aspects in the portfolio, as if the portfolio were different sources of income
        - That is not true: the portfolio as a global must be regarded: its outcome is the realization of a set of possibilities; it could go in different directions, the important thing is to have a diversified portfolio
        - Therefore, options are regarded as insurance and relieve in a portfolio, as a source of income
        - But, that is not really true

### Ubiquity of Options
- Options are everywhere: stocks, mortgages, farms, ...
- Options are as old as civilization
- Dutch had options in standardized forms in the 1670s.

### Derivatives
- Futures contracts, forward contracts, options, swaps, and warrants are commonly used derivatives.
- Derivatives can be used to either mitigate risk (hedging) or assume risk with the expectation of commensurate reward (speculation).
- Derivatives are often called weapons of mass destruction
    - They increase so rapidly that it's difficult to track them
    - There are typically derivatives in ETFs
    - However, they initially had a good insurance purpose

### Put / Call Parity
- On the exercise day, the price of the action can be higher/lower/same as the one specified in the option; if we have the right to sell (put) and the price is higher than the option, of course we sell and earn the difference
    - Usually, we need to take into account the Present Discounted Value of the stock and the dividends associated to it in the option period
    - Something analogous happens with the call options
- Recall: Preset Value = Future Value / (1+r)^n, n
    - n: number of periods
    - r: rate of interest
- The Put-Call Parity refers to the fact that both put and call options are equivalent and one can thus make money with them; in fact, many people gamble with options: if large amounts of money are used, big margins can be made
    - Price of stock = call price + pdv strike + pdv dividends - put price
- Black-Scholes differential equation is used to model the option and asset price
    - The obtained formula can be used to make money
    - However, Black-Scholes makes the assumption of normal distributions, which is not true
        - Due to that assumptions, tail events are not modelled

### Using Options to Hedge
- Imagine we trust a company and we want to buy stocks, but at the same time we fear the stock price might fall below a threshold
    - In that case, we buy the stocks and a put option so that we make sure we can sell the stock at a low limit
- Another option to reduce risk or insure: stop-loss orders
    - We ask our broker to sell if the stock falls below a threshold price
    - It seems to be similar to a put option, even better, because you don't have to buy the option
        - However, the broker is a human being and cannot buy/sell so fast and he/she may sell way below
        - Additionally, the price ca fluctuate around the stop-loss threshold; what should the broker then do?
        - A put option does not have these problems: we pay the price of the option to avoid these issues

### Skew
- CBOE publishes the skew value of put options, which could help predicting short-term market falls
    - Skew is the 3rd moment of the price, as variance is the 2nd
    - If markets fear a fall, the price of put options is expected to increase, because they'd be more demanded
    - However, the skew has a 30-day delay (?)


```python

```
