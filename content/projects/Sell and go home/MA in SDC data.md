---
date: "2021-11-01"
math: true
title: "M&A in SDC data"
type: book
weight: 10
diagram: true
---

## Goal:
---
- Get incremental M&A transactions related to commuters' companies from SDC data
- Match other RAs manual work with SDC records
<br></br>
## Data Source
---
**SDC data**: contains company merger and acquisition transactions

<br></br>
## Process flowchart
---
```mermaid
graph TD
A1[Other RAs manual matches ] --> | search for SDC ID|B1(other RAs work matches with SDC)
A3(SDC data) -->|Filter Target Company.py|B1 

A(Commuter CEOs company) -->|get CEOs info|B1

A-->|"new match SDC.py"|C1(Incremental M&A records)
C1-->|clean new match.py and manual check|D(result)
```
<br></br>
## Code detail
---
#### Get increment matches
1. Fuzzy search for companies name
2. Search for 6-digit CUSIP first and then manually check
3. Search for the first 5 CUSIP digits and set flag to identify if deal synopsis contains company name
#### Identify other RAs' work in SDC
1.  Get SDC ID: Fuzzy search for target company name and acquiror company name in SDC data
2.  Get CEO ID: Fuzzy search CEOs' name and their companies' name in 'commuter file'(data that contains commuter CEO information)