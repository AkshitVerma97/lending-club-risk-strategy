# lending-club-risk-strategy
A quantitative investment strategy using Machine Learning to identify high-yield borrowers and target a 9-11% Net Annualized Return. (Python, Scikit-Learn, Financial Modeling)

# Lending Club Strategy: Mining "Safe" Bets in High-Risk Pools
[![View Business Plan](https://img.shields.io/badge/View-Business_Plan_PDF-blue?style=for-the-badge&logo=adobeacrobatreader)](docs/lending_club_business_plan.pdf)

> **Timeline:** Fall 2025
> **Role:** Group Project (Led Financial Modeling & Risk Analysis)
> **Tools:** Python (Pandas, Scikit-Learn), PowerPoint

---

## The Business Question
**"Can we capture the high yields of risky loans (Grades C, D, & E) while avoiding the defaults?"**

High-grade loans (Grade A) are safe but offer low returns (approx. 5-7%). Lower-grade loans offer high yields but come with significant default risks. The team's goal was to build a model that identifies the **"Hidden Gems"**- borrowers in these risky grades who are actually financially stable—to maximize the fund's spread.

---

## Key Insights

### 1. The "High-Yield" Strategy
Our analysis revealed that blindly investing in High-Yield loans leads to losses. However, by using our algorithm to **selectively filter borrowers within Grades C, D, and E**, we projected a **Net Annualized Return (NAR) of 9-11%**, significantly outperforming the passive investor average of 4-6%.

### 2. The "Data Gap" Reality
We tested Deep Learning (Neural Networks) and SVM classifiers against the industry baseline.
* **Our Result:** Test set AUROC of **0.689**.
* **Industry Baseline:** AUROC of **0.72**.
* **Critical Insight:** Our model underperformed the industry standard. This signals that standard borrower features (FICO, Loan Term) have reached a predictive ceiling. To beat the market, the fund must acquire **non-linear alternative data** (e.g., transactional behavior) rather than just tuning algorithms.

---

## Recommendations
*Based on the analysis, the team proposes:*

**1. Target Grades C, D, & E with Strict Filtering**
Shift capital allocation away from Grade A. Focus on the "risky" bands (C, D, E) where interest yields are highest, but enforce a strict algorithmic "Hurdle Rate" to reject borrowers with a high probability of charge-off.

**2. Pivot to Alternative Data Acquisition**
Since our Neural Network could not surpass the 0.72 industry baseline using standard credit data, we recommend allocating the $150k operational budget toward acquiring **alternative data sources** to better model complex borrower behaviors that credit scores miss.

---

## Technical Appendix
* **Data Handling:** Processed 1M+ rows; utilized imputation and class imbalance techniques (since defaults are rare) to prevent model bias.
* **Modeling:** Compared Linear Models (Baseline) vs. Support Vector Machines (SVM) and Neural Networks (Challenger).
* **Validation:** Rigorously tested against the most recent 10% of loans to simulate real-world deployment.

---

### [Read the Full Business Plan (PDF)](docs/lending_club_business_plan.pdf)
### [Full Presentation (PDF)](docs/lending_club_presentation_pdf.pdf)
### [Full Presentation (PPT)](docs/lending_club_ppt.pptx)
### [Python Notebook (ipynb)](lending_club_python.ipynb)
