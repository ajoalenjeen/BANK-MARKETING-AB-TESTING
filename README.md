# BANK-MARKETING-CAMPAIGN-ANALYSIS

### Improving Conversion Rates Through A/B Testing & Statistical Segmentation

A statistical analysis of a Portuguese bank's direct telemarketing campaign (2008–2010), focused on identifying which targeting strategies could improve conversion rates and reduce wasted call volume.

---

## 🎯 Project Goal

Analyze 41,176 contact records to answer: **How can the bank improve conversion rates and optimize contact strategies for term deposit subscriptions?**

The project deliberately excludes predictive modeling to focus on statistical rigor and business interpretability — the methodology a product or marketing analyst would use day-to-day.

---

## 🔑 Key Findings


1. **Macroeconomic conditions dominated campaign performance.** Conversion rose from 4.8% (2008) to 52.1% (2010) as the Euribor rate fell from 4.82 to 0.81. The bank made 67% of its calls in its worst-performing year.

2. **Previous campaign success is the strongest predictor (validated by A/B test).** Prior subscribers converted at 65.1% vs 8.8% for fresh leads — a 56 percentage point gap (two-proportion z-test, p < 0.001, **Cohen's h = 1.27, very large effect**).

3. **Cellular outperforms telephone by 2.8x — universally and significantly.** 14.7% vs 5.2% across all 41,176 contacts (z-test, p < 0.001, h = 0.33). The advantage holds within every job category and every month — no demographic segment performs better on telephone.

4. **Diminishing returns set in after 3 contacts (chi-square confirmed).** Conversion drops from 13.0% (1 contact) to 5.5% (6+ contacts). Pairwise z-tests show the effect becomes meaningful at the 4-5 contact threshold.

5. **Day-of-week is statistically significant but practically irrelevant.** A deliberate null finding (Cramér's V = 0.025) — included to demonstrate that with 41k records, p-values alone are insufficient for decision-making.

6. **The "month effect" is largely a year confound.** May converted at 3.1% in 2008 but 57.5% in 2010 — calendar timing matters less than the rate environment. This insight emerged after the initial month analysis was reframed by temporal investigation.

---

## ✅ Recommendations

Based on the analysis, the bank should adopt a **layered targeting strategy**:

### Tier 1 — Immediate, no-risk change
**Stop calling the worst-performing segment.** Eliminate clients who match: *telephone channel + May + blue-collar/services/entrepreneur job category.* This single rule removes 9% of call volume while losing only 3% of subscribers — a 27:1 cost-benefit ratio with zero operational disruption.

### Tier 2 — Primary strategy: Crisis-Aware targeting
**Calibrate call volume to the interest rate environment.** Term deposits become more attractive when alternative safe-haven returns are low, so call volume should scale up during low-Euribor periods and scale down during high-Euribor periods — regardless of calendar month.

### Tier 3 — Within Crisis-Aware, prioritize high-value clients
- **Channel:** Cellular only. Telephone underperforms by 2.8x in every job category.
- **History:** Prioritize clients with prior contact history (any outcome). Previous campaign success is the strongest single predictor in the dataset.
- **Frequency:** Cap at 3 contacts per client. Beyond 5 contacts, conversion drops below 6%.



## 📊 Projected Impact

| Strategy | Calls | Subscribers | Conv Rate | Calls Saved |
|----------|------:|------------:|----------:|------------:|
| Baseline (actual campaign) | 41,176 | 4,639 | 11.27% | — |
| **Crisis-Aware** | **11,652** | **2,999** | **25.74%** | **-72%** |

The Crisis-Aware strategy would have captured **65% of subscribers using 28% of the call volume** — a **2.28x improvement in conversion efficiency**.

---

## 🛠️ Methods Used

- **Exploratory data analysis** — distribution analysis, missing-value diagnostics, multicollinearity checks
- **Statistical hypothesis testing** — chi-square tests of independence, two-proportion z-tests
- **Effect size validation** — Cohen's h for proportions, Cramér's V for categorical associations
- **Multi-variable customer segmentation** — micro-segment analysis with sample-size guards
- **Temporal & macroeconomic analysis** — year reconstruction, economic phase bucketing
- **Retrospective strategy simulation** — four alternative targeting frameworks compared against the baseline

---

## 📂 Repository Structure

```
bank-marketing-ab-testing/
├── data/                       # Raw dataset
├── notebooks/                  # Main analysis notebook
├── reports/
│   ├── executive_summary.md
│   └── figures/                # Exported charts
└── docs/                       # Methodology notes
```

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/ajoalenjeen/bank-marketing-ab-testing.git
cd bank-marketing-ab-testing

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook notebooks/bank_marketing_analysis.ipynb
```

---

## 📊 Dataset

UCI Bank Marketing Dataset (`bank-additional-full.csv`) — 41,188 records, 20 input features, binary subscription target. Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).

Citation: *Moro, S., Cortez, P., & Rita, P. (2014). A data-driven approach to predict the success of bank telemarketing. Decision Support Systems, 62, 22-31.*

---

## 🧰 Technologies

Python · pandas · NumPy · SciPy · statsmodels · matplotlib · seaborn · Jupyter

---

## 📝 Caveats

This is a **retrospective analysis**, not a forecast. Findings should be revalidated in a different economic environment, as the dataset captures the unique 2008–2010 financial crisis period. The Crisis-Aware strategy trades acquisition volume for efficiency — a 35% subscriber loss is the cost of the 72% call reduction.

---

## 👤 Author

**Ajo Alenjeen**
MBA Candidate, Business Analytics — Pace University
[LinkedIn](https://linkedin.com/in/your-profile) · [Portfolio](https://github.com/ajoalenjeen)
