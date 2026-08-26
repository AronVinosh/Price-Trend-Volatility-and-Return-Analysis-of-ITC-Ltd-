# ITC Ltd — Price Trend, Volatility & Return Analysis (1996–2023)

MSc Financial Data Analytics — Case Study Assignment
Manipal Academy of Higher Education (MAHE), Bengaluru Campus

## Business Objective

To analyze the historical price trend, volatility, and return characteristics of ITC Ltd (NSE: ITC) stock over a 27-year period, in order to assess its risk-return profile and evaluate its suitability as a long-term investment.

## Dataset

- **Source:** Historical daily stock price data for ITC Ltd (ticker: ITC.NS)
- **Period:** January 1996 – May 2023
- **Records:** 6,890 daily observations
- **Columns:** Date, Open, High, Low, Close, Adj Close, Volume

## Project Structure

```
├── ITC.NS.csv                      # Raw dataset
├── itc_analysis.py                 # Full analysis script (or notebook version)
├── itc_analysis_output.csv         # Cleaned dataset with computed metrics
├── chart1_price_trend.png          # Closing price with 50/200-day moving averages
├── chart2_returns_distribution.png # Distribution of daily returns
├── chart3_rolling_volatility.png   # 30-day rolling volatility
├── ITC_Case_Study.docx             # Final written case study report
└── README.md
```

## Methodology

1. **Data Acquisition and Integrity** — Loaded raw price data, parsed dates (day-first format), sorted chronologically, checked for and forward-filled missing values, and confirmed no duplicate records.
2. **Descriptive Statistics** — Computed mean, median, standard deviation of closing price and daily returns; assessed skewness.
3. **Time Series Analysis** — Calculated 50-day and 200-day moving averages, year-over-year growth, and 30-day rolling volatility.
4. **Visualisation** — Produced three charts: price trend with moving averages, return distribution histogram, and rolling volatility over time.
5. **Limitations & Suggestions** — Identified gaps in the analysis (no fundamentals data, forward-fill assumptions, data ending before the 2024 hotels demerger) and proposed extensions (index benchmarking, fundamental ratios).

## Key Findings

| Metric | Value |
|---|---|
| Mean closing price | ₹121.43 |
| Median closing price | ₹72.62 |
| Std. deviation | ₹106.35 |
| Avg. daily return | 0.084% |
| Daily return std. dev | 2.057% |
| Approx. annualized return | 21.17% |
| Approx. annualized volatility | 32.66% |

## How to Run

```bash
pip install pandas numpy matplotlib openpyxl
python itc_analysis.py
```

Ensure `ITC.NS.csv` (or the `.xlsx` equivalent) is in the same directory, or update the file path in the script.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- openpyxl (if reading `.xlsx`)

## Author

[Your Name] — MSc Financial Data Analytics, MAHE Bengaluru

## Limitations

This analysis is based solely on market price data and does not include company fundamentals (revenue, profit, EBITDA). See the full case study report (`ITC_Case_Study.docx`) for a complete discussion of limitations and suggestions for further research.
