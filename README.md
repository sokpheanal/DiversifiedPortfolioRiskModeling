# Diversified Portfolio Risk Modeling and Optimization

This repository contains the analysis, code, and results from the research paper *"Risk Modeling and Optimization of a Diversified Portfolio: Financial Services, Technology, and Real Estate Sectors."* 
The study explores quantitative portfolio management strategies, focusing on equally weighted and risk-parity approaches, and evaluates the performance of different sectors: Technology, Financial Services, and Real Estate.

The main methodologies employed include:

- **Markowitz Mean-Variance Optimization**
- **Extreme Value Theory (EVT) for tail risk analysis**
- **ARIMA models for return forecasting**
- **Generalized Hyperbolic (GHYP) and Normal Inverse Gaussian (NIG) distributions for return modeling**

This work demonstrates how portfolio optimization techniques can be applied to build a diversified and resilient portfolio across multiple sectors.

## Contents

- **Methods:** Details of the quantitative models, including Markowitz Mean-Variance Optimization, ARIMA modeling, and EVT analysis.
- **Data Analytics Plan:** Describes the data manipulation, return calculations, and risk assessments.
- **Results:** A comparative analysis of portfolio strategies, sector correlations, and tail risk evaluations.
- **Discussion & Conclusion:** Interpretation of the findings and practical implications for portfolio management.
- **Future Directions:** Suggestions for improving the model with machine learning and multi-factor models.

## Data

The analysis focuses on six securities representing three sectors:

- **Financial Services:** JPMorgan Chase & Co. (JPM), Goldman Sachs Group, Inc. (GS)
- **Technology:** Amazon.com, Inc. (AMZN), NVIDIA Corporation (NVDA)
- **Real Estate:** Crown Castle Inc. (CCI), American Tower Corporation (AMT)

The stock data is sourced using the `quantmod` package in R, and returns are calculated from the adjusted closing prices.

## Tools & Packages Used

- **R Tools:** 
  - `quantmod`, `xts`, `forecast`, `quadprog` for portfolio optimization and forecasting
  - `fExtremes`, `evir`, `ismev` for EVT analysis
  - `FRAPO`, `ghyp`, `fBasics` for fitting return distributions

## Key Results

- **Portfolio Strategies Comparison:** Equally weighted vs. risk-parity portfolios were evaluated, with the equally weighted strategy slightly outperforming the risk-parity strategy in cumulative returns.
- **Tail Risk Assessment:** Extreme Value Theory (EVT) showed that the Technology sector had the highest tail risk, making it more susceptible to extreme losses.
- **ARIMA Forecasting:** Forecast accuracy varied across sectors, with Financial Services showing the most predictable returns.
- **Optimization Results:** Using Markowitz mean-variance optimization, Real Estate received the highest allocation in the optimized portfolio due to its lower risk.

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Diversified-Portfolio-Risk-Modeling.git
    ```

2. Install the required R packages:
    ```R
    install.packages(c("quantmod", "xts", "forecast", "quadprog", "fExtremes", "evir", "ismev", "FRAPO", "ghyp", "fBasics"))
    ```

3. Run the R scripts to reproduce the analysis:
    - `portfolio_optimization.R`: Runs the portfolio optimization using mean-variance methods.
    - `risk_analysis.R`: Analyzes the risk and tail risk using EVT.
    - `forecasting.R`: Performs ARIMA forecasting for the individual securities.

## Future Work

Future research directions include the incorporation of advanced machine learning models for return forecasting.
In addition, dynamic portfolio re-balancing, where the portfolio is continuously adjusted based on real-time data, can also be explored.
Lastly, future studies could assess the performance of sustainable and ESG (Environmental, Social, and Governance) investments in these sectors.
