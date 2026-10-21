# A/B Testing: Marketing Campaigns

Analysis of Facebook Ads and AdWords campaign performance using daily campaign data from 2019. The notebook explores campaign metrics, conversion patterns, hypothesis testing, regression, and time-based trends.

## Project contents

- `ab-testing-marketing-campaigns.ipynb` — Jupyter notebook with the analysis and visualizations.
- `marketing_campaign.csv` — daily marketing campaign dataset used by the notebook.
- `requirements.txt` — Python packages needed to run the notebook.

## Questions explored

- How do clicks and conversions compare between Facebook and AdWords?
- Are higher click counts associated with more conversions?
- Is the difference in average conversions statistically significant?
- Can Facebook conversions be estimated from click counts using linear regression?
- How do Facebook campaign conversions and cost metrics vary over time?
- Is there evidence of a long-term relationship between advertising cost and conversions?

## Getting started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd marketing-campaign-ab-testing
```

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
# macOS/Linux
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

```bash
jupyter notebook ab-testing-marketing-campaigns.ipynb
```

Keep `marketing_campaign.csv` in the same directory as the notebook so the relative file path works.

## Methods and libraries

The notebook uses pandas and NumPy for data handling, Matplotlib and Seaborn for charts, SciPy for statistical testing, and scikit-learn and statsmodels for regression and time-series analysis.

## Notes

The notebook's written interpretations reflect its original analysis. Statistical results describe this dataset and should not automatically be treated as proof that one platform will perform better in every future campaign.
