---
date: "2021-11-01"
math: true
title: Main idea
type: book
weight: 10
diagram: true
---

There are a few factors that are shown to be significantly correlated with cryptocurrency returns. This project is intended to extract those factors and try to use them construct a trading strategy.

### 1. Cryptocurrency network factors
Liu and Tsyvinski (2021)[1] construct this factor using data from Blockchain.info and Coinmetrics.io. But those datasets are paid and have 2 months time lag which can not be used in the daily trading strategy. I am still looking for the better data source
* the number of wallet users
* the number of active addresses
* the number of transaction count
* the number of payment count


### 2. Stock market return
Even though Liu and Tsyvinski (2021)[1] found cryptocurrency's risk exposure on stock market return is not significant, they are using data before 2018. After 2018, a lot of institutional investors entered this market. In recent months, Bitcoin price is often going down when Dows' is going down. Since institutional investors also invest heavily in stock markets, according to intermediary asset pricing theory their marginal value of wealth can be influenced and reflected by the stock market. Therefore, stock market is likely to co-move with the stock market. I will also analyze this factor.

### 3. Investor sentiment
Two papers found this factor is significant in cryptocurrency returns. Their data sources are open sources, so I can use those websites' API to extract data and use text analysis to quantify the investor sentiment.
* Chen, Despres, etc. (2019)[2] think there is huge bubble in cryptocurrency market and found investor sentiment factor is significant on crypto returns. To construct this factor, they use different text analysis techniques to analyze messages from StockTwits and Reddit.
* Liu & Tsyvinski (2021)[1] define sentiment factor as: *'log-ratio between the count of positive and the count of negative phrases of cryptocurrencies in Google searches'*


### 4. Investor attention
The Investor attention factor (Liu & Tsyvinski,2021)[1] is constructed by using open source(Google and Twitter). These two media platforms provide APIs to extract them.
* Google searches
* Twitter post counts


### 5. Cryptocurrency momentum
Momentum is also proved significant (Liu & Tsyvinski ,2021)[1]. Some technical analysis methods in the stock market are using momentum factor. I could refer to those methods to construct momentum factor indicator in crypto market.


### 6. Degree of disagreement
Liu & Tsyvinski (2021)[1] found 'cryptocurrency return is high when the current volume-volatility ratio is high. Volumes are usually high when investors have more disagreement with the price. This means volumes and price volatility could also reflect crypto prices.

### 7. Arbitrage across different currecy exchanges
Makarov and Schoar (2020) found there are arbitrage opportunities across different currency exchanges due to market segmentation. However, it's kinda hard to trade using different currencies on different crypto platforms. In the US, only a limited number of platforms are allowed. And they can only trade in US dollars.


## Reference
*[1] Liu, Yukun, and Aleh Tsyvinski. 2021. “Risks and Returns of Cryptocurrency.” Edited by Itay Goldstein. The Review of Financial Studies 34 (6): 2689–2727. https://doi.org/10.1093/rfs/hhaa113.*

*[2] Chen, Cathy Yi‐Hsuan, Romeo Despres, Li Guo, and Thomas Renault. 2019. “What Makes Cryptocurrencies Special? Investor Sentiment and Return Predictability During the Bubble.” SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3398423.*

*[3] Makarov, Igor, and Antoinette Schoar. 2020. “Trading and Arbitrage in Cryptocurrency Markets.” Journal of Financial Economics 135 (2): 293–319. https://doi.org/10.1016/j.jfineco.2019.07.001.*




