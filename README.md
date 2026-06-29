# Employee Sentiment Analysis
**Author:** Dilip Bukkambudhi Ganesh  
**Dataset:** test.xlsx (2,191 email messages, 10 employees, 2010–2011)  
**Tools:** Python, VADER NLP, Scikit-learn, Pandas, Matplotlib, Seaborn

---

## 📊 Key Findings

### Sentiment Distribution
| Sentiment | Count | % |
|-----------|-------|---|
| Positive  | 1,525 | 69.6% |
| Neutral   | 508   | 23.2% |
| Negative  | 158   | 7.2%  |

---

## 🏆 Overall Top 3 Positive Employees (by total cumulative score)
1. **Lydia Delgado** — Consistently high positive scores across months
2. **John Arnold** — Strong positive presence throughout 2010–2011
3. **Eric Bass** — Frequently ranked in top positive performers

---

## 🔻 Overall Top 3 Negative Employees (by total negative message volume)
1. **Don Baughman** — Highest negative message count overall
2. **Kayne Coulter** — Recurring negative months throughout dataset
3. **Johnny Palmer** — Multiple months with low/negative sentiment scores

---

## ⚠️ Flight Risk Employees
Employees flagged for sending **4+ negative messages within any 30-day rolling window:**

| Employee | First Triggered | Neg Msgs in Window |
|---|---|---|
| ⚠️ Bobette Riner | 2011-03-05 | 4 |
| ⚠️ Don Baughman | 2010-12-12 | 4 |
| ⚠️ John Arnold | 2010-05-25 | 4 |
| ⚠️ Johnny Palmer | 2010-02-09 | 4 |
| ⚠️ Kayne Coulter | 2010-04-06 | 4 |
| ⚠️ Sally Beck | 2011-08-06 | 5 |

**6 out of 10 employees (60%) were flagged as flight risks at some point.**

---

## 🤖 Predictive Model Summary
- **Model:** Linear Regression
- **R² Score:** 0.1962
- **RMSE:** 0.3751
- **Top Feature:** `word_count` (most positively correlated with sentiment score)
- **Interpretation:** Message length and word count show the strongest influence on sentiment. Longer, word-rich messages tend to be more positive.

---

## 💡 Key Insights & Recommendations

1. **High Flight Risk Rate:** 60% of employees were flagged — HR should conduct engagement surveys and 1-on-1 check-ins.
2. **Don Baughman** shows consistently negative communication — recommend immediate HR review.
3. **Lydia Delgado and John Arnold** are strong positive influencers — consider peer mentorship roles.
4. **Sentiment dips** appear in specific months — correlate with company events for root cause analysis.
5. **Short, terse messages** tend to be more negative — encourage richer communication culture.

---

## 📁 Project Structure
```
employee_sentiment/
├── employee_sentiment_analysis.ipynb  ← Main analysis notebook
├── test.xlsx                          ← Original dataset
├── test_labeled.xlsx                  ← Dataset with sentiment labels
├── README.md                          ← This file
├── report.docx                        ← Detailed report
└── visualizations/
    ├── sentiment_distribution.png
    ├── sentiment_over_time.png
    ├── messages_per_employee.png
    ├── negative_heatmap.png
    ├── monthly_scores_per_employee.png
    ├── employee_rankings.png
    ├── flight_risk.png
    ├── model_performance.png
    └── residual_plot.png
```
