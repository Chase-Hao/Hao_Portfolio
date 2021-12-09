---
date: "2021-11-01"
math: true
title: "CEO and Spouse voting panel"
type: book
weight: 20
diagram: true
---

## Goal
---
Create an address panel data for all M&A target companies' CEOs and their spouses based on voting history records.
<br></br>
## Data Source
---
Voting history data
Lexisnexis data (personal address data)
SEC edgar data (Head quarter address)
<br></br>
## Process flowchart
---
```mermaid
graph TD
A1[matched M&A transaction] --> |match with Lexis data|B1(CEOs and spouses information)

B1 -->| get_vote_his.py|C1(CEOs voter registration records)

B1 -->| spouse_match.py|C2( Spouse voter registration records)

C1 -->| match_history.py| D1(CEOs voting history records)

C2 -->| match_history.py| D2(Spouses voting history records)

D1-->| voter panel2.py|E1( CEOs, Spouses and HQ addresses panel)

D2-->|munual check|E1

E1 -->|calculate panel distance|F1( distance between CEOs and spouses, CEOs and HQs)
```
<br></br>
## Code detail
---
1. Match voting registration records based on first name, last name, date of birth, houses address (from Lexis data), spouse information. 
2.  Manual checking is needed when searching voting history because different states' voting data has different variables.
3.  Check if voting registration addresses are listed in Lexis reports
4.  Extract Headquarter address from HQ address panel created in RA_work1
5.  When there are no voting records in a particular year, use the house address with the maximum number of household members in Lexis reports.