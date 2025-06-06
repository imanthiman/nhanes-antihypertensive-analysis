# Antihypertensive Drug Efficacy Analysis (NHANES 2017–2018)

## Objective

To evaluate and compare the real-world effectiveness of selected antihypertensive medications across major therapeutic classes, using national health survey data from the U.S. NHANES 2017–2018 dataset.

## Background

Hypertension remains a leading modifiable risk factor for cardiovascular disease. Despite widespread pharmacologic options, real-world treatment outcomes vary based on drug class, patient factors, and clinical context. This analysis investigates how effective specific high-potency antihypertensive agents are in achieving blood pressure control in the U.S. population.

## Data Sources

All data were sourced from the publicly available NHANES 2017–2018 cycle:

- `DEMO_J.XPT` — Demographic data  
- `BPX_J.XPT` — Blood pressure measurements  
- `RXQ_RX_J.XPT` — Prescription medications reported within the past 30 days

## Tools Used

- Python 3.11  
- Jupyter Notebook  
- pandas, seaborn, matplotlib  

## Drugs Compared

One widely accepted, guideline-supported agent was selected from each major antihypertensive drug class:

**Ramipril**    | ACE Inhibitor
**Telmisartan** | Angiotensin II Receptor Blocker (ARB)  
**Bisoprolol**  | Beta-blocker
**Amlodipine**  | Calcium Channel Blocker **Chlorthalidone** | Thiazide-like Diuretic

These agents were chosen based on clinical potency, guideline recommendations, and real-world prescribing patterns.

## Outcome Definition

A participant was classified as having **controlled blood pressure** if:
- **Systolic BP < 140 mmHg** and  
- **Diastolic BP < 90 mmHg**

This definition follows contemporary hypertension treatment thresholds from JNC 8 and ACC/AHA guidelines.

## Method Summary

- Merged demographic, blood pressure, and prescription data using `SEQN`
- Filtered the dataset to identify individuals taking each of the five target drugs
- Calculated and visualized the proportion of patients with controlled BP by drug
- Compared treatment effectiveness across classes based on control rates

## Limitations

- **Cross-sectional data only**: NHANES is not longitudinal, so we cannot evaluate before-and-after treatment effects  
- **No dosage or duration data**: We only know whether a drug was reported in the past 30

## Summary Plot

-This chart shows the real-world blood pressure control rate for five potent antihypertensive drugs using NHANES data.

![bp_control_by_drug](https://github.com/user-attachments/assets/da093019-8390-4d79-a0ce-c972bbf8dc9a)
