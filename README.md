# FUTURE_DS_03
> **Data Analytics Internship of Future Interns - Task 3**
# 📊 Bank Marketing Campaign — Funnel & Conversion Performance Analysis

> **Data Analytics Internship — Task 3**
> Analyzing a real-world Portuguese bank telemarketing dataset to uncover funnel drop-offs, conversion patterns, and actionable business recommendations using Power BI.

---

## 📌 Project Overview

This project analyzes the marketing funnel of a Portuguese banking institution that ran direct telemarketing campaigns to sell **term deposit subscriptions**. The goal is to identify where customers drop off in the funnel, which segments convert best, and how the bank can improve its overall conversion rate.

The analysis was built entirely in **Power BI** using the UCI Bank Marketing dataset.

---

## 📁 Repository Structure

```
├── dataset/
│   ├── bank-full.csv                  # Full dataset (45,211 records)
│   ├── bank-additional-full.csv       # Extended dataset with social/economic features
│   ├── bank-additional.csv            # 10% sample of extended dataset
│   ├── bank-names.txt                 # Attribute descriptions (original dataset)
│   └── bank-additional-names.txt      # Attribute descriptions (extended dataset)
├── dashboard/
│   └── Task_3.pbix                    # Power BI dashboard file
├── report/
│   └── Bank_Marketing_Analysis.pdf   # Full written analysis report
└── README.md
```

---

## 📂 Dataset Information

| Property | Details |
|---|---|
| Source | UCI Machine Learning Repository |
| Institution | Portuguese Banking Institution |
| Period | May 2008 – November 2010 |
| Total Records | 45,211 |
| Total Features | 16 input + 1 output |
| Target Variable | `y` — Has the client subscribed a term deposit? (yes/no) |

### Key Columns Used

| Column | Description |
|---|---|
| `age` | Age of the customer |
| `job` | Type of job |
| `education` | Education level |
| `contact` | Contact communication type (cellular, telephone, unknown) |
| `month` | Last contact month |
| `duration` | Last call duration in seconds |
| `campaign` | Number of contacts made during this campaign |
| `pdays` | Days since last contact from previous campaign (-1 = never) |
| `poutcome` | Outcome of the previous marketing campaign |
| `y` | Target — Did the client subscribe? |

---

## 📉 Funnel Stages & Conversion Rates

| Funnel Stage | Customers | Conversion Rate |
|---|---|---|
| Stage 1 — Total Customers Contacted | 45,211 | 100% (baseline) |
| Stage 2 — Reached via Cellular | 29,285 | 64.8% |
| Stage 3 — Previously Contacted | 8,257 | 18.3% |
| Stage 4 — Subscribed ✅ | 5,289 | **11.70%** |

---

## 🔴 Key Drop-off Insights

### Drop-off 1 — Stage 1 to Stage 2 (35.2% Lost)
- 13,020 customers were contacted via **unknown channel** — only **4.1%** of them converted
- Cellular contact converts at **14.9%** vs unknown at **4.1%** — a 3.6x difference
- Switching entirely to cellular outreach could recover ~1,400 extra subscriptions

### Drop-off 2 — Stage 2 to Stage 3 (71.8% Lost) — Biggest Drop-off
- **21,028 customers lost** — the single largest drop-off in the funnel
- 81.8% of all contacts had **no prior relationship** with the bank
- New customers convert at **9.2%** vs previously successful customers at **64.7%** (7x higher)

### Drop-off 3 — Stage 3 to Stage 4 (35.9% Lost)
- Customers called **6+ times** convert at only **5.8%** vs **14.6%** for a single call
- Over-calling is actively hurting conversion rates
- Call fatigue is the primary cause of drop-off at this final stage

---

## 📊 Key Findings

### By Contact Type
| Contact Method | Conversion Rate |
|---|---|
| Cellular | 14.9% ✅ |
| Telephone | 13.4% |
| Unknown | 4.1% ❌ |

### By Month (Top & Bottom)
| Month | Conversion Rate |
|---|---|
| March | 52.0% 🔥 |
| September | 46.5% 🔥 |
| December | 46.7% 🔥 |
| October | 43.8% ✅ |
| May | 6.7% ❌ |

### By Job Type (Top & Bottom)
| Job | Conversion Rate |
|---|---|
| Student | 28.7% 🔥 |
| Retired | 22.8% 🔥 |
| Blue-collar | 7.3% ❌ |
| Entrepreneur | 8.3% ❌ |

### By Previous Campaign Outcome
| Outcome | Conversion Rate |
|---|---|
| Success | 64.7% 🔥 |
| Other | 16.7% |
| Failure | 12.6% |
| Unknown / New | 9.2% ❌ |

### By Number of Calls Made
| Calls | Conversion Rate |
|---|---|
| 1 Call | 14.6% ✅ |
| 2–3 Calls | 11.2% |
| 4–5 Calls | 8.6% |
| 6+ Calls | 5.8% ❌ |

---

## ✅ Actionable Recommendations

| Priority | Recommendation | Expected Impact |
|---|---|---|
| #1 | Re-target previously successful customers first | 64.7% conversion — 7x ROI |
| #2 | Switch all contacts to cellular method | 3.6x improvement over unknown |
| #3 | Focus campaigns in March, Sep, Oct, Dec | 52% vs 11.7% average |
| #4 | Set a maximum of 3 calls per customer | Eliminate call fatigue drop-off |
| #5 | Prioritize Students and Retired segments | 2–3x above average conversion |
| #6 | Improve new customer onboarding script | +~1,000 subscriptions potential |

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| Power BI Desktop | Dashboard building and data visualization |
| DAX | Custom measures and conversion rate calculations |
| Power Query | Data cleaning and transformation |
| CSV | Raw dataset format |
| Microsoft Word | Written analysis report |

---

## 📈 Dashboard Pages

The Power BI dashboard (`Task_3.pbix`) contains the following:

1. **Funnel Overview** — KPI cards, funnel chart, overall conversion metrics
2. **Channel & Campaign Analysis** — Conversion by contact type, month, and number of calls
3. **Customer Segmentation** — Conversion by job, education, and previous campaign outcome
4. **Comparison Cards** — Previously successful vs new customer conversion rates

---

## 🚀 How to Use

1. Clone this repository
```bash
git clone https://github.com/your-username/bank-marketing-funnel-analysis.git
```

2. Open the dashboard
   - Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
   - Open `dashboard/Task_3.pbix`

3. Load the dataset
   - If prompted, redirect the data source to `dataset/bank-full.csv`
   - Ensure the delimiter is set to **semicolon (;)**

4. Explore the report
   - Use slicers to filter by month, job, contact type, and previous outcome
   - All visuals are interactive and cross-filter each other

---

## 📚 Dataset Citation

```
[Moro et al., 2014] S. Moro, P. Cortez and P. Rita.
A Data-Driven Approach to Predict the Success of Bank Telemarketing.
Decision Support Systems, In press.
http://dx.doi.org/10.1016/j.dss.2014.03.001
```

---

## 👤 Author

**Karthik Boddupally**
Data Analytics Intern
- LinkedIn: [https://www.linkedin.com/in/karthik-boddupally-824b70290/]
- GitHub: [https://github.com/karthik-boddupally]

---

## 📄 License

This project is for educational purposes as part of a Data Analytics Internship program. The dataset is publicly available from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).
