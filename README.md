# 🌿 Analysing New Zealand's Economic and Carbon Trends (2010–2024)

> A data science project exploring the relationship between GDP growth and greenhouse gas emissions across New Zealand industries using real-world government data.

---

## 📋 Project Overview

This project investigates a core question in environmental economics:

**Does economic growth in New Zealand come at the cost of the environment?**

Using two official datasets from [Stats NZ](https://www.stats.govt.nz/), I merged GDP data with greenhouse gas emissions data across industries and engineered a custom **Carbon Intensity** metric (emissions per dollar earned) to compare industries fairly and track national trends over 15 years.

The analysis is presented as a professional, client-focused Jupyter Notebook report.

---

## 🔬 Research Questions

| # | Research Question |
|---|------------------|
| RQ1 | Which specific industry has the highest Carbon Intensity (emissions per dollar earned) in New Zealand? |
| RQ2 | Has New Zealand's national carbon intensity overall increased or decreased between 2010 and 2024? |
| RQ3 | Is there a direct linear relationship between an industry's economic growth (GDP) and its total greenhouse gas emissions? |
| RQ4 | When comparing economic value against environmental impact, which sectors are the most "green" or future-proof? |

---

## 📊 Key Findings

- ✅ **New Zealand is becoming more carbon efficient** — national carbon intensity has steadily decreased since 2010, even as the economy has grown.
- 🚜 **Agriculture is the major outlier** — it produces significantly more emissions per dollar of GDP than any other sector, far exceeding industries like Construction and Professional Services.
- 📉 **GDP and emissions are not directly linked** — a Pearson Correlation of **-0.005** shows there is almost no linear relationship between an industry's economic size and its emissions output.
- 🌱 **Services sectors are the most "green"** — industries like Professional Services generate high GDP while maintaining very low emissions.

---

## 🗂️ Datasets

| Dataset | Source | Description |
|--------|--------|-------------|
| Regional GDP by Industry | [Stats NZ](https://www.stats.govt.nz/assets/Uploads/Regional-gross-domestic-product/Regional-gross-domestic-product-Year-ended-March-2025/Download-data/regional-gross-domestic-product-year-ended-march-2025.csv) | GDP (NZD millions) by industry, year ended March 2025 |
| Greenhouse Gas Emissions by Industry | [Stats NZ](https://www.stats.govt.nz/assets/Uploads/Greenhouse-gas-emissions-industry-and-household/Greenhouse-gas-emissions-industry-and-household-September-2025-quarter/Download-data/greenhouse-gas-emissions-industry-and-household-september-2025-quarter.csv) | Greenhouse gas emissions (kilotonnes) by industry and household, Sep 2025 quarter |

> Both datasets are publicly available from Stats NZ and do not require authentication to access.

---

## 🛠️ Tools & Libraries

| Library | Purpose |
|--------|---------|
| `pandas` | Data wrangling, merging, groupby operations |
| `numpy` | Numerical calculations |
| `matplotlib` | Core charting and visualisation |
| `seaborn` | Enhanced chart styling and readability |
| `Jupyter Notebook` | Interactive report environment |

### Installation

```bash
pip install pandas numpy matplotlib seaborn notebook
```

---

## 📁 Project Structure

```
📦 nz-carbon-trends-analysis
 ┣ 📓 Project_1.ipynb        # Main analysis notebook (run this)
 ┣ 📄 README.md              # Project overview (you are here)
```

---

## 🚀 How to Run

1. **Clone this repository**
   ```bash
   git clone https://github.com/farbin/nz-carbon-trends-analysis.git
   cd nz-carbon-trends-analysis
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn notebook
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook Project_1.ipynb
   ```

4. **Run all cells** — the notebook fetches data directly from Stats NZ URLs, so an internet connection is required.

> 💡 All outputs are already embedded in the notebook, so you can also just read through it without running any code.

---

## 🔍 Methodology

### Data Wrangling
- Renamed non-standard column names for consistency using `rename()`
- Handled missing values using `dropna()`
- Used a mapping dictionary to standardise industry names across both datasets before merging
- Applied `groupby()` to aggregate sub-sector emissions into industry totals per year
- Validated data integrity using `.describe()`, `.unique()`, and `.duplicated()`

### Analysis Techniques
- **Ratio Analysis** — calculated Carbon Intensity (Emissions ÷ GDP) per industry per year
- **Time-Series Analysis** — tracked national carbon intensity from 2010 to 2024
- **Pearson Correlation** — tested for a linear relationship between GDP and emissions
- **Comparative Visual Analysis** — overlaid economic output against environmental impact across sectors

### Visualisations Used
- Bar charts (industry comparisons)
- Line graphs (trends over time)
- Scatter plots (GDP vs emissions correlation)
- Distribution plots (carbon intensity spread across industries)

---

## ⚠️ Limitations

- **Data aggregation** — broad categories like "Manufacturing" combine many sub-industries, which may hide individual outliers within those groups.
- **National averages** — a single Pearson Correlation across all industries does not capture sector-level nuance; each industry behaves differently.
- **Time lag** — government datasets may have a reporting delay, so the most recent data points should be interpreted with caution.

---

## 👤 Author

**Farbin Aziz**
Master of Information Sciences — Massey University (Te Kunenga ki Pūrehuroa), Auckland NZ
[LinkedIn](https://www.linkedin.com/in/farbin/) | farbin.aziz07@gmail.com

---

## 📌 Course

158.755 Data Science — Semester 1, 2026 | Massey University
