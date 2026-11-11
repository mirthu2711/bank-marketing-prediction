# Bank Term Deposit Prediction (PRCP-1000)

**Goal:** predict which customers will subscribe to a term deposit, so the marketing team can prioritise calls.

**Data:** 41,188 calls from a Portuguese bank (2008-2010), 20 features, 11.3% positive class.

**Approach:** EDA, cleaning (removed 12 duplicates, excluded `duration` to avoid leakage),
preprocessing pipeline (imputation, one-hot encoding, scaling), stratified 80/20 split,
comparison of four models: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting.

**Best model:** Gradient Boosting, ROC-AUC 0.809 on the test set (0.796 in 5-fold cross-validation).
At a threshold of 0.2: precision 0.48, recall 0.59, about 4x the random-call hit rate.

**Key findings:**
- Cellular contact converted at 14.7% vs 5.3% for telephone
- Customers with a previous successful campaign subscribed at 64.9%
- Students (30.5%) and retired customers (25.5%) subscribed most often

**Files:**
- `bank_marketing_analysis.ipynb`: full analysis
- `bank_marketing_analysis.html`: read-only copy of the notebook
- `bank-additional-full.csv`: dataset
- Problem statement PDF: project description and tasks
