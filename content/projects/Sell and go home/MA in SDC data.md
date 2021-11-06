---
date: "2021-11-01"
math: true
title: MA in SDC data
type: book
weight: 10
diagram: true
---

## Goal:
---
- Get M&A transactions related to commuters' companies from SDC data

<br></br>
## Data Source
---
SDC data

<br></br>
## Process flowchart
---
```mermaid
graph TD
A1[Other RAs munual matches ] --> | search for SDC ID|B1(other RAs work matches with SDC)
A3(SDC data) -->|Filter Target Company.py|B1 

A(Commuter CEOs company) -->|get CEOs info|B1

A-->|"new match SDC.py"|C1(Incremental M&A records)
C1-->|clean new match.py and manual check|D(result)
```
<br></br>
## Code detail
---
1. Fuzzy search for companies name
2. Search for 6-digit CUSIP first and then manually check