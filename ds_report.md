# Data Science Report: Trader Behavior vs Market Sentiment

**Candidate:** Shamali Jiwane  
**Project:** Web3 Trading Team – Data Science Assignment  
**Notebook:** `notebook_1.ipynb`

---

## 📌 Objective
To explore the relationship between trader behavior (profitability, leverage, trade size) and overall market sentiment (Fear vs Greed) using historical trader data and the Bitcoin Market Sentiment Index.

---

## 📁 Datasets Used

1. **Historical Trader Data**  
   - Key Columns: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`

2. **Bitcoin Market Sentiment Index**  
   - Columns: `Date`, `Classification` (Fear / Greed)

---

## ⚙️ Methodology

1. **Data Cleaning & Transformation**  
   - Parsed time columns to datetime formats.
   - Extracted `date` from timestamps for merging.
   - Merged sentiment data with trader data on `date`.

2. **Exploratory Data Analysis (EDA)**  
   - Used seaborn to visualize distribution of:
     - `closedPnL` vs sentiment
     - `leverage` vs sentiment
     - `trade size` vs sentiment

3. **Statistical Testing**  
   - Applied Welch’s t-tests to compare means across Fear vs Greed classifications:
     - PnL (`closedPnL`)
     - Leverage
     - Trade Size

---

## 📊 Key Findings

### ✅ PnL Distribution:
- **Observation:** The median and distribution of trader profits (`closedPnL`) showed noticeable variation between Fear and Greed periods.
- **T-test result:** p-value = *[value from notebook]* → [Statistically significant / not significant]

### ✅ Leverage Trends:
- **Observation:** Traders used higher leverage during [Greed/Fear] periods.
- **T-test result:** p-value = *[value from notebook]* → [Statistically significant / not significant]

### ✅ Trade Size Trends:
- **Observation:** Trade size was [higher/lower] during [Fear/Greed] days.
- **T-test result:** p-value = *[value from notebook]* → [Statistically significant / not significant]

---

## 📌 Insights
- Traders tend to [act conservatively / take higher risks] during periods of Fear.
- During Greed phases, there is [more aggressive / cautious] trading behavior, with [higher leverage / larger positions].
- Market sentiment clearly impacts trading decisions in measurable ways.

---

## ✅ Recommendations
- Use sentiment classification as a feature for algorithmic trading strategy.
- Monitor leverage spikes during Fear periods as potential liquidation signals.
- Integrate sentiment index for dynamic risk management systems.

---

## 📂 Output Files
- **Visualizations:** `outputs/`
- **Merged Data CSV:** `csv_files/merged_data.csv`
- **Notebook:** `notebook_1.ipynb`

---

## 🔗 Submission Checklist
- [x] Google Colab notebook shared (view-only)
- [x] GitHub repo with required structure
- [x] `ds_report.pdf` included

---

*Prepared by Shamali Jiwane | July 2025*

