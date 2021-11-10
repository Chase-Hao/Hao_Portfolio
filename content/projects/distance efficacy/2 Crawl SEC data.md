---
date: "2021-10-01"
math: true
title: 2.Crawl SEC data
type: book
weight: 20
diagram: true
---
## Goal:

---

1.  Get all companies' Headquarter addresses from 2000 to 2020.
2.  Find records that companies relocate their headquarters.
<br/><br/>

## Data source
---
**SEC EDGAR**: <u>https://www.sec.gov/cgi-bin/srch-edgar</u>

I also manually checked all companies' headquarter addresses from 2000 to 2020. If you need this data for research, please contact me.*
<br/><br/>

## Processing flowchart
---
```mermaid
graph TD
A(SEC edgar web) -->|get_10k_url.py| B(Get all 10k report links)
B --> |crawl header.py| C( SEC header info for each company)
C-->|parse header address.py| D(HQ addresses in header)

B-->|crawl_10k.py| C1(HQ address in annual report)
C1-->|HQ_coor.py|D1(HQ address coordinates)

```
<br/><br/>
## Code detail

---

### Get url
Get all 10k reports' **url links**. There are 3 different types of financial reports: **10-K** (Regular annual report),**10-K405** (Delayed report),**10-KSB** (Small business).

### Get address
1. Address in **'header'**: 'header' usually appears before report content in Html which is not shown directly in the website. It is usually **standardized**, so it's easy to use a regular expression (**regex**) to parse. However, addresses in the header are usually **out-of-date**. It's hard to accurately identify when a company relocates its HQ.
2. Address in **annual report (10k)**: Because the time range is so long, Html evolves through 3 **different formats** (old Html, Html, iXBRL). So I need to **cut**  the first page of each report, then parse this small part. A lot of HQ addresses are in **certain position**, like, before '(address of principal address)'. But some of them are not in the standard format. I create a sophisticated **address regex** to capture the remaining HQ addresses. Besides, there is also a situation that financial reports containing **multiple** companies. In this case, I search for the target company name first and then search for the HQ address

### HQ Relocation
I also search for **headquarter relocation indicator**: whether this company relocates its headquarter in this year.
1.  **Search** every 10k report for certain **keywords**. For example, search 'headquarters' first and then search for 'relocate' around 50 words of the first search. I used a list of keywords in the code.
2.  Because the address' format is slightly different from year to year. I need to **calculate the similarity** of a company's this year's HQ address and its last year's address. Usually, 'similarity'<80% indicates the change of HQ address.
