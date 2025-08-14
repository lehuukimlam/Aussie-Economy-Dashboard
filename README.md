
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

*(To be completed once final Power BI design is in place)*

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

