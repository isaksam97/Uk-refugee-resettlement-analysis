# UK Refugee Resettlement Analysis — Gloucestershire (2020–2025)

## Project Overview

This project analyses UK refugee resettlement data for the South West region (Gloucestershire) covering 2020 to 2025. It examines arrivals, housing allocation, service uptake, and processing times across four resettlement schemes: the UK Resettlement Scheme (UKRS), Afghan Resettlement Programme, Ukraine Scheme, and Community Sponsorship Scheme.

The analysis was built to support insight-driven decision-making for local authority stakeholders — mirroring the kind of management information and community data analysis carried out by county council data teams.

---

## Tools Used

- **Python (Pandas)** — data cleaning, transformation, and enrichment
- **Power BI** — interactive dashboard and data visualisation
- **SQL** — data querying and aggregation
- **CSV / Open Data** — UK government resettlement statistics

---

## Dataset

The dataset covers 58 records across 6 years (2020–2025) and includes:

| Column | Description |
|---|---|
| year / quarter | Time period of data |
| scheme | Resettlement scheme (UKRS, Afghan, Ukraine, Community) |
| nationality | Country of origin |
| arrivals | Number of people arrived |
| housing_allocated | Number successfully housed |
| housing_pending | Number awaiting housing |
| service_uptake_pct | % accessing resettlement services |
| avg_processing_days | Average days to process each case |
| employment_support | Number receiving employment support |
| english_language_support | Number receiving English language support |
| children_in_education | Number of children enrolled in education |

---

## Data Preparation

The raw dataset was cleaned and enriched using Python (Pandas):

- Created a proper `date` column for Power BI time-series charts
- Added `quarter_num` to ensure correct chronological sorting
- Calculated `housing_fill_rate_pct` — percentage of arrivals successfully housed
- Calculated `housing_gap` — number of arrivals not yet housed
- Calculated `employment_rate_pct` and `english_support_rate_pct`
- Added `processing_speed` category (Fast / Medium / Slow) for visual colour coding
- Validated data for nulls, duplicates, and out-of-range values — none found

---

## Key Insights

### 1. The 2022 Ukraine surge
Arrivals rose sharply from 1,298 in 2021 to 4,205 in 2022 — a 3x increase driven entirely by the Ukraine Scheme following Russia's full-scale invasion. This placed significant pressure on local housing and service capacity.

### 2. Processing speed gap between schemes
The Ukraine Scheme processed arrivals in an average of **52 days**, compared to **191 days** for the UKRS — a 3.7x difference. This reflects the emergency fast-track nature of the Ukraine response versus standard resettlement procedures.

### 3. Strong housing fill rate overall
**7,330 out of 7,902 arrivals (92.8%)** were successfully housed. However, housing pending figures spiked during the 2022 surge, highlighting the strain placed on local authority housing teams during peak periods.

### 4. Service uptake is consistently high
Average service uptake across all schemes was **86.5%**, suggesting strong engagement between resettled communities and local support services. This is a positive indicator for integration outcomes.

### 5. Post-peak decline requires forward planning
Arrivals dropped sharply from 4,205 in 2022 to just 122 in early 2025. This trend has significant implications for resource allocation — services scaled up for peak demand may need reconfiguration as volumes decline.

### 6. Ukrainian nationals dominate overall arrivals
Ukrainians account for **63% of all arrivals (5,000)**, followed by Afghans (28%, 2,231), Syrians (6%, 480), Eritreans (1.3%, 99) and Sudanese (1.2%, 92).

---

## Power BI Dashboard

The dashboard includes 5 interactive visuals:

1. **KPI card** — Total arrivals (7,902)
2. **Line chart** — Sum of arrivals by year (shows 2022 surge clearly)
3. **Bar chart** — Sum of arrivals by nationality
4. **Donut chart** — Arrivals by scheme breakdown
5. **Bar chart** — Average processing days by scheme

All visuals are connected to a **year slicer** — clicking a year filters the entire dashboard instantly.

![Dashboard Screenshot](dashboard_screenshot.png)

---

## How to Run

1. Clone this repository
2. Open `uk_refugee_resettlement_transformed.csv` in Power BI Desktop via Get Data → Text/CSV
3. All visuals will load automatically
4. Use the year slicer to filter by time period

Or run the Python cleaning script:

```bash
pip install pandas
python clean_data.py
```

---

## Relevance to Local Authority Work

This project directly mirrors the data management and reporting work undertaken by county council data teams supporting UK resettlement programmes. The analysis focuses on:

- Monitoring arrivals and housing allocation against targets
- Identifying service uptake gaps across demographic groups
- Producing KPI reporting for local authority stakeholders
- Supporting resource planning through trend analysis

It was built with reference to Gloucestershire's role in the South West resettlement programme and reflects the kind of insight-driven analysis that supports elected Members and operational teams in understanding community needs.

---

## Author

**Isak Sam** — Data Analyst  
MSc Data Science, UEL University  
GIS & Data Analyst, Gloucestershire County Council  
[LinkedIn](https://www.linkedin.com/in/isaksam) | [GitHub](https://github.com/isaksam97)  
isaksam97@gmail.com

