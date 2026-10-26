# Data Science Case Studies

A collection of two hands-on Python projects demonstrating **exploratory data analysis (EDA), statistical analysis, predictive modelling, and unsupervised machine learning** using Jupyter Notebooks.

## Projects

### 1. Wine Quality Assessment

**Notebook:** [`Wine_Quality_Case_Study(2).ipynb`](Wine_Quality_Case_Study(2).ipynb)

**Objective:** Explore how physicochemical properties relate to wine quality and assess how accurately a multiple linear regression model can predict sensory quality scores.

**What the notebook covers:**
- Combining the red and white Vinho Verde wine datasets (6,497 records).
- Descriptive statistics: mean, median, mode, standard deviation, skewness, and coefficient of variation.
- EDA using quality distributions, box plots, and a correlation heatmap.
- Pearson and Spearman correlation analysis.
- Multiple linear regression with an 80/20 train–test split.
- Model evaluation using MAE, MSE, RMSE, and R².
- Standardised coefficients, multicollinearity (VIF), and red-versus-white robustness checks.
- Business interpretation and limitations of automated quality prediction.

**Key finding:** Alcohol content shows the strongest positive individual correlation with quality. The pooled linear model has a test-set R² of approximately **0.26**, making it more useful for preliminary screening than as a replacement for expert tasting.

### 2. EastWest Airlines Customer Segmentation

**Notebook:** [`EastWest_Airlines_Clustering(3).ipynb`](EastWest_Airlines_Clustering(3).ipynb)

**Objective:** Group frequent-flyer customers based on mileage, rewards, credit-card activity, and travel behaviour to support targeted marketing decisions.

**What the notebook covers:**
- Data inspection and preprocessing of 3,999 customer records.
- Missing-value and duplicate checks, extreme-outlier handling, and feature standardisation.
- EDA, correlation analysis, and two-dimensional PCA visualisation.
- **K-Means** clustering with elbow and silhouette analysis.
- **Hierarchical clustering** with dendrograms and linkage-method comparisons.
- **DBSCAN** with neighbourhood-distance analysis and parameter search.
- Comparison using silhouette, Davies–Bouldin, and Calinski–Harabasz scores.
- Customer cluster profiles and marketing recommendations.

**Key finding:** The notebook recommends **K-Means with three clusters** for interpretable customer segmentation, while using DBSCAN to help identify unusual customer patterns. The major customer groups reflect low engagement, card/bonus-driven loyalty, and frequent flying.

## Tools and Libraries

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Data analysis:** NumPy, Pandas, SciPy
- **Visualisation:** Matplotlib, Seaborn
- **Machine learning:** Scikit-learn
- **Statistical modelling:** Statsmodels

## Repository Structure

```text
Data-Science-Case-Studies/
├── README.md
├── Wine_Quality_Case_Study(2).ipynb
└── EastWest_Airlines_Clustering(3).ipynb
```

> This repository intentionally contains only the two notebooks and this README. The input datasets are not included.

## Running the Notebooks Locally

1. Clone or download this repository.
2. Install the required packages:

   ```bash
   pip install notebook numpy pandas matplotlib seaborn scipy scikit-learn statsmodels openpyxl
   ```

3. Obtain the input datasets and place them **in the same folder as the notebooks**:

   | Notebook | Required dataset files |
   | --- | --- |
   | Wine Quality Assessment | `winequality-red.csv`, `winequality-white.csv` |
   | EastWest Airlines Customer Segmentation | `EastWestAirlines.xlsx` (with a sheet named `data`) |

   The wine data corresponds to the **UCI Wine Quality** dataset. The airline notebook expects the **EastWest Airlines** sample workbook. These files must be supplied separately.

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open either notebook and run its cells in order.

## Concepts Demonstrated

`EDA` · `Statistical Analysis` · `Data Visualisation` · `Linear Regression` · `Model Evaluation` · `Feature Scaling` · `PCA` · `K-Means` · `Hierarchical Clustering` · `DBSCAN` · `Customer Segmentation`

## Note

These case studies are educational analyses. Their findings are specific to the datasets, model choices, and preprocessing steps documented in the notebooks.
