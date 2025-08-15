
## 📊 Power BI Dashboard Overview

This Power BI report visualizes key Australian economic and industry indicators using three main pages. The dashboard is fully interactive, with filters and dynamic visuals designed to support exploratory analysis.

---

### 📁 Pages & Visuals

#### 1. **Macro Page**
- **KPI Cards**: GDP, GDP per Capita, CPI, Unemployment Rate, Trade Imbalance — each includes Year-over-Year % change.
- **Economy Status Card**: Auto-generated label indicating economic state (e.g., Peak, Mixed, Recession).
- **Line Charts**: Time series for each indicator.
- **Filters**:
  - **Year Selector (Dropdown)**: Choose a specific year for snapshot analysis.
  - **Date Range Slider**: Analyze indicator trends across a multi-year period.

---

#### 2. **Cities and States Page**
- **Bar Charts**:
  - GDP by State
  - GDP per Capita by State
  - Employment-to-Population Ratio by State
  - CPI by City
- **Treemaps**:
  - GDP by Industry Sector (State level)
  - Employment by Industry (State level)
- **Map Visual**:
  - Interactive geographic view based on state and city-level indicators.
- **Filters**:
  - **Year Selector** (affects all visuals on page)

---

#### 3. **Correlation Matrix Page**
- **Correlation Table**:
  - Shows Pearson correlation coefficients among all macro indicators.
- **Paired Scatter Plots**:
  - Interactive scatter plots for selected variable pairs.

---

### 🧭 Notes on Interactivity
- Filters are limited to **year** only due to the data model structure.
- Industry and location dimensions are displayed separately; there is no cross-filtering between state and industry or city and industry.
