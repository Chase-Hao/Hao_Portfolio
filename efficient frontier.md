## Data 

1. Use monthly return and weekly return   
    -    monthly and weekly returns' time range is the same for S&P500 and crypto
2. exclude stable coin, exclude coin whose market cap smaller than 10000 $
3. Crypto ranking criteria is based on market cap rank (Market Cap = Price * Circulating Supply)
    -   circulating supply defination: https://support.coinmarketcap.com/hc/en-us/articles/360043396252-Supply-Circulating-Total-Max-#circulating_supply

## Calculation
#### 1. Efficient Frontier
$$ \min_w \sigma^2_{portfolio,w} =  w^T\sum{w}$$
$$s.t. \  \  \ \  1^Tw = 1$$
$$ w^T \bar{R} \ge r$$
 - r is all possible return
 -  R_bar is sample mean
#### 2. Optimal ex-post portfolio
$$ \min_w SP ratio= \frac{w^T \bar{R}}{\sigma_{portfolio,w}}$$
$$s.t. \ \ \  1^Tw=1$$

## Result