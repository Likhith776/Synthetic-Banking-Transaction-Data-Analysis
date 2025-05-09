# Synthetic Banking Transaction Data Analysis

This project involves a comprehensive exploratory data analysis (EDA) on a synthetic banking transaction dataset. The aim is to demonstrate skills in data wrangling, statistical hypothesis testing, visualization, and uncovering patterns related to financial fraud detection.

---

## Project Structure

.
├── data/
│   └── transactions.csv           # Synthetic dataset (1000 records)
├── notebooks/
│   └── analysis.ipynb             # Main Jupyter Notebook for EDA
├── visuals/
│   └── *.png                      # Saved plots and graphs
├── README.txt                     # Project documentation
└── requirements.txt               # Python dependencies

---

## Dataset Overview

The dataset contains 1,000 synthetic banking transactions, each with the following features:

- Transaction ID, Sender ID, Receiver ID
- Amount, Type (Transfer, Withdrawal, Deposit)
- Timestamp (1-hour window on Jan 17, 2025)
- Status (Success/Failure), Fraud Flag (0 or 1)
- Latitude, Longitude
- Device Type, Network Slice ID
- Network Latency, Bandwidth
- PIN Code (masked)

---

## Analysis Workflow

1. **Initial Analysis**
   - Loaded and inspected dataset structure.
   - Checked for missing values and inconsistencies.
   - Confirmed artificial data distribution (controlled noise).

2. **Preprocessing**
   - Converted timestamps into numeric form (minutes from baseline).
   - Validated feature distributions using histograms and boxplots.

3. **Geolocation Review**
   - Found uniform/engineered geolocation data.
   - No real-world mapping potential.

4. **Exploratory Data Analysis (EDA)**
   - Compared categorical features using boxplots and strip plots.
   - Found weak relationships between variables (e.g., Network Slice ID and Latency).

5. **Fraud Analysis**
   - Fraud data is evenly distributed.
   - Conducted:
     - Shapiro-Wilk Test for normality
     - Welch’s T-Test for mean difference
     - Mann-Whitney U Test for distribution differences
   - Found no significant relation between fraud and transaction amount.

6. **Categorical Feature Analysis**
   - Analyzed impact of Device Type, Transaction Type, and Status on fraud.
   - No categorical variable showed significant correlation with fraud.

7. **Temporal & Latency Trends**
   - Used bubble plots to examine fraud over time, latency, and bandwidth.
   - No visible trend or clustering.

8. **Correlation Testing**
   - Used Cramér’s V for categorical correlation.
   - All values < 0.07 — no meaningful associations.
   - Continuous variables also weakly correlated.

9. **Feature Engineering Observations**
   - Highlighted the need for engineered/derived features (e.g., behavioral aggregation).
   - Suggested multivariate modeling over single-variable analysis.

---

## Key Insights

- Dataset is clean, uniformly distributed, and artificially generated.
- No single feature strongly predicts fraud.
- Advanced modeling or engineered features likely required for real fraud detection.
- Project illustrates robust statistical thinking and EDA workflow.

---

## Requirements

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels

Install via:

pip install -r requirements.txt

---

## License

This project is open for academic and educational purposes. The dataset is synthetic and contains no real-world personal or financial data.


