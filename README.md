# US Macroeconomic Analysis: Income vs. Inflation

## 📌 Project Overview
This Business Intelligence project analyzes the historical relationship between US inflation rates and industry-specific job growth and earnings. The goal is to identify which economic sectors demonstrate the highest resilience and growth during periods of high macroeconomic stress.

## 📊 Dashboard Preview
*(Note: You can view the full static dashboard in the `Dashboard_Preview.pdf` file).*

## 🛠️ Tech Stack & Skills Demonstrated
* **Tool:** Power BI
* **Data Modeling:** Star Schema architecture (1-to-Many relationships, customized central Date dimension).
* **DAX Implementation:** Engineered dynamic measures using `CALCULATE`, `FILTER`, `AVERAGE`, `MAX`, and `IF` logic to isolate sector performance during high-risk inflation periods (>4%).
* **Data Visualization:** Dual-axis charting, Top N dynamic filtering, and custom hierarchy mapping.

## 📂 Repository Structure
* `/data`: Contains raw historical datasets from the Federal Reserve Economic Data (FRED) and US Census.
* `US_Economic_Analysis.pbix`: The complete Power BI project file containing the data model and interactive visuals.
* `Dashboard_Preview.pdf`: A static export of the dashboard for quick viewing.

## 💡 Key Business Findings
1. **Purchasing Power Erosion:** While average industry income nominally increases over time, the dual-axis analysis reveals severe erosion of real purchasing power during inflation spikes (e.g., the 13.55% peak).
2. **Sector Resilience:** Filtering the data specifically for high-inflation years (>4%) shows that the Utilities and Management sectors maintain the highest average compensation, making them highly resilient to economic downturns.
3. **Market Consolidation:** A snapshot of the most recent data indicates heavy job market consolidation. The Government and Healthcare sectors alone account for a massive share of the workforce, demonstrating consistent long-term growth regardless of short-term inflation volatility.

## 👨‍💻 Author
**Abdullah Alshammari**
* Portfolio: [alshammarii.me](https://alshammarii.me)
* LinkedIn: [Insert Link Here]
