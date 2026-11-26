# Machine Learning Prediction of Daily Energy Consumption in a Full-Scale Wastewater Treatment Plant

CHE1147 Chemical Data Science and Engineering, University of Toronto, Fall 2026

Group: Athalia Beatrice Molianto, Kanishk Deshpande, Sadiyah Shafath

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aili01sky/CHE1147H-Group-Project/blob/main/02_Modelling.ipynb)

## Project overview
Wastewater treatment plants are among the most energy-intensive municipal facilities. This project uses daily data (January 2014 to June 2019) from the Melbourne Eastern Treatment Plant to predict daily energy consumption (MWh/day) with supervised machine learning.

## Repository map

| File | Contents |
|------|----------|
| `01_EDA.ipynb` | Exploratory data analysis: distributions, missing data, correlations, seasonality |
| `02_Modelling.ipynb` | Full ML pipeline: cleaning, feature engineering, baselines, Ridge / Random Forest / Gradient Boosting, tuning, evaluation, permutation importance, bootstrap uncertainty, SHAP |
| `Dataset_Fixed.csv` | Input dataset |
| `requirements.txt` | Python packages needed to run the notebooks |
| `results_table.csv` | Cross-validation and test metrics for all models (created by `02_Modelling.ipynb`) |
| `fig2_heatmap_small.png` | Correlation heat map (created by `01_EDA.ipynb`) |
| `fig_test_timeseries.png` | Actual vs predicted energy over the test period |
| `fig_parity.png` | Parity plots of Gradient Boosting (A) and Ridge (B) |
| `fig_permutation_importance.png` | Permutation importance of Random Forest (A), Gradient Boosting (A), Ridge (B) |
| `fig_uncertainty_ridgeB.png` | Bootstrap uncertainty of Ridge (B) |
| `fig_shap_gbA.png` | SHAP beeswarm of Gradient Boosting (A) |
| `fig_shap_waterfall.png` | SHAP waterfall for the highest predicted test day |

## Environment and how to run

**Option 1: Google Colab (no installation needed)**
1. Click the **Open in Colab** badge above (or open the notebook from GitHub in Colab).
2. Upload `Dataset_Fixed.csv` using the folder icon in the left sidebar.
3. Select **Runtime > Run all**. The notebook installs `shap` itself; all other packages are pre-installed in Colab.

**Option 2: Local computer**
1. Clone or download this repository.
2. Install the packages: `pip install -r requirements.txt`
3. Open the notebooks with Jupyter (`jupyter notebook`) and run `01_EDA.ipynb`, then `02_Modelling.ipynb`, from top to bottom.


## Data source
- Data: Kaggle "Full Scale Waste Water Treatment Plant Data" (d4rklucif3r); original source: https://data.mendeley.com/datasets/pprkvz3vbd/1
- Data originally published with:: F. Bagherzadeh, A. S. Nouri, M.-J. Mehrani and S. Thennadil, "Prediction of energy consumption and evaluation of affecting factors in a full-scale WWTP using a machine learning approach," *Process Safety and Environmental Protection*, vol. 154, pp. 458–466, 2021, doi: 10.1016/j.psep.2021.08.040.
