# ◈ DataScope — Interactive Data Quality Inspector

> Find it. Understand it. Fix it yourself.

A Python tool that scans any CSV file for data quality issues and opens 
an interactive HTML dashboard showing exact problem locations — row by 
row — in plain English. The human analyst decides what to fix.

---

## Demo

![IBM HR Dashboard](screenshots/dashboard_ibm.png)
![UK Retail Dashboard](screenshots/dashboard_retail.png)
![Column Detail](screenshots/column_detail.png)

---

## The Problem

IBM research shows bad data costs companies an average of $12.9 million 
per year. Yet 76% of data professionals still use spreadsheets as their 
main cleaning tool — scrolling through thousands of rows manually trying 
to find problems.

DataScope solves this: automated detection, human-controlled fixing.

---

## What It Detects

| Check | What It Finds | Severity |
|-------|--------------|----------|
| Missing Values | Empty cells per column with exact % | GREEN / AMBER / RED |
| Duplicates | Repeated rows across whole dataset | GREEN / AMBER / RED |
| Data Types | Numbers or dates stored as text | AMBER |
| Outliers | IQR-based unusual values with row numbers | GREEN / AMBER / RED |

---

## How It Works

1. Tool reads any CSV file using pandas
2. Every column is scanned automatically across 4 checks
3. A health score out of 100 is calculated
4. An interactive HTML dashboard is generated
5. Dashboard opens automatically in your browser
6. Click any column to see exact row numbers and charts
7. Export full report as PDF
8. YOU decide what to fix — the tool never touches your data

---

## Tested On Two Real Datasets

**IBM HR Analytics** (1,470 rows · 35 columns)
- Health Score: 36/100
- Found: 10 columns with salary and tenure outliers
- Source: Kaggle — IBM HR Analytics Attrition Dataset

**UK Retail Sales** (421,570 rows · 17 columns)
- Health Score: 0/100
- Found: 5 columns with 60-73% missing values
- Found: 35,000+ outliers in weekly sales figures
- Source: Kaggle — Retail Dataset (combined from 3 files)

---

## Key Design Decision

The tool surfaces problems and explains their business impact but 
**never modifies the source data.** The human analyst stays in full 
control of every fix.

This is called Human-in-the-Loop — the direction the entire industry 
is moving in 2026, supported by research from Gartner and IBM.

---

## How To Run It

```bash
git clone https://github.com/yogalakshmi1426/Datascope.git
pip install -r requirements.txt
jupyter notebook notebooks/datascope.ipynb
```

---

## Skills Demonstrated

Python · pandas · NumPy · IQR Statistics · matplotlib · seaborn · 
HTML generation · JavaScript interactivity · Data Quality Analysis · 
Human-in-the-Loop Design

---

## Author

Yogalakshmi Shanmuga Jothi
MSc Computer Science (Merit) — University of Sussex
Dissertation: Cyber Threat Detection using ML — 99.6% accuracy