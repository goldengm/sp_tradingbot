# Blockchain Trading Bot

In this proprietary program from [DaScient Capital](https://dascientcapital.us), we utilize Reinforcement Learning ensembles, the SuperTrend indicator, Kalman Filter Forecast Model/Parameterization, Simple & Exponential Moving Averages, the Relative Strength Index (RSI), and various other robust technical indicators. These tools are used in a template to generate intelligent trade signals, suggesting profitable buy and sell orders on platforms like Robinhood, Binance.US, and TD Ameritrade, all implemented using Python.

Feel free to expand, modify, and enhance your own versions, as the core principles of this project (i.e., decision science & forecast modeling) are widely applicable to any predictive/time-series/machine learning endeavors beyond trading and asset management. We only ask that you acknowledge our contributions and adhere to our open-source community guidelines.

More information on the project’s initiation and development can be found in this [Medium publication](https://medium.com/coinmonks/daily-binance-us-crypto-trade-signals-fda4e8a205c8). This [Kaggle Notebook](https://www.kaggle.com/code/dascient/daily-crypto-buy-sell-decision-maker) demonstrates an automated solution with intricately calculated recommendations.

Our current focus is to incorporate social sentiment analyses, advanced technical indicators, and pre-built strategies to enable autonomous trading. Our platform aims to let users replicate peer portfolios, create their own, or join publicly reviewed group-asset allocation pools rated by the community. Additionally, we plan to continuously assess and fine-tune the bot’s parameters to enhance decision signals over time, increasing confidence the longer it operates.

Our ultimate objective is to optimize returns and minimize losses for everyone, making trading as straightforward and accessible as possible through automation.

Our mission is to leverage statistical and mathematical modeling, deep financial analytics, data science, strategic intelligence, and machine learning to provide reliable, resourceful, and open-source user-friendly products.

If you find value in our project or wish to contribute, even just to say thanks, please contact us. Contributions are welcome as donations to this ongoing effort, and we appreciate a "hello, world!"

---

### SuperTrend - Trends! :computer:

This feature enables users to fully or partially imitate the portfolio allocations of others. The Trends enhancement helps users stay informed about the SuperTrends trading community. Users can search for groups and strategies that match their risk levels. They can also create, share, and update their own portfolios within the community, meaning any new allocations by the group leader will automatically reflect in everyone’s portfolios. Let your creativity roam.

---

## The Bot - Our SuperTrend Overview :robot:

This repository documents the development of our first trading bot, categorized into three main classes:

1. Data Class
2. Trade Strategy Class
3. Execution Class

---

### What’s Needed?

While our team is diligently developing and deploying a user-friendly app, you can still test the bot on your own as we work towards our goals. Feel free to fork, star, and watch for updates on GitHub.

Here’s what you need to run the bot locally. An introductory Python course might be helpful. Your input, suggestions, and ideas for improving efficiency or scalability are welcome. The project is far from perfect, but your support and interest motivate us to release and refine it. Contact us at contact@dascient.com if you need help.

---

#### Requirements

1. [Python (Latest +3.9.7)](https://www.python.org/ftp/python/3.9.7/python-3.9.7-macosx10.9.pkg)
2. Jupyter Notebook - Anaconda ([mini-conda is sufficient](https://docs.conda.io/en/latest/miniconda.html))
3. Binance.US crypto brokerage account (API_KEY, API_SECRET)
4. Clone this repository to an easily accessible location (e.g., ./Desktop/GitHub).

Don’t have Binance.US? [Sign up here!](https://accounts.binance.us/en/register?ref=52441695)

1. After logging in, go to settings and find API MANAGEMENT.
2. Create an API and follow approval instructions.
3. Save and KEEP SAFE your api.key & api.secret (store in a config.py as per [this format](https://github.com/DaScient/SuperTrendTradingBot/blob/main/Binance%20Trading%20Bot/config.py)).

## To run

Open terminal, navigate to binance_bot.py, and execute with:

```bash
$ python binance_bot.py
```


For [Reinforcement Learning Mod - Binance Bot](https://github.com/DaScient/SuperTrendTradingBot/tree/main/RL-Binance), follow these [instructions](https://github.com/DaScient/SuperTrendTradingBot/blob/main/RL-Binance/README.md).

 ---

### SuperTrend - Data :computer:

This class connects to the Binance.US WebSocket interface via CCXT, providing live cryptocurrency data in the form of candlesticks: Open, High, Low, Close (OHLC).

We also apply rolling averages, upper/lower Bollinger bands, and binary variables that evaluate uptrend/downtrend intervals.

---

### Trade Strategy :chart_with_upwards_trend:

With a variety of trade strategies to choose from, the strategy class is designed to be modular. It supports a "plug-and-play" approach, allowing different trading strategies to be developed over time. As long as the strategy sends a buy/sell signal for execution, it will work correctly.

---

### Execution :moneybag:

Once a trade signal is generated, the execution class sends the order to Binance.US via ccxt.exchange.

Relax, have fun, and stay hydrated! :tada::rocket::full_moon:

---