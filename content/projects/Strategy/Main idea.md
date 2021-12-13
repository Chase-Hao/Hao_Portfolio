---
date: "2021-11-01"
math: true
title: Main idea
type: book
weight: 10
diagram: true
---

There are a few factors that are shown to be significantly correlated with cryptocurrency returns. This project is intended to extract those factors and try to use them to construct a trading strategy.

#### 1. Cryptocurrency network factors
Liu and Tsyvinski (2021)[1] construct this factor using data from Blockchain.info and Coinmetrics.io.But those datasets are paid and have two months time lag which can not be used in the daily trading strategy. I am still looking for the better data source.  The crypto-network factor is measured from the following perspectives.
* the number of wallet users
* the number of active addresses
* the number of transaction count
* the number of payment count


#### 2. Stock market return
Liu and Tsyvinski (2021)[1] found cryptocurrency’s risk exposure on stock market return is insignificant using data prior to 2018. After 2018, a lot of institutional investors entered the market. In recent months, Bitcoin price often goes down when Dows goes down. Since institutional investors also invest heavily in stock markets, shocks in stock market probably influence institutions' investment strategies' in crypto-market and further influence crpto prices.

#### 3. Investor sentiment
Two papers found this factor to be significant in cryptocurrency returns. Their data sources are open sources, so I can use those websites' API to extract data and use text analysis to quantify investor sentiment.
* Chen, Despres, etc. (2019)[2] think there is a huge bubble in the cryptocurrency market and found that the  investor sentiment factor is significant on crypto returns. To construct this factor, they use different text analysis techniques to analyze messages from StockTwits and Reddit.
* Liu & Tsyvinski (2021)[1] define sentiment factor as: *'log-ratio between the count of positive and the count of negative phrases of cryptocurrencies in Google searches'*


#### 4. Investor attention
The Investor attention factor (Liu & Tsyvinski, 2021)[1] is constructed by using open sources (Google and Twitter). These two media platforms provide APIs to extract themthis data.
* Google searches
* Twitter post counts


#### 5. Cryptocurrency momentum
Momentum is also proved shown to be significant (Liu & Tsyvinski , 2021)[1]. Some technical analysis methods in the stock market are based on momentum factors. I could refer to those methods to construct momentum factor indicators in the crypto market.


#### 6. Degree of disagreement
Liu & Tsyvinski (2021)[1] found "cryptocurrency return is high when the current volume-volatility ratio is high". Volumes are usually high when investors have more disagreement with the price. This means volumes and price volatility could also reflect crypto prices.

#### 7. Arbitrage across different currency exchanges
Makarov and Schoar (2020) found arbitrage opportunities across different currency exchanges due to market segmentation. However, it's quite hard to trade using different currencies on different crypto platforms. In the US, only a limited number of platforms are allowed and they can only trade in US dollars.

## Recent event 
1.  Bitcoin ETF was approved by SEC last month
2.  Companies which accept bitcoins 
    -   https://www.yahoo.com/now/10-major-companies-accept-bitcoin-190340692.html
3.  Banks which invest into cryptomarket
    -   https://money.usnews.com/investing/stock-market-news/slideshows/bank-stocks-investing-in-cryptocurrency
4.  Companies which own bitcoin
    -   https://www.buybitcoinworldwide.com/treasuries/
    
## Further exploration 
1.  Will institutional investors make Bitcoin prices more stable?
    -  The financial market tends to be more mature when there are more institutional investors (like the US stock market). Investment companies use high-frequency trading bots to gain profit. This may reduce volatility.
    -  Institutional investors can also use financial derivatives (like Perpetual contracts) to flatten volatility
    -  Brunnermeier and Nagel(2004)[4] found institutional investors may prefer to ride bubbles during 2000 Technology Bubble.
2.  How do Bitcoin ETFs influence Bitcoin price?
3.  Will Bitcoin price move together with blockchain tech companies' stock price?
4.  Why do companies invest in Bitcoin? How does bitcoin price influence company value, cash flow, or other performance?
6.  People say Bitcoin is electronic gold but does it have the same financial characters as gold.
    -   How does bitcoin price correlate with the US Dollar Index/inflation rate?
## Related paper

#### Factor model (empirical)
1.  Liu, Yukun, Aleh Tsyvinski, and Xi Wu. n.d. “Common Risk Factors in Cryptocurrency,”
2.  Liu, Yukun, Aleh Tsyvinski, and Xi Wu. 2021. “Accounting for Cryptocurrency Value.” SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3951514.
3.  Liu, Yukun, and Aleh Tsyvinski. 2021. “Risks and Returns of Cryptocurrency.” Edited by Itay Goldstein. The Review of Financial Studies 34 (6): 2689–2727. https://doi.org/10.1093/rfs/hhaa113.
4.  Chen, Cathy Yi‐Hsuan, Romeo Despres, Li Guo, and Thomas Renault. 2019. “What Makes Cryptocurrencies Special? Investor Sentiment and Return Predictability During the Bubble.” SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3398423.

#### Theoretical model
5.  Cong, Lin William, Ye Li, and Neng Wang. 2021. “Tokenomics: Dynamic Adoption and Valuation.” Edited by Itay Goldstein. The Review of Financial Studies 34 (3): 1105–55. https://doi.org/10.1093/rfs/hhaa089.

#### Mining industry
6.  Lin William Cong, Zhiguo He, Jiasun Li, Decentralized Mining in Centralized Pools, The Review of Financial Studies, Volume 34, Issue 3, March 2021, Pages 1191–1235
#### Other
7.  Alexander, C., and M. Dakos. 2020. “A Critical Investigation of Cryptocurrency Data and Analysis.” Quantitative Finance 20 (2): 173–88. https://doi.org/10.1080/14697688.2019.1641347.

## Reference
*[1] Liu, Yukun, and Aleh Tsyvinski. 2021. “Risks and Returns of Cryptocurrency.” Edited by Itay Goldstein. The Review of Financial Studies 34 (6): 2689–2727. https://doi.org/10.1093/rfs/hhaa113.*

*[2] Chen, Cathy Yi‐Hsuan, Romeo Despres, Li Guo, and Thomas Renault. 2019. “What Makes Cryptocurrencies Special? Investor Sentiment and Return Predictability During the Bubble.” SSRN Electronic Journal. https://doi.org/10.2139/ssrn.3398423.*

*[3] Makarov, Igor, and Antoinette Schoar. 2020. “Trading and Arbitrage in Cryptocurrency Markets.” Journal of Financial Economics 135 (2): 293–319. https://doi.org/10.1016/j.jfineco.2019.07.001.*

*[4] K. Brunnermeier, Markus, and Stefan Nagel. 2004. “Hedge Funds and the Technology Bubble.” The Journal of Finance 59 (5): 2013–40. https://doi.org/10.1111/j.1540-6261.2004.00690.x.*



