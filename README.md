# H-1B LCA Visa Data Analysis & Denial Prediction (2020–2024)

This project explores the U.S. H-1B visa landscape through the lens of data science. By analyzing over 3.5 million Labor Condition Application (LCA) records filed between 2020 and 2024, we identify denial risk factors, forecast job demand, assess wage trends, and uncover location-based approval patterns using advanced machine learning and time-series models.

## 🔍 Project Goals

- **Forecast Job Market Trends**: Use SARIMA to predict demand for top SOC job titles over the next 24 months.
- **Predict Visa Denials**: Train ML models to classify visa outcomes based on employer reputation, job role, wages, and region.
- **Model Comparison**: Evaluate Logistic Regression, Decision Tree, Random Forest, and XGBoost for denial prediction accuracy.
- **Wage Fairness Analysis**: Compare offered wages to prevailing wages and detect compliance risks.
- **Geospatial & Economic Risk Profiling**: Analyze how cost of living and violent crime influence approval likelihood.
- **Post-COVID Employer Patterns**: Track how top H-1B sponsors and wage trends evolved before and after the pandemic.

## 🧠 Key Insights

- **Employer History Matters**: XGBoost revealed that “Willful Violator” status is the most influential factor in denials.
- **Wage Influences Risk**: A U-shaped relationship shows that both low and abnormally high wages increase denial likelihood.
- **Software & Data Roles Dominate**: Software Developers and BI Analysts remain the most in-demand H-1B roles.
- **Location Has an Impact**: Job offers in high-crime or high-cost ZIP codes show unique approval dynamics.
- **Forecasting Accuracy**: SARIMA achieved <15% MAPE when forecasting monthly job demand, confirming seasonal hiring trends.

## 📊 Data Sources

- **H-1B LCA Disclosure Data (FY2020–2024)** – Kaggle (3.5M+ rows, 69 columns)
- **Cost of Living by ZIP Code** – Merged by `worksite_postal_code`
- **Crime Statistics by ZIP Code** – U.S. national crime dataset

## 🛠️ Tools & Technologies

- **Languages**: Python (Pandas, NumPy, Scikit-learn)
- **Modeling**: Random Forest, XGBoost, SARIMA, Logistic Regression, Decision Tree
- **Balancing**: SMOTE, Random Undersampling
- **Visualization**: Seaborn, Matplotlib, Folium (interactive crime maps)
- **Data Handling**: Jupyter Notebooks, Google Colab
- **Deployment Ready Concepts**: Model interpretability (feature importance), forecasting with confidence intervals

## 🧩 Feature Engineering

- Employer behavior flags: `willful_violator`, `h_1b_dependent`
- Wage normalization & cost-of-living ratio
- Crime zone labeling (top 25% ZIPs by crime index)
- SOC group and NAICS sector mapping
- Derived job-level attributes: `log_wage`, `decision_duration`, `below_prevailing_flag`

## 🗺️ Interactive Maps

Created with Folium, our maps plot H-1B certified locations by ZIP code and overlay violent crime data, highlighting safety-related risks and regional employer density.

## 📌 Strategic Recommendations

- **For Job Seekers**: Target high-demand roles, ensure wage competitiveness, and vet employers with a strong approval history.
- **For Policymakers**: Enforce wage transparency, focus audits on flagged employers, and expand visa accessibility in non-coastal states.
- **For Analysts**: Incorporate regional economic indicators for more accurate predictions of visa adjudication trends.

## 🧪 Future Enhancements

- Use SHAP for model explainability.
- Apply SARIMAX with macroeconomic variables.
- Deploy real-time dashboards using Power BI or Tableau Public.
- Integrate APIs for live labor market data (e.g., BLS, USCIS updates).
