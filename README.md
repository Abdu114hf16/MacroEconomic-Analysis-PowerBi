# Macroeconomic Analysis: Income vs. Inflation

## 📌 Project Overview
This Business Intelligence project is an end-to-end data analysis pipeline designed to uncover the historical relationship between US inflation rates and industry-specific job growth and earnings. The objective is to identify which economic sectors demonstrate the highest resilience during periods of severe macroeconomic stress in US.

## 🏗️ End-to-End Analysis Pipeline

### Phase 1: Data Integration & Ingestion
To simulate a real-world enterprise environment, data was extracted and consolidated from three disparate sources:
1. **Local Datasets:** Foundational census and industry data files.
2. **Cloud Storage:** Remote datasets ingested directly from a Microsoft Azure Blob Storage container.
3. **Web Extraction:** Additional required data about Consumer Price Index (CPI) and inflation data extracted from the [Federal Reserve Economic Data (FRED) database](https://fred.stlouisfed.org/).

### Phase 2: Data Cleaning & Transformation and Modeling
* Processed raw data using different techniques through Power Query to clean and format, and standardize column structures.
* Architected a Star Schema relational model, connecting multiple fact tables (Industry Jobs, Industry Earnings) to a centralized, custom-built Date dimension table to ensure accurate time-intelligence filtering.

### Phase 3: DAX & Business Logic
Engineered dynamic DAX measures to translate raw data into business logic, utilizing functions such as `CALCULATE`, `FILTER`, `AVERAGE`, `MAX`, and `IF`. 
* *Example:* Created contextual measures to isolate and average industry income specifically during high-risk inflation years (>4%).

### Phase 4: Visualization & Reporting
Developed an interactive, multi-page Power BI dashboard:
* **Executive Summary:** High-level KPIs and top-market-share breakdowns for immediate stakeholder consumption.
* **Income vs. Inflation:** A dual-axis time-series analysis comparing raw wage growth against inflation percentage spikes.
* **Industry Job Growth:** Dynamic "Top N" filtering allowing users to explore the historical workforce volume of the top 5 US industries.

## 📊 Dashboard Preview
*(Note: View the full static dashboard in the `Dashboard_Preview.pdf` file).*

## 💡 Key Business Findings
1. **Purchasing Power Erosion:** While average industry income nominally increases over time, the dual-axis analysis reveals severe erosion of real purchasing power during inflation spikes (e.g., the historical 13.55% peak).
2. **Sector Resilience:** Filtering the data specifically for high-inflation years (>4%) shows that the Utilities and Management sectors maintain the highest average compensation, making them highly resilient to economic downturns.
3. **Market Consolidation:** A snapshot of the most recent data indicates heavy job market consolidation. The Government and Healthcare sectors alone account for over 35% of the tracked workforce, demonstrating consistent long-term growth regardless of short-term inflation volatility.

## 🎓 Acknowledgments
This project was developed as part of the rigorous curriculum provided by **Udacity**. The foundational scenario and local datasets were supplied by Udacity, while the data modeling, external FRED integration, DAX engineering, and dashboard architecture were independently developed.

## 👨‍💻 Author
**Abdullah Alshammari**
* Portfolio: [alshammari.dev](https://alshammari.dev)
* LinkedIn: [Abdullah Alshammari](https://www.linkedin.com/in/abdullah-alshammari-0983843a8/)

## Data sources and coverage

The two halves of this model have **different coverage**, and keeping them
apart is the single most important thing when reading any figure from it.

| Data | Coverage | Source |
| --- | --- | --- |
| Inflation, consumer prices for the United States | **Annual, 1960 to 2024** | FRED series [`FPCPITOTLZGUSA`](https://fred.stlouisfed.org/series/FPCPITOTLZGUSA), annual percentage, not seasonally adjusted. Original source: World Bank, retrieved through FRED. |
| Industry earnings | **Four snapshot years: 1990, 2000, 2010, 2020** | `Datasets/Industry Earnings.xlsx` |
| Jobs by industry | Annual series | `Datasets/` |
| Supporting series | Various | US Bureau of Labor Statistics extracts, `Datasets/Historical Population.xlsx` |

Any statement placing a sector next to an inflation rate is anchored to one of
the four earnings snapshot years. There is no annual industry **earnings**
series behind it, and four points must not be read as a line drawn through
sixty-five.

## Limitations

- **Descriptive, not causal.** Two series moving together is not evidence that
  one drove the other.
- Nominal and inflation-adjusted values are different things. Any comparison
  across periods should state which it is using.
- Sector averages are sensitive to workforce composition, which changes over
  the period. A shift in who is employed moves an average with nobody
  receiving a raise.
- **United States only.** The inflation series is a national aggregate and says
  nothing about how prices moved for any particular household.
- FRED revises its series. Figures here reflect the vintage at the time the
  model was built.

## Case study

A full write-up: the business question, the method, the evidence, and what the
result does not support.

<https://alshammari.dev/projects/income-inflation-purchasing-power/>

## License

MIT. See [LICENSE](LICENSE).
