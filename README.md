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

2. **Previous campaign success is the strongest year-independent predictor.** Prior subscribers converted at 65.1% vs 8.8% for fresh leads (Cohen's h = 1.27, very large effect).

3. **Cellular outperforms telephone by 2.8x universally** — across every job category, every month, every customer segment.

4. **Diminishing returns set in after 3 contacts.** Beyond 5 contacts per client, conversion drops below 6%.

5. **The "month effect" is largely a year confound.** May converted at 3.1% in 2008 but 57.5% in 2010 — calendar timing matters less than the rate environment.

---

## 📈 Recommended Strategy: Crisis-Aware Targeting

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
