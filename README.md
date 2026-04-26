# ACC102-ROEESG Analysis Project
## Project Title
Correlation Analysis Between Long-term Corporate Profitability and ESG Performance of Chinese A-share Listed Companies

---

## 1. Problem & User
In recent years, ESG (Environmental, Social and Governance) has become a core evaluation dimension for global sustainable investment. This project aims to quantify and examine the actual linkage between a company’s historical long-term profitability and its ESG comprehensive performance.

The analytical conclusions and visualized results can serve as reliable decision support for individual and institutional investors, corporate management teams, and academic sustainability research practitioners.

---

## 2. Data
- **Financial Profitability Dataset**: Sourced from the CSMAR database library under WRDS (Wharton Research Data Services), officially accessed in April 2026. Core raw fields include annual net income and total shareholder's equity, based on which the Return on Equity (ROE) indicator is manually computed.Notably, all annual ROE calculations are strictly based on audited December fiscal year-end annual reports of A-share listed companies, maintaining a unified accounting caliber throughout the whole time window. The 5-year average ROE is constructed to represent long-term profitability.
- **ESG Rating Dataset**: Extracted as an Excel export file directly from the Wind Financial Terminal, accessed in April 2026. Contains full 2025 overall ESG rating score, as well as segmented Environmental (E), Social (S) and Governance (G) pillar sub-scores.

- **Sample Scale**: Starting from over 29,000 raw firm-year observations, after aggregation, All datasets are merged on unique company identification codes for one-to-one matching. Missing values are eliminated and 1% winsorization is applied to remove extreme outliers, ensuring the accuracy and validity of subsequent statistical analysis.The final valid research sample covers more than 5,000 unique A-share listed enterprises.

---

## 3. Methods
1. Raw dataset importing, structure inspection and preliminary data validation
2. Professional financial indicator construction: ROE is accurately calculated following the standard formula: ROE = Net Income / Total Shareholder Equity
3. Firm-level longitudinal aggregation: compute the stable 5-year average ROE (2020–2024) to eliminate annual performance noise and short-term operational fluctuations
4. Data standardization: unify stock security codes and calendar year formats across two independent databases to achieve precise one-to-one record matching
5. Data preprocessing: conduct 1% winsorization to mitigate the interference of extreme outliers, and systematically remove incomplete missing-value records
6. Statistical analysis: implement Pearson correlation coefficient calculation, two-tailed significance testing, and Spearman rank correlation robustness verification
7. Academic data visualization: construct 7 standardized analytical charts, including ROE distribution histogram, regression scatter plot, ESG tiered group boxplot, violin plot, pillar correlation bar chart, and pairwise correlation heatmap matrix
8. Time matching logic:match 2025 cross-sectional ESG ratings with the average realized ROE over the preceding 5-year window (2020–2024). 
This configuration smooths idiosyncratic yearly profit shocks, reflects persistent long-term profitability performance, and allows us to examine the ex-post profitability characteristics of currently high/low ESG-rated firms.
---

## 4. Key Findings
- The overall Pearson correlation coefficient between a firm's 5-year average ROE and its total ESG score is measured at r ≈ 0.043, reaching a high statistical significance level (p < 0.001)
- While statistically significant, the magnitude of the positive linkage is economically extremely weak, proving ESG performance barely explains the variation in long-term corporate profitability
- Subgroup comparison confirms that enterprises with superior high ESG performance show negligible profitability gaps relative to low ESG counterparts
- Among the three individual ESG pillars, the Environmental (E) dimension demonstrates the strongest relative correlation with long-term firm profitability
- There exists a strong positive internal correlation across E/S/G sub-dimensions, indicating that ESG construction develops holistically rather than independently in Chinese listed firms
- Spearman rank robustness test further validates that the weak positive relationship remains stable regardless of linearity assumptions

---

## 5. How to Run
1. Download the complete Jupyter Notebook (Python_Notebook_ROEESG.ipynb) file from this GitHub repository
2. Open and run the file within a standard Jupyter Notebook/Lab environment or VS Code, with Python and required data analysis libraries installed (pandas, numpy, matplotlib, seaborn, openpyxl)
3.The required ESG data file has been included in the attachment folder together with the code, users can run the entire project directly without changing any file paths.
4. Execute all code cells sequentially from top to bottom to fully reproduce the entire data cleaning process, statistical test outputs, and all high-resolution academic visualizations

---

## 6. Limitations & Next Steps
### Limitations
- This study confirms pairwise linear correlation only, and cannot establish strict causal inference between profitability and ESG performance
- Core firm characteristic control variables, including industry category, firm total size and capital structure, are not incorporated into the current baseline analysis
- The research adopts cross-sectional design only, without constructing multi-year panel data to observe dynamic long-term trends

### Next Steps for Improvement
- Introduce industry fixed effects and firm-level control variables to conduct multivariate regression and enhance result robustness
- Expand the dataset to multi-year panel ESG and financial data to track long-term dynamic changes
- Conduct grouped heterogeneity analysis to explore differing relationships across distinct industry sectors
