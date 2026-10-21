# Marketing Campaign A/B Testing

**A Python-based analysis of Facebook Ads and Google AdWords campaign performance using daily marketing data from 2019.**

This project explores which advertising channel generated more conversions in the supplied dataset, how clicks relate to conversions, and how Facebook campaign results changed over time. It combines exploratory data analysis, visualisation, statistical hypothesis testing, and a simple linear regression model.

> **Scope:** This is an analysis of the supplied historical dataset, not a controlled randomised experiment. The findings should not be treated as proof that one platform will always outperform the other.

## Project highlights

- Compare daily clicks and conversions for Facebook Ads and AdWords.
- Explore the distribution and frequency of conversion levels.
- Measure the relationship between clicks and conversions using correlation.
- Test the difference in average daily conversions with a Welch two-sample t-test.
- Fit a simple linear regression model to estimate Facebook conversions from clicks.
- Explore monthly and weekly Facebook conversion patterns and a cost-per-conversion trend.

## Key findings in this dataset

| Metric | Facebook Ads | AdWords |
|---|---:|---:|
| Total conversions across 2019 | 4,286 | 2,183 |
| Average conversions per day | 11.74 | 5.98 |
| Total clicks across 2019 | 16,078 | 22,040 |
| Correlation: daily clicks vs. conversions | 0.87 | 0.45 |

The notebook reports a statistically significant difference in average daily conversions, with Facebook higher in this dataset. Correlation describes association, not causation; other campaign differences may also affect results.

## Visual overview

### Average daily conversions

![Average daily conversions by platform](assets/average-daily-conversions.png)

### Daily clicks and conversions

![Scatter plots of clicks and conversions for Facebook and AdWords](assets/clicks-vs-conversions.png)

### Facebook conversions over the year

![Facebook monthly conversions in 2019](assets/facebook-monthly-conversions.png)

## Dataset

The file `marketing_campaign.csv` contains **365 daily records** covering 1 January to 31 December 2019. It includes fields for both campaigns, such as:

- Date and campaign identifier
- Ad views, clicks, and conversions
- Campaign cost
- Click-through rate (CTR)
- Conversion rate
- Cost per click (CPC)

The notebook reads the CSV using a relative path, so keep the CSV in the same folder as the notebook when running it.

## Methods used

1. **Data preparation:** load the CSV, parse dates, inspect column types and descriptive statistics, and convert currency/percentage fields for time-based analysis.
2. **Exploratory analysis:** histograms, conversion-category counts, bar charts, and scatter plots.
3. **Correlation analysis:** compare the relationship between daily clicks and conversions for each platform.
4. **Hypothesis testing:** compare mean daily conversions using an independent two-sample t-test with unequal variances (Welch's t-test). The notebook uses a 5% significance threshold.
5. **Regression:** use scikit-learn's `LinearRegression` to model Facebook conversions from Facebook clicks and report R² and mean squared error.
6. **Time-based analysis:** examine Facebook conversions by weekday and month, calculate a monthly cost-per-conversion measure, and run a cointegration test.

## Repository contents

- `AB Testing (Marketing Campaigns).ipynb` — the analysis notebook, including code, visualisations, and written interpretations.
- `marketing_campaign.csv` — the dataset used by the notebook.
- `assets/` — chart images displayed in this README.

## View the project

You can inspect the notebook and chart images directly in the GitHub repository using the file preview. **No cloning instructions are included here.**

## Run the notebook (optional)

If you choose to execute the notebook locally, you will need Python and the libraries imported by the notebook: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`, `statsmodels`, and Jupyter.

The notebook can be opened in Jupyter Notebook or JupyterLab. The CSV should remain beside the notebook because the notebook loads it with the relative path `marketing_campaign.csv`.

## Limitations and interpretation

- The dataset covers one year and may not represent current campaign performance.
- The analysis does not establish that the ad platform alone caused the observed difference.
- The notebook's regression uses the same dataset for fitting and evaluation; its reported R² is not a measure of out-of-sample predictive performance.
- The results depend on the quality and definitions of the supplied data.
- Cost and conversion metrics should be checked carefully before making budget decisions.

## Author's note

This project demonstrates a practical workflow for marketing analytics with Python: exploring data, visualising patterns, testing a hypothesis, and communicating results with appropriate caveats.
