# Explainable Risk Scoring for Decision-Oriented Analytics

This project demonstrates how a simple, interpretable analytics pipeline can be used to support real-world decision-making under risk.  
Rather than optimising for complex models, the focus is on **clarity, explainability, and decision readiness**.

The notebook builds an end-to-end risk scoring workflow that translates raw data into:
- A clear risk score (0–100)
- Interpretable drivers of risk
- Case-level narratives suitable for analyst review

---

## Why This Project
In many organisations, analytics fails not because models are weak, but because decisions cannot be clearly explained or defended.  
This project is designed as a **decision-support baseline**, prioritising transparency over complexity.

It reflects how analytics is actually reviewed by managers, auditors, and risk committees.

---

## Data
- Public dataset from OpenML: *German Credit*  
- The label "bad" is treated as a proxy for higher risk
- The dataset is used strictly for demonstration purposes

---

## Methodology
- One-hot encoding for categorical features
- Logistic regression (audit-friendly and interpretable)
- Class balancing to prioritise detection of higher-risk cases
- Evaluation using ROC-AUC, confusion matrix, and recall-focused metrics

---

## Key Outputs
- **Risk score (0–100)** for prioritisation
- **Top risk-increasing drivers**
- **Top risk-reducing drivers**
- **Case narrative** explaining why a specific record is flagged

---

## How a Manager Would Use This
- Scores above a defined threshold are prioritised for analyst review
- Borderline cases are manually assessed using the explanatory drivers
- Outputs support transparency and accountability in decision-making
- This tool is intended for **decision support**, not automated rejection

---

## Interpretability & Governance Notes
- Model coefficients indicate associations, not causality
- Some features may act as sensitive proxies and require governance review
- Outputs should always be interpreted with human oversight

---

## How to Run
```bash
pip install -r requirements.txt
