
# 🇦🇺 Australian Economic & Industry Trends Dashboard

This project builds an interactive Power BI dashboard supported by a transparent Python ETL pipeline to monitor Australia's macroeconomic performance. It uses public data from the ABS and RBA and is designed for analysts, policymakers, and researchers.

The project follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology to ensure a structured, iterative data science approach.

---
## Project Workflow
<img width="1357" height="518" alt="image" src="https://github.com/user-attachments/assets/af5be13f-9f8b-464d-94a6-70d5ecc8256d" />

## 📌 Framework: CRISP-DM

### 1. Business Understanding

The goal is to create a centralized, visual, and up-to-date view of Australia's economic health using key indicators:
- GDP (and per capita)
- Consumer Price Index (CPI)
- Unemployment Rate
- Interest Rate (Cash Rate)
- Exports & Imports (Trade Balance)
- Gross Value Added by Industry
- State-level performance

These indicators help stakeholders make informed decisions across economic, financial, and policy domains.

---

### 2. Data Understanding

**Primary Sources:**
- 📊 ABS (Australian Bureau of Statistics)
- 🏦 RBA (Reserve Bank of Australia)

Datasets include GDP, CPI, unemployment rate, interest rate, exports, imports, GVA, and state-level economic figures. All are publicly available and regularly updated.

---

### 3. Data Preparation

Python was used for ETL tasks in Google Colab:
- Cleaned raw ABS Excel/CSV files
- Reshaped tables to long-format fact tables
- Created dimension tables for indicators and locations
- Normalized date formats and handled missing values
- Saved outputs to `/cleaned_data/` for Power BI ingestion

Notebooks are organized in `/notebooks/` with one notebook per dataset.

---

### 4. Modeling

Data was modeled in Power BI using:
- Star schema with fact and dimension tables
- Time-series relationships for trend analysis
- Hierarchical filters (e.g., Year → Quarter → Month)
- Semantic formatting (units, KPIs, regional tags)

---

### 5. Evaluation

Each section of the Power BI dashboard supports the business goal of monitoring and understanding Australia’s economic trends across time and regions:

#### Macro Page
- **KPI Cards** display key national metrics (GDP, GDP per Capita, CPI, Trade Imbalance, Unemployment Rate), with YoY % change indicators to signal economic direction.
- **Economy Status Label** (e.g., Peak, Mixed, Recession) is algorithmically generated based on cash rate trends and macro deltas, offering a quick classification of economic conditions.
- **Single-Year Selection** enables users to assess the macroeconomic snapshot for a chosen year, supporting point-in-time decision-making.
- **Time Range Slider** facilitates multi-year trend analysis for identifying growth or contraction phases across indicators.

#### Cities & States Page
- **State-Level Bar Charts** allow comparisons across GDP, GDP per Capita, and Employment-to-Population Ratio to uncover disparities and regional strengths.
- **City-Level Charts** visualize CPI changes to reflect cost-of-living trends in urban areas.
- **Treemaps** categorize GDP by sector and Employment by industry, offering a breakdown of economic composition across geographies.

#### Correlation Matrix Page
- **Correlation Table** quantifies the statistical relationships among core macro indicators, assisting in hypothesis generation (e.g., does higher GDP align with lower unemployment?).
- **Scatter Plots** help users visually detect linear or inverse relationships between paired metrics, aiding both intuitive understanding and deeper data exploration.


---

### 6. Deployment

While public Power BI publishing isn't available due to license limits, the `.pbix` file and screenshots are provided in the [`/powerbi/`](./powerbi) folder for review.

---

## 📁 Project Structure

```
├── data/            # Raw ABS & RBA datasets
├── cleaned_data/    # Processed datasets (CSV)
├── notebooks/       # Python notebooks for cleaning and transformation
├── powerbi/         # Power BI file and visual screenshots
├── requirements.txt # Python dependencies
└── README.md        # Project overview (this file)
```

---

## 🛠 Tech Stack

- Python (Pandas, openpyxl)
- Power BI Desktop
- GitHub (for versioning & collaboration)
- Public data from ABS & RBA

---

## 🧠 Future Enhancements

- Automate ABS data pulls via web scraping or API
- Add forecasting models for GDP & CPI
- Deploy dashboard to Power BI service or embed in website
- Add interactive tooltips and drillthroughs

---

## 📄 License

MIT — feel free to fork, build, or contribute.




