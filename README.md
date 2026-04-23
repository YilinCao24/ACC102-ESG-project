# ACC102-ROE&ESG analysis-project
# Project Title
Correlation Analysis Between Long-term Corporate Profitability and ESG Performance of Chinese A-share Listed Companies

## 1. Problem & User
In recent years, ESG (Environmental, Social and Governance) has become a core evaluation dimension for global sustainable investment. This project aims to quantify and examine the actual linkage between a company’s historical long-term profitability and its ESG comprehensive performance.
The analytical conclusions and visualized results can serve as reliable decision support for individual and institutional investors, corporate management teams, and academic sustainability research practitioners.

## 2. Data
- **Financial Profitability Dataset**: Sourced from the **CSMAR database library under WRDS (Wharton Research Data Services)**, officially accessed in April 2026. Core raw fields include annual net income and total shareholder’s equity, based on which the Return on Equity (ROE) indicator is manually computed.
- **ESG Rating Dataset**: Extracted from the **Wind Financial Terminal**, accessed in April 2026. Contains full 2025 overall ESG rating score, as well as segmented Environmental (E), Social (S) and Governance (G) pillar sub-scores. 2025 ESG data is selected specifically due to its highest data integrity and coverage; pre-2024 ESG datasets suffer from extensive missing values and poor data quality.
- Sample scale: Starting from over 20,000 raw annual firm observations, after aggregation, matching and rigorous cleaning, the final valid research sample covers more than 5,000 unique A-share listed enterprises.

## 3. Methods
1. Raw dataset importing, structure inspection and preliminary data validation
2. Professional financial indicator construction: ROE is accurately calculated following the standard formula: *ROE = Net Income / Total Shareholder Equity*
3. Firm-level longitudinal aggregation: compute the stable 5-year average ROE (2020–2024) to eliminate annual performance noise and short-term operational fluctuations
4. Data standardization: unify stock security codes and calendar year formats across two independent databases to achieve precise one-to-one record matching
5. Data preprocessing: conduct 1% winsorization to mitigate the interference of extreme outliers, and systematically remove incomplete missing-value records
6. Statistical analysis: implement Pearson correlation coefficient calculation and two-tailed significance testing
7. Academic data visualization: construct three standardized analytical charts, including regression scatter plot, ESG tiered group boxplot, and pairwise correlation heatmap matrix

## 4. Key Findings
- The overall Pearson correlation coefficient between a firm’s 5-year average ROE and its total ESG score is measured at **r = 0.059**, reaching a high statistical significance level (p < 0.001)
- While statistically significant, the magnitude of the positive linkage is economically extremely weak, proving ESG performance barely explains the variation in long-term corporate profitability
- Subgroup comparison confirms that enterprises with superior high ESG performance show negligible profitability gaps relative to low ESG counterparts
- Among the three individual ESG pillars, the Environmental (E) dimension demonstrates the strongest relative correlation with long-term firm profitability
- There exists a strong positive internal correlation across E/S/G sub-dimensions, indicating that ESG construction develops holistically rather than independently in Chinese listed firms

## 5. How to run
1. Download the complete Jupyter Notebook (.ipynb) file from this GitHub repository
2. Open and run the file within a standard Jupyter Notebook/Lab environment or VS Code with Python and required data analysis libraries installed
3. Execute all code cells sequentially from top to bottom to fully reproduce the entire data cleaning process, statistical test outputs, and all high-resolution academic visualizations

## 6. Limitations & next steps
### Limitations
- This study confirms pairwise linear correlation only, and cannot establish strict causal inference between profitability and ESG performance
- Core firm characteristic control variables, including industry category, firm total size and capital structure, are not incorporated into the current baseline analysis
- The research adopts cross-sectional design only, without constructing multi-year panel data to observe dynamic long-term trends
### Next Steps for Improvement
- Introduce industry fixed effects and firm-level control variables to conduct multivariate regression and enhance result robustness
- Expand the dataset to multi-year panel ESG and financial data to track long-term dynamic changes
- Conduct grouped heterogeneity analysis to explore differing relationships across distinct industry sectors.
