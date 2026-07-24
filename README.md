# BMW Global Sales Analysis (2018-2025)

Analysis of the BMW Group's global sales performance between 2018 and 2025, covering sales volumes, model mix, the EV transition, pricing, and seasonality across four major regions. This is a portfolio project built as part of a transition into data analytics.

**Objective:** identify the key trends shaping the BMW Group's global performance between 2018 and 2025, and translate these findings into actionable recommendations around product, market, and commercial priorities.

## Project Structure

The project is organized as two Jupyter notebooks, meant to be read in order:

| Notebook | Purpose |
|---|---|
| `01_Data_Audit_Cleaning.ipynb` | Audit of the raw dataset (data types, invalid ranges, categorical inconsistencies, outliers), followed by cleaning and export to `bmw_data_cleaned.csv` |
| `02_Analysis.ipynb` | Analysis of the cleaned data across seven dimensions: global sales trend, region/model breakdown, EV vs thermal transition, premium share, revenue and pricing, macroeconomic factors, and seasonality |

## Key Findings

- Total sales grew by **+27.52%** and revenue by **+28.02%** over the period, with revenue slightly outpacing volume, consistent with a gradual shift toward premium, price-driven growth rather than volume-driven growth.
- The EV transition is real but uneven: the average EV share sits around **~25%**, but the overall progression is only **+2.2 percentage points** over the period. China is the only region where EV momentum is clearly accelerating.
- The model mix stays balanced by design (less than 4% separates the top and bottom sellers by volume), but the X3's growth (**+3%**) and the iX's growth (**+45%**) diverge sharply, suggesting a shift already under way within that balance.
- Seasonality is limited but culturally grounded: global monthly sales share fluctuates within a narrow 1.68 percentage point range, with regional peaks aligning with local patterns (China: post-Chinese New Year spending, Europe: year-end fleet renewals, Usa/Restofworld: June).
- Two macroeconomic variables in the dataset, `GDP_Growth` and `Fuel_Price_Index`, showed distributions inconsistent with real-world data and were excluded from the core analysis.

## Tech Stack

- **Python**: pandas
- **Visualization**: seaborn, matplotlib
- **Environment**: Jupyter Notebook

## Setup

```
pip install pandas seaborn matplotlib
```

## Data

The dataset is publicly available on Kaggle: [BMW Global Sales Analysis 2018-2025](https://www.kaggle.com/datasets/mohamedamiralkrdawy/bmw-global-sales-analysis-20182025). It covers the BMW Group (including the MINI nameplate) across four regions: China, Europe, Usa, and Restofworld.

- `bmw_global_sales_2018_2025.csv`: the original dataset as published on Kaggle
- `bmw_global_sales_DIRTY.csv`: a version with intentionally introduced data quality issues, used as the input for the audit and cleaning notebook
- `bmw_data_cleaned.csv`: the output of the cleaning notebook, used as the input for the analysis notebook
