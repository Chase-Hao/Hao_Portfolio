---
date: "2021-11-01"
math: true
title: Auto-Trading bot
type: book
weight: 10
diagram: true
---
## Goal:
---
- Code to realize auto-trading under a strategy
<br></br>
## Requirement
---
CXCT: framework combining different platforms' API
<br></br>
## Code detail
---
Use CXCT framework to get different platform API: cryptocurrency platform API
* log in one of the cryptocurrency platform
* fetch last n 15mins candle sticks data
* build strategy, create signal to buy and sell
* when signal occurs, trade in market value
* set time schedule to run it in every 15 minutes