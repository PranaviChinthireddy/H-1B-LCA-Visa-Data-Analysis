# H-1B LCA Visa Data Analysis & Denial Prediction: 2020–2024

This project applies advanced data science to explore the U.S. H-1B visa landscape. Using over 3.5 million Labor Condition Application (LCA) records from 2020 to 2024, we identify key denial risk factors, forecast job demand, assess wage fairness, and uncover geographic approval patterns through machine learning and time-series modeling.

## 🔍 Project Goals

- **Forecast Job Market Trends**: Predict future demand for top SOC roles using SARIMA.
- **Predict Visa Denials**: Classify outcomes using employer reputation, job role, wage, and region.
- **Compare ML Models**: Evaluate Logistic Regression, Decision Tree, Random Forest, and XGBoost.
- **Assess Wage Fairness**: Compare offered vs prevailing wages and flag compliance risks.
- **Profile Geographic Risk**: Analyze cost of living and violent crime impact on approvals.
- **Track Post-COVID Shifts**: Identify changes in top H-1B sponsors and wage patterns.

## 🧠 Key Insights

- **Employer History Matters**: XGBoost revealed that “Willful Violator” status is the most influential factor in denials.
- **Wage Influences Risk**: A U-shaped relationship shows that both low and abnormally high wages increase denial likelihood.
- **Software & Data Roles Dominate**: Software Developers and BI Analysts remain the most in-demand H-1B roles.
- **Location Has an Impact**: Job offers in high-crime or high-cost ZIP codes show unique approval dynamics.
- **Forecasting Accuracy**: SARIMA achieved <15% MAPE when forecasting monthly job demand, confirming seasonal hiring trends.

## 📊 Data Sources

- **[H-1B LCA Disclosure Data (FY2020–2024) – Kaggle](https://www.kaggle.com/datasets/zongaobian/h1b-lca-disclosure-data-2020-2024)**  
  *(3.5M+ rows, 69 columns; includes employer, job, wage, location, and decision outcome data)*
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

## 📍 Strategic Recommendations

### For Job Seekers
- Target high-approval roles (e.g., Software Dev, BI Analyst)
- Avoid employers with a poor compliance history
- Choose locations with high wage-to-cost-of-living ratios

### For Employers
- Ensure wage offers exceed prevailing wage thresholds
- Avoid risky job descriptions or borderline roles
- Monitor denial trends by region and role

### For Policymakers
- Expand employer access beyond high-volume metro areas
- Promote wage transparency and cost-of-living indexing
- Use ML-driven forecasting to inform cap planning and audits

These findings support data-driven decision-making for job seekers, employers, and immigration analysts navigating the evolving U.S. labor market.
