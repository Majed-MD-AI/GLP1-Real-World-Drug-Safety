# GLP-1 Receptor Agonist Pharmacovigilance Using FDA FAERS

**Status: v0.1 — protocol and analysis scaffold**

This project is a reproducible pharmacovigilance study exploring whether selected adverse events are disproportionately reported with commonly used GLP-1 receptor agonists in the FDA Adverse Event Reporting System (FAERS), accessed through the openFDA Drug Event API.

The project is designed as a learning and portfolio study in **pharmacoepidemiology, real-world safety evidence, and regulatory evidence generation**.

> **Important:** This is a spontaneous-report pharmacovigilance analysis. A reporting signal is **not** evidence that a drug causes an adverse event, and FAERS cannot be used to estimate incidence or absolute risk.

## Research question

Among FDA adverse-event reports, which pre-specified safety events are disproportionately reported with selected GLP-1 receptor agonists, and how consistent are those signals across drugs and over time?

## Drugs
- semaglutide
- liraglutide
- dulaglutide

## Pre-specified adverse events
- pancreatitis
- cholelithiasis
- cholecystitis
- gastroparesis
- nausea
- vomiting

## Planned analyses
1. Drug-level report counts and common reaction terms
2. Reporting Odds Ratio (ROR) with 95% CI for each Drug × Event pair
3. Serious-report and calendar-year sensitivity analyses
4. Conservative regulatory/RWE interpretation

## Why this project

This repository complements **ATLAS — ICU Early Deterioration Prediction** by adding a second methodological track focused on:
- pharmacoepidemiology
- drug safety
- real-world evidence
- regulatory interpretation
- observational-data limitations

The longer-term goal is to progress from pharmacovigilance signal detection toward comparative effectiveness and causal inference using longitudinal real-world data.

## Data source

FDA FAERS via the official openFDA Drug Event API.

Base endpoint: `https://api.fda.gov/drug/event.json`

## Current milestone

**v0.1**
- research question defined
- exposures and outcomes pre-specified
- interpretation limits defined
- reproducible openFDA data-access notebook scaffold created

**Next milestone**
- retrieve report counts
- validate drug/event field definitions
- build first Drug × Event summary table

## Tech stack
Python, pandas, requests, NumPy, scipy, matplotlib, Jupyter Notebook

## Author
**Majed Hamad, MD**

Medical doctor transitioning into clinical data science, pharmacoepidemiology, real-world evidence, and clinical AI.

GitHub: https://github.com/Majed-MD-AI
