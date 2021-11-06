---
date: "2021-10-01"
math: true
title: 5.CEO network
type: book
weight: 50
diagram: true
---

## Goal:
---
1.  Get CEOs pairs who live in 1km away to each other.
2.  Get CEOs who live in same block and same tract.
<br/><br/>

## Data source
---
**LexisNexis Data**: CEOs addresses information

**Census tract and block data**: <u>https://www2.census.gov/geo/tiger/TIGER2020/TRACT</u>

**Census geocoder** :<u>https://geocoding.geo.census.gov/geocoder/geographies/coordinates</u>
<br/><br/>

## Processing flowchart
---
```mermaid
graph TD
A(Lexis CEO address data) -->|CEO_distance_matrix.py | B( CEO distance pairs)
B-->| clean_distance_matrix.py|C(CEO pairs living within 1 km)
A1(Census web) -->|download tract.py| B1(US tract and block geodata)
B1-->|CEO_tract_block.py|C1(CEO address with tract and Block ID)
A1-->|"crawl block and tract.py (slow)"|C1
```
<br/><br/>


## Code detail
---
**Multiprocessing** for big-data calculation and matching
### Distance matrix
1.  Get all CEOs home addresses coordinates and **translate** into meter coordinates.
2.  For each CEO, remove his/her addresses in whole dataset first and then calculate the distance to every other address (**distance matrix**)
3. write down every calculation into a file named by LexID

### Get Tract and Block ID
1.  **Restricting search range** can save a lot of time. For **TractID**, label geodata into different state name and then for each address search only in its state's tract data. For **BlockID**, similarily search each block based on TractID first.
2. **Alternative way**: Just crawl from census geocoder website, it's easy but slow for big data