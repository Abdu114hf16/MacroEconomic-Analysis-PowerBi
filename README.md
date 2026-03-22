# US Macroeconomic Analysis: Income vs. Inflation

## 📌 Project Overview
This Business Intelligence project is an end-to-end data analysis pipeline designed to uncover the historical relationship between US inflation rates and industry-specific job growth and earnings. The objective is to identify which economic sectors demonstrate the highest resilience during periods of severe macroeconomic stress.

## 🏗️ End-to-End Analysis Pipeline

### Phase 1: Data Ingestion & Integration
To simulate a real-world enterprise environment, data was extracted and consolidated from three disparate sources:
1. **Local Datasets:** Foundational census and industry data files.
2. **Cloud Storage:** Remote datasets ingested directly from a Microsoft Azure Blob Storage container.
3. **Web Extraction:** Historical Consumer Price Index (CPI) and inflation data extracted from the [Federal Reserve Economic Data (FRED) database](https://fred.stlouisfed.org/).

### Phase 2: Data Modeling & Transformation
* Processed raw data using Power Query to clean, format, and standardize column structures.
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
* Portfolio: [alshammarii.me](https://alshammarii.me)
* LinkedIn: [Abdullah Alshammari](https://www.linkedin.com/in/abdullah-alshammari-0983843a8/)
