# **Analyzing the Impact of Macroeconomic Indicators on Nifty50 Using Granger Causality**

## Table of Contents
1. [Project Overview](#project-overview)
2. [What is Granger Causality?](#what-is-granger-causality)
3. [Repository Structure](#repository-structure)
   - [Data](#data)
   - [Results](#results)
   - [Scripts](#scripts)
   - [Other Files](#other-files)
4. [Methodology](#methodology)
5. [Key Findings](#key-findings)
   - [Granger Causality F-Test Values by Lag](#granger-causality-f-test-values-by-lag)
   - [India vs China: S&P 500 Influence](#india-vs-china-s-p-500-influence)
6. [Implications](#implications)
7. [Future Work](#future-work)
8. [How to Run the Project](#how-to-run-the-project)
9. [License](#license)

---

## Project Overview
This project explores the relationship between macroeconomic indicators and the Nifty50 index using **Granger Causality tests**. The goal is to identify the extent to which global factors like the **S&P 500**, **USD/INR exchange rate**, and **Crude Oil Prices** influence the Nifty50 index and how these relationships compare with the influence on China's **CSI300** index.

---

## What is Granger Causality?
The **Granger Causality Test** is a statistical hypothesis test for determining whether one time series can predict another. It evaluates whether the lagged values of one variable provide statistically significant information about the future values of another variable. In this project, we use Granger causality to assess the predictive influence of macroeconomic indicators (e.g., S&P 500, USD/INR) on Nifty50 and compare these relationships with China's CSI300 index.

---

## Repository Structure
The repository is organized as follows:

### **Data**
- `Data/macrodata.csv` *(Hidden in the public repository)*: Contains macroeconomic indicator data such as USD/INR, Crude Oil Prices, and S&P 500.
- `Data/nifty50_data.csv` *(Hidden in the public repository)*: Historical Nifty50 data from 2007 to 2024.

### **Results**
- `correlation_heatmap.png`: Heatmap visualizing correlations between Nifty50, macroeconomic indicators, and global indices.
- `granger_causality_macro_ec.png`: Plot showing Granger causality F-test values for Nifty50 and macroeconomic indicators.
- `india_china_comparison.png`: Bar chart comparing the influence of S&P 500 on India (Nifty50) and China (CSI300).
- `results.html`: Interactive HTML file summarizing key results and visualizations.

### **Scripts**
- `analysis.ipynb`: Jupyter Notebook containing the complete analysis, from data preprocessing to Granger Causality tests and visualizations.

### **Other Files**
- `.gitignore`: Configured to hide sensitive dataset files from the public repository.
- `LICENSE`: License details for the repository.
- `README.md`: Project documentation (this file).

---

## Methodology
1. **Data Collection:**
   - Data was collected for key macroeconomic indicators and indices, including USD/INR, Crude Oil Prices, S&P 500, Nifty50, and CSI300.

2. **Exploratory Data Analysis:**
   - Generated a correlation heatmap to understand relationships between variables.

3. **Granger Causality Tests:**
   - Conducted Granger Causality tests to quantify the influence of macroeconomic indicators on Nifty50.
   - Compared the influence of S&P 500 on Nifty50 and CSI300 across multiple lags.

4. **Visualizations:**
   - Plotted Granger causality F-test values to highlight key relationships.
   - Created comparative visualizations to contrast the impact on India and China.

---

## Key Findings
### Granger Causality F-Test Values by Lag
- **S&P 500** has the most significant impact on Nifty50, with high F-test values, particularly at lag 2 (~175).
- **Crude Oil Price** and **USD/INR** show weaker but statistically significant influences.

### India vs China: S&P 500 Influence
- **Nifty50 (India)** exhibits a strong dependency on the S&P 500, with significantly higher F-test values across all lags.
- **CSI300 (China)** shows weaker Granger causality, highlighting its relative independence from global indices.

---

## Implications
- **For Investors:**
  - Monitoring global indices like the **S&P 500** is critical for understanding and predicting Nifty50 movements.
  - A localized strategy may be more effective for investing in China.

- **For Policymakers:**
  - India's strong dependency on global factors highlights vulnerability to external shocks, necessitating robust economic policies to mitigate risks.

---

## Future Work
1. **Advanced Modeling:**
   - Apply advanced time-series models (e.g., VAR, SARIMA) to validate findings.

2. **Additional Indicators:**
   - Include more macroeconomic variables, such as inflation and interest rates.

3. **Temporal Analysis:**
   - Analyze the stability of these relationships across different time periods (e.g., pre- and post-pandemic).

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory and open the Jupyter Notebook:
   ```bash
   jupyter notebook Scripts/analysis.ipynb
   ```
3. Ensure the necessary libraries are installed by running:
   ```bash
   pip install -r requirements.txt
   ```
4. Replace the hidden data files (`macrodata.csv`, `nifty50_data.csv`) with your own datasets in the `Data` folder to reproduce the analysis.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
