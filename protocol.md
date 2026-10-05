# Analysis Protocol

## Objective
Characterize selected adverse-event reporting patterns for commonly used GLP-1 receptor agonists in FDA FAERS and estimate report-level disproportionality using Reporting Odds Ratios (RORs).

## Study design
Retrospective pharmacovigilance analysis of spontaneous adverse-event reports.

This is **not** a cohort study and **not** a causal comparative-effectiveness analysis.

## Data source
FDA Adverse Event Reporting System (FAERS) via the openFDA Drug Event API.

## Exposure definition
1. semaglutide
2. liraglutide
3. dulaglutide

## Pre-specified outcomes
1. PANCREATITIS
2. CHOLELITHIASIS
3. CHOLECYSTITIS
4. GASTROPARESIS
5. NAUSEA
6. VOMITING

No primary outcome will be added solely because it appears statistically strong in exploratory results.

## Unit of analysis
FAERS adverse-event report.

Because one report may contain multiple drugs and multiple reactions, all results will be interpreted as **reporting associations**, not patient-level risks or causal effects.

## Primary measure

For each drug-event pair:

|                    | Event present | Event absent |
|--------------------|--------------:|-------------:|
| Drug present       | a             | b            |
| Comparator reports | c             | d            |

ROR = (a × d) / (b × c)

A 95% confidence interval will be calculated on the log scale.

## Planned comparator
Initial MVP comparator: other FAERS reports in the same data source/time window.

## Primary outputs
- drug-level report counts
- drug × event counts
- ROR
- 95% CI
- forest plot
- calendar-year reporting trends

## Bias and limitations to address
- spontaneous reporting bias
- under-reporting
- stimulated/notoriety reporting
- missing exposed-population denominator
- duplicate/follow-up reports
- co-medications and confounding by indication
- inability to estimate incidence or absolute risk
- inability to infer causality
- differences in time on market and drug utilization

## Next evidence step
A confirmatory RWE study would ideally use longitudinal EHR, claims, or registry data with:
- incident-user design when possible
- active comparator
- explicit time zero
- follow-up definition
- measured-confounder adjustment
- sensitivity analyses
- potentially target-trial emulation
