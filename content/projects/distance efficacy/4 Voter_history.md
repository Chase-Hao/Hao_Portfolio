---
date: "2021-10-01"
math: true
title: 4.Voter history
type: book
weight: 40
diagram: true
---

## Goal:
---
Get all CEOs voting history to identify their living addresses.
<br/><br/>
## Data source
---
**Voter History** and **Voter Registration**
<br/><br/>
## Processing flowchart
---
```mermaid
graph TD
A(Voter master data) --> B((voteID_match.py))
B --> |Name and DOB match|C( Voter Registration ID for each CEO)
B-->|City and Zip match |C
B -->|Spouse match|C

C-->|vote history search.py|D(Voter history records)
```
<br/><br/>

## Code detail
---
I use multiprocessing to do big-data matches.

Since there is no link between Voter registration ID and Lexis ID, I need to match them based on CEOs' info. There are three ways to match them.
1.  Based on CEOs' first and last name, the first character of middle name, month and year of birth .
2.  Based on CEOs' house address city and zip code. If CEOs have houses in this city or this zip code, then search CEOs' names and date of birth (DOB) in this area.
3.  Regardless of CEOs' house addresses, search CEOs' names and DOB and their spouses' names and DOB. If both matching results have the same addresses, we consider it a solid match because CEOs and their spouses live together in the same address.