---
date: "2021-11-01"
math: true
title: Main idea
type: book
weight: 10
diagram: true
---

There are a few factors are proved to be significantly correlated with cryptocurrency returns. This project is to extract those factors and try to use them construct strategy


### 1. Cryptocurrency network factors
Liu and Tsyvinski (2021)[1] construct this factor using data from Blockchain.info and 
Coinmetrics.io. But those datasets are paid and have 2 months time lag. I am still looking for the better data source to construct this factor
* the number of wallet users
* the number of active addresses
* the number of transaction count
* the number of payment count


### 2. Stock market return
Even though Liu and Tsyvinski (2021)[1] found crypto currency found crypto's exposure on stock market return is not significant. However, they are using data before 2018. After 2018, a lot institutional investors entered this market. In recent months, bitcoin price is usually going down when Dows' is going dow. Instituational investors' marginal value of wealth is likely to be influeced by stock market and thus influenced crypto market. I will also analyze this factor.


### 3. Investor sentiment
Two papers found this factor is significant in returns. Their data source is open source, I can use those websites' API to extract data and use text analysis to quantify the factor.
* Chen,Despres and ext. (2019)[2] think cryptocurrecy price exist huge bubble and found investor sentiment factor is significant in cryto price. They use different text analysis techique to analyze messages from StockTwits and Reddit.
* Liu & Tsyvinski (2021)[1] defines sentiment factor as 'log ratio between the count of positive and the count of negative phrases of cryptocurrencies in Google searches'


### 4. Investor attention
The Investor attention factor (Liu & Tsyvinski ,2021)[1] is constructed using open source and these two media provides API to extract them.
* Google searches
* Twitter post counts


### 5. Cryptocurrency momentum
Momentum is also proved significant (Liu & Tsyvinski ,2021)[1]. I can use technical analysis indicators in stock market to construct this factor.


### 6. Degree of disagreement
Liu & Tsyvinski (2021)[1] found 'cryptocurrency return is high when the current volume-volatility ratio is high. Volumns are usually high when investors have more disagreement with the price. So I can combine this indicator into technical analysis indictors


### 7. Arbitrage across different currecy exchanges
Makarov and Schoar (2020) found there are arbitrage opportunities across different currency exchanges due to market segmentation. However, it's kind hard to trade using different currencies.


## Reference
*[1] Liu, Yukun, and Aleh Tsyvinski. 2021. “Risks and Returns of Cryptocurrency.” Edited by Itay Goldstein. The Review of Financial Studies 34 (6): 2689–2727. https://doi.org/10.1093/rfs/hhaa113.*

*[2] Chen, Cathy Yi‐Hsuan, Romeo Despres, Li Guo, and Thomas Renault. 2019. “What Makes Cryptocurrencies Special? Investor Sentiment and Return Predictability During the Bubble.” SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3398423.*

*[3] Makarov, Igor, and Antoinette Schoar. 2020. “Trading and Arbitrage in Cryptocurrency Markets.” Journal of Financial Economics 135 (2): 293–319. https://doi.org/10.1016/j.jfineco.2019.07.001.*




