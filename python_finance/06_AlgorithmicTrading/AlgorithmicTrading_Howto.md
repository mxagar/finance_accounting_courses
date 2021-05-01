# Algorithmic Trading

This document summarizes the last two sections of the Udemy course by José Marcial Portilla

**Python for Financial Analysis and Algorithmic Trading**

The videos of the original course explain how to perform backtests with trading algorithms using Quantopian. However, Quantopian was acquired in late 2020 by Robinhood and the `zipline` servers offering the Quantopian services were shut down. Therefore, two alternatives are possible:
1. Run the backtests locally installing the `zipline` library
2. Use Blueshift instead of Quatopian; Blueshift seems to be identical, also free: https://blueshift.quantinsti.com

However, my experience with Blueshift was not as good as expected. The main issue is that they have almost no documentation and there seems to be no text completion/documentation in the IDE's code editor. [Zipline](www.zipline.io) seems to be down, so I cannot access to the documentation to install it correctly.

## Some notes on the videos

- We use an online IDE accessed through the browser.
- In the IDE, we write trading algorithms and backtest them: we run our algorithms and see how portfolios would have developed with historical data; then, it is possible to go live.
    - Buy/sell actions are executed in the backtest; our algorithm decides to buy/sell depending on the price
    - Note that we could implement backtests and trading algorithms in python using pandas an numpy, but that functionality is already implementes in `zipline` and `pyfolio`, and embedded in a comfortable IDE
    - Morevover, a complete history of states is registered with those libraries, which can be later analyzed
- Create an account.
- In the Strategies tab
    - We can create strategies: basically, trading algorithms
    - We can see the strategies
    - We can backtest them
    - We can also see the backtests
- Usual workflow
    - Press `Create Strategy`
    - Code in IDE
    - Press Backtest: we see the returns of algorithm and the benchmark (market)
- Visit the Quantopian github! (however, some links are not working)
    - [https://github.com/quantopian](https://github.com/quantopian)
    - There are several packages
        - `zipline`: if we install it locally, we can do backtests locally on our computer; however, it's not that easy to install
        - `alphalens`: alpha prediction
        - `pyfolio`: portfolio risk analysis
        - ...
- The IDE uses `zipline` and it requires some expeteced functions
    - `initialize`: a `context` variable is created, which contains the stocks or the portfolio
    - `handle_data`: called every minute to perform actions depending on stock values
    - `schedule_function`
    - ...
- The Quantopian IDE had a debugger integrated, too
- Quantopian had Jupyter notebooks, too
- It is possible to
    - do leveraging: you borrow money and invest it; basically, the sum of the weights is lager than 1
        - that is really risky
        - we can put some leverage ratio thresholds to avoid too much risk
    - short: basically, the weights of stocks to short are negative
    - work with futures
 
### Some algorithms programmed

- Pair-trading: Order when the spread of two highly correlated stocks increases
    - Two highly correlated stocks are often cointegrated, which is great for pair trading
    - When two stocks are highly correlated, they move together, therefore their spread (difference) should be small
    - The historical spread is computed, and the Z-score along the time: (value - mean)/std
    - The Z score is like the normalized (Gaussian with mean 0 and std 1) transform of the spread in time; **every time its magnitude gets big, we expect a regression to the mean!**
    - We compute the Z score and plot it; we detect positive and negative limits in the diagram for Z
    - The algorithm would be: every time Z is below the negative limit or above the positive one, I expect a regression to the mean (0), therefore I could long or short on or the other stock
    - The Z-score will be computed with rolling in a window of 30 days, for instance, because during production it makes more sense to go that way (we don't have all the historical data)
    - Note: in the backtest, the instructor lost money with 2 years of data
- Trading using Bollinger bands
    - We compute the running Bollinger bands of a stock price
    - If price goes above the upper limit, we short it
    - If the price goes below the lower limit, we buy the stock
    - The returns in the backtest were 60%, but it really depends on the stock tried: some stocks yield -45%!
- Stock sentiment analysis
    - Sentiment analysis performs natural language processing (NLP) on texts related to stocks to evaluate a sentiment score `[-1,1]` which would predict the evolution of the price
    - The texts are extracted from social media and news
    - Usually sentiment analysis data is not free; we can also program it on our own... however, Quantopian offered free sentiment analysis data for certain time periods
    - The instructor performs sentiment analysis and it performs pooly; possible reasons:
        - The analyzed texts might be generated after the price action has happened, e.g., when it goes down people write bad news, when it goes up people write good things; therefore, teh sentiment is not a predictor, but the predicted by the price
        - The used dataset is a free one; companies usually have their own datasets, probably better than those free ones
        - We can expect many people are using available datasets, free or not; that has an effect, since we are not spotting a bargain, as we might expect