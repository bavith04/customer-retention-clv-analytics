# Customer Retention Ledger & Lifetime Value (CLV) Analytics

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Tests](https://img.shields.io/badge/Tests-149%20Passed-brightgreen.svg)]()
[![Dataset](https://img.shields.io/badge/Dataset-Online%20Retail%20II%20(800K+)-orange.svg)]()
[![Dashboard](https://img.shields.io/badge/Interactive%20UI-Chart.js%20Dashboard-purple.svg)]()

An enterprise-grade customer analytics, cohort retention, and probabilistic Customer Lifetime Value (CLV) prediction pipeline built on 800,000+ multi-year e-commerce transactions from the **Online Retail II** dataset.

The system translates raw transactional ledger data into actionable commercial strategy across **28 modular analytical phases**, validated by **149 automated unit tests** (`pytest`) and an interactive browser-based business intelligence dashboard.

---

## 📊 Key Executive Findings

* **Extreme Revenue Concentration:** The top **36.0% of customers** (*Champions* and *Loyal Customers*) drive **85.3% of all historical revenue (£14.15M)**.
  * Stress-tested across alternative quantile boundaries (4-bin vs 5-bin scoring), confirming concentration is an inherent commercial reality (84.9%–85.3%) rather than a segmentation artifact.
* **Quantified Revenue-at-Risk:** A targeted 5% reduction in churn among top-tier *Champions* preserves more revenue than attempting to reactivate the entire bottom 40% of dormant accounts.
* **Cohort Retention Dynamics:** Triangular cohort retention tracking across 24 monthly cohorts reveals rapid initial attrition followed by steady long-term customer monetization.
* **100% Deterministic Reconciliation:** Full transaction reconciliation ensuring aggregate customer revenue sums identically match raw ledger totals with zero data leakage.

---

## 🏗️ Technical Architecture & Pipeline (28 Phases)

```
[ Raw Transactions (800K+) ] 
             │
             ▼
[ Phase 1–4: Data Cleaning & Ledger Reconciliation ]
  ├── Canceled order handling, unit price validation, customer ID linkage
  └── Consolidated Customer Summary Table
             │
             ▼
[ Phase 5–9: RFM Segmentation & Stability Stress-Testing ]
  ├── Recency, Frequency, Monetary Value quantile scoring
  └── Stability testing across varying segmentation cutoffs
             │
             ▼
[ Phase 10–14: Triangular Cohort Retention Matrices ]
  ├── Monthly cohort grouping & retention percentage decay heatmaps
  └── Repeat purchase cycle & customer attrition modeling
             │
             ▼
[ Phase 15–18: Probabilistic CLV Modeling & Validation ]
  ├── Transaction frequency modeling + monetary spend distribution
  └── Holdout period validation and forecast calibration
             │
             ▼
[ Phase 19–23: Revenue-at-Risk & Churn Simulation ]
  ├── Counterfactual intervention modeling for customer preservation
  └── Multi-country distribution & cross-border customer analysis
             │
             ▼
[ Phase 24–28: Interactive BI Dashboard & Final Audits ]
  ├── Standalone Chart.js retention & CLV dashboard
  └── 149 automated unit tests & business decision reports
```

---

## 📈 Interactive Retention Dashboard

The project includes a lightweight, zero-dependency interactive dashboard (`retention_dashboard.html`):
* **Visualizes Cohort Matrices:** Interactive retention decay heatmaps across acquisition months.
* **RFM Breakdown:** Drill down into customer counts, average monetary spend, and recency distributions by tier.
* **CLV Predictions & What-If Simulator:** Dynamically simulate the revenue impact of adjusting retention rates across customer segments.

To view: simply double-click `retention_dashboard.html` to open it in any web browser.

---

## 🧪 Automated Testing & Quality Assurance

Every analytical transformation is enforced by a comprehensive automated test suite:
* **149 unit tests** verifying schema constraints, data reconciliation, statistical metrics, edge cases, and numerical tolerances.
* Run tests with:
  ```bash
  pytest src/ -v
  ```

---

## 🚀 Quick Start & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/bavith04/customer-retention-clv-analytics.git
cd customer-retention-clv-analytics
```

### 2. Environment Setup
```bash
python3 -m venv venv
source venv/bin/activate
pip install pandas numpy scikit-learn pytest
```

### 3. Open the Interactive Dashboard
Open `retention_dashboard.html` in Safari, Chrome, or Firefox:
```bash
open retention_dashboard.html
```

---

## 🛠️ Tech Stack & Methodologies
* **Language & Analysis:** Python 3.9+, Pandas, NumPy, Scikit-learn
* **Testing:** Pytest (149 passing test cases)
* **Frontend / BI:** Standalone HTML5, CSS3, Chart.js v4.4.0
* **Core Domains:** Cohort Retention, RFM Segmentation, Probabilistic CLV, Churn Simulation, Ledger Financial Reconciliation

---

## 👤 Author
**Bavith Dalu**  
* GitHub: [@bavith04](https://github.com/bavith04)