---
title: Investing in Flourishing Extractor Knowledge Base
Created by: Shams Sadhin
Last Modified: June 15

---

# Investing in Flourishing Extractor Knowledge Base

One-page instructions for extracting intervention study evidence into a simplified Excel file and companion source log.

The agent should produce one Excel workbook with one sheet named `Extractor_Results`, plus a separate plain text source log.

## Project Overview

The Investing in Flourishing literature review extracts structured evidence from intervention studies and reports. The focus is programs for children from prenatal through age 3 for the children and caregiver across multiple social domains such as  healthcare, education, child welfare, employment, and criminal justice outcomes that support the evidence base.

The goal is to capture program details, study design, population, outcomes, baseline/final values, treatment/control values, sample sizes, uncertainty terms, source locations, and effect size calculations which can later support validation, meta-analysis, and simulations.

## Simple Output Schema

Create one Excel workbook with one sheet named `Extractor_Results`. Use these columns in this exact order:

`Program | Description | Location | Population | Year | Study Sample | Program Domain | Study Type | Outcome_Fixed | Outcome | Outcome Domain | Group | Control Baseline | Control Final | Treatment Baseline | Treatment Final | Control Sample Size | Treatment Sample Size | N | Period | Original Unit | Abs Diff | Rel Change | Significance | Confidence Intervals | CI_lower | CI_upper | Standard Error | p value | Source Location | Notes`

Create a separate plain text file named `extraction_source_log.txt`. The log records where each extracted value came from the source and validation concerns.

## Unit of Analysis

Each row represents one paper, one program or intervention arm, one outcome, one comparison or group, and one time period.

Split rows when outcomes differ, subgroups differ, follow-up periods differ, or comparison/intervention group differs.

If a source reports only one group with no comparator, create one row and explain the design in `Group` or `Notes`.

If a paper reports multiple interventions compared separately to controls, create separate rows for each intervention and outcome.

## Codebook

| Column | Definition |
|---|---|
| Program | Intervention or program arm being evaluated. |
| Description | Two to three concise sentences describing the program, what it does and what the study evaluates.|
| Location | Study geography. |
| Population | Eligible or analyzed population. |
| Year | Publication, report, or study year when available. Indicate in Notes whether the value is a publication year, report year, or study cohort year when unclear. |
| Study Sample | Reported sample statement, including treatment/control counts if shown. |
| Program Domain | Primary domain: Healthcare, Education, Child Welfare, Criminal Justice, or another needed domain. |
| Study Type | Study design category. |
| Outcome_Fixed | Standardized outcome label used across studies, such as ED visits, Inpatient admissions, Low birth weight, Special education placement, or Child maltreatment. Find Outcome_Fixed from the outcome mappings and if unsure leave it blank |
| Outcome | Exact or close source wording for the outcome. |
| Outcome Domain | Domain affected by the outcome: Healthcare, Education, Child Welfare, Criminal Justice, Employment, or another needed domain. |
| Group | Subgroup, analytic sample, comparison, intervention arm, or follow-up window if relevant. |
| Control Baseline | Control or comparison value before intervention or at baseline. |
| Control Final | Control or comparison value after intervention or at follow-up. |
| Treatment Baseline | Treatment or intervention value before intervention or at baseline. |
| Treatment Final | Treatment or intervention value after intervention or at follow-up. |
| Control Sample Size | Control/comparison analytic sample for the outcome. |
| Treatment Sample Size | Treatment/intervention analytic sample for the outcome. |
| N | Total analytic sample if arm-specific sizes are unavailable. |
| Period | Measurement or follow-up period in months up to 2 decimals when convertible. |
| Original Unit | Source unit for the value, such as rate, percent, mean visits, dollars, days, odds ratio, or IRR. |
| Abs Diff | Absolute effect or difference when calculable from source values. |
| Rel Change | Relative change when denominator and comparison are clear. |
| Significance | Significant, Not significant, Not reported, or Check notes. |
| Confidence Intervals | CI level |
| CI_lower / CI_upper | Numeric lower and upper confidence interval bounds when reported. |
| Standard Error | Standard error for the estimate when reported. |
| p value | Exact p-value or threshold as reported. |
| Source Location | Page plus table, figure, appendix, exhibit, section, or body location for the extracted numeric values. |
| Notes | Detailed extraction note with caveats, conversions, modeled-effect details, and ambiguity. |

## Outcome_Fixed Mapping

Use this mapping to choose `Outcome_Fixed`. Match the paper outcome wording to the closest original outcome wording below. If there is no clear match, leave `Outcome_Fixed` blank and explain the uncertainty in `Notes` and `extraction_source_log.txt`.

| Outcome_Fixed | Original outcome wording examples |
|---|---|
| ED visits | ED Visits; Reduced ED Visits; Reduced ED visits; Reduced ED with admission; Reduced ED without admission; Reduced any ED visit (with or without admission); Reduced outpatient ER Visits; Reduction in ED Visits; Reduction in ED visits |
| Inpatient admissions | Hospitalizations; Reduced Hospitalizations; Reduced hospitalizations; Reduced hospitalizations/ overnight visits; Reduced inpatient hospital overnights; Reduced overnight visits; Reduction in Hospitalizations; Reduction in Impatient Admissions; Reduction in Impatient admissions; Reduction in hospitalizations |
| Grade retention | Increased Never Grade Retained (elementary school); Increased Never Grade Retained (middle school); Reduced Grade Retention; Reduced grade retention; Reduction in Grade Retention |
| Out-of-home placement | Child out-of-home placements; Out-of-home care placement; Reduced out of home placement; Reduced out-of-home placement; Reduced removed from home; Reduced subsequent removal; Reduction in out of home placement; Reduction in out of home placement reduction |
| Special education placement | Reduced Special Education; Reduced Special Education (elementary school); Reduced Special Education (middle school); Reduced special education |
| Low birth weight | Low birth weight; Reduced low birth weight (<2500 g); Reduced very low birth weight (<1500 g) |
| Preterm birth | Preterm birth; Reduced extremely preterm birth (<28 weeks gestation); Reduced preterm birth (<37 weeks gestation) |
| Child maltreatment | Child maltreatment injuries (hospitalization/ER); Reduced abuse or neglect; Reduced child maltreatment incidence; Reduction in child abuse and neglect; Reduction in child maltreatment; Reduction in children maltreatment |
| Reunification | Increase in reunification; Increased experienced reunification; Increased reunification; Increased reunification with caregiver; Increased reunification with parent; Reunification; Succesful reunification |
| Days in out-of-home placement | Reduced days in foster care; Reduced days in out-of-home care; Reduced days in out-of-home placement; Reduced days out of home; Reduction in days out of home |
| Employment | Employment at age 40; Increase in parental employment; Increased employment full-time status |
| Urgent healthcare use | Reduction in Urgent Health Care Use; Reduction in urgent health care; Reduction in urgent health care use |
| Substantiated maltreatment report | Reduced substantiated maltreatment report; Reduction in substantiated neglect report; Reduction in substantiated report; Substantiated child maltreatment cases; substantiated child maltreatment |
| Wage income | Increase in parental wage income |
| Hours worked per week | Increase in hours worked per week |
| Cesarean delivery | Reduced cesarean delivery; Reduction in cesarean section births |
| Time to permanency | Decreased time to permanency; Reduction in time for relative/ guardian; Reduction in time to adoption; Reduction in time to reunification |
| Placement changes | Reduced placement changes; Reduction in placement changes; Reduction in placement changes after kinship; Reduction in placements change rates |
| Maltreatment report | Reduced concern for abuse or neglect claim; Reduced maltreatment report; Reduction in maltreatment reports |
| Emergency medical care use | Reduced child total emergency medical care use; Total child emergency medical care |
| School attendance | Increased school attendance; Reduced missed school days; Reduction in missed school days |
| Healthcare professional visits | Reduced visits to health care professionals; Visit to Health care Professional |
| Permanency outcomes | Increased Permanency Outcomes; Overall Permanency; Successful permanency attempts |
| Infant mortality | Infant mortality |
| Violent crimes | Reduction in violent crimes |
| Composite adverse birth outcome | Reduced composite adverse birth outcome; Reduced composite adverse birth outcome (preterm birth, low birth weight, SGA, or perinatal mortality) |
| NICU stay | Reduced overnight NICU stay |
| Weight gain during pregnancy | Adequate weight gain during pregnancy; Reduced weight gain during pregnancy |
| Prenatal care adequacy | Adequate prenatal care (Adequacy of Prenatal Care Utilization (APNCU) Index) |
| Kinship placement | Decrease Relative / guardian / other exits; Increased placement with kin |
| Adoption | Decreased adoption; Succesful adoption |
| ED visits or hospitalizations (asthma) | Emergency Department Visits or Hospitalizations (for asthma) |
| Repeat maltreatment report | Reduced repeat maltreatment report; Reduced repeat substantiated maltreatment report |
| Small for gestational age | Small for gestational age |
| Re-abuse incident | Reduced reabuse incident (by target parent; abuse of any child); Reduced reabuse incident (target youth) |
| Parent missed work days | Missed work in past 2 weeks; Reduced parent work days |
| Abusive head trauma (AHT) | Reduction in AHT cases |
| Hospitalization spending | Reduced hospital spending; Reduced hospitalization spending |
| Primary care visits | Reduced doctor visits; Reduction in Primary Care Visits |
| Annual health-related costs | Reduction in annual health related costs |
| Perinatal mortality | Reduced perinatal mortality |
| High school graduation | Graduated high school |
| Criminal arrests | Arrested (5+ times by age 40) |
| Subsequent birth | Reduction in subsequent second birth |
| Symptom-free days | Increase in sympton free days |
| Medicaid spending | Reduced Medicaid Spending per member per month |
| All-cause mortality (including fetal death) | Reduced all-cause mortality including fetal death |
| Major injury | Reduced any major injury |
| Composite adverse outcome | Reduced composite adverse outcome (major injury, mortality, or abuse/neglect) |
| Severe maternal morbidity | Reduced severe maternal morbidity |
| Large for gestational age | Reduced large for gestational age |
| College degree attainment | Increased college degree attainment |
| Neonatal morbidity | Reduced neonatal morbidity |
| Years of education completed | Increased years of education completed |
| Emergency medical care costs | Reduced total emergency medical care billing costs |
| Asthma cases | Reduction in Asthma cases |
| Re-entry into foster care | Reduced re-entry into foster care within 12 months |
| Physical or sexual abuse report | Reduction in physical or sexual abuse report |
| Unsubstantiated maltreatment report | Reduction in unsubstantiated report |
| Homelessness | Reduction in homelessness |
| Therapy costs | Reduced therapy cost |
| Still in foster care | Decreased still in foster care status |
| Cerebral palsy | Reduction in cerebral palsy |
| Time to any exit (foster care) | Reduction in time for any exit |
| Earnings (age 40) | Earned $20k+ at 40 |

## Controlled Values

| Field | Allowed Values |
|---|---|
| Program Domain | Healthcare; Education; Child Welfare; Criminal Justice. Add a relevant domain only when none fit. |
| Outcome Domain | Healthcare; Education; Child Welfare; Criminal Justice; Employment. Add a relevant domain only when needed. |
| Study Type | RCT; Quasi-Experimental; Simulation; Nonexperimental; WSIPP Meta Analysis; Observational/ Non-RCT; Group Study; Pre-post evaluation; Other. |
| Significance | Significant; Not significant; Not reported; Check notes. |

## Decision Rules

### Study Type

- Use **RCT** for randomized controlled trials, including cluster randomized trials.
- Use **Quasi-Experimental** for matched comparison, difference-in-differences, regression discontinuity, interrupted time series with comparison, or similar designs.
- Use **Observational/ Non-RCT** when the design is observational and has no credible quasi-experimental identification.
- Use **Simulation** for modeled or simulation results.
- Use **WSIPP Meta Analysis** when the row is from a WSIPP meta-analysis rather than a single source study.
- Use **Other** only when none of the listed categories fit and explain in Notes.

### Treatment, Control, Baseline, and Final

- Use baseline fields for pre-intervention or baseline values.
- Use final fields for post-intervention, follow-up, or final values.
- If only final treatment and control values are reported, leave baseline fields blank.
- If only pre-post treatment values are reported, fill Treatment Baseline and Treatment Final and explain the missing comparator.
- Never enter zero for an unreported value. Leave missing numeric cells blank.

### Effects and Calculations

- First extract raw inputs for treatment, control, baseline, and final values when available.
- If only final group means or rates are reported, calculate `Abs Diff = Treatment Final - Control Final`.
- If both groups have baseline and final values, calculate `Abs Diff = (Treatment Final - Treatment Baseline) - (Control Final - Control Baseline)`.
- Finals-only relative change: `(Treatment Final - Control Final) / Control Final`.
- Single-arm pre-post relative change: `(Treatment Final - Treatment Baseline) / Treatment Baseline`.
- Full 2x2 relative change: `(Treatment Final / Treatment Baseline) / (Control Final / Control Baseline) - 1`.
- Keep direction consistent with the source outcome. Do not flip signs unless explicitly instructed.
- If the paper only reports modeled effects such as IRR, odds ratio, regression coefficient, adjusted difference, cost difference, or net savings and raw inputs are unavailable, do not invent raw values. Record the reported effect, uncertainty terms, and interpretation in Notes and Source Log.

### Error Terms and Missing Values

- Extract all available p-values, confidence interval text, CI level, CI lower bound, CI upper bound, standard error, and significance statements.
- If no p-value, CI, or significance statement is reported, set Significance to Not reported and leave numeric error fields blank.
- Use Check notes when a result is ambiguous, internally inconsistent, or hard to map into the schema.
- Do not invent missing values, sample sizes, denominators, or time periods.

## Source Log TXT File

Create a separate plain text file named `extraction_source_log.txt`.

Organize it by PDF or paper title and then by extracted row. Use page numbers and the most precise available source marker. If line numbers are unavailable, use table/figure/exhibit/appendix/section and a short body excerpt.

For each row, include:

- Program, outcome, group, and period.
- For every extracted numeric value: field name, value, page, table/figure/section/body location, and short source excerpt or paraphrase. For other values also include page and short phrase
- Calculation notes for Abs Diff and Rel Change, including formula used and denominator.
- Validation concerns: missing source, ambiguous comparison, wrong-unit risk, modeled-only effect, unclear denominator, missing sample size, inconsistent values, or needs human review.
- If they are same values just report those where they were available once

## Example Extractor_Results Rows

These example rows are adapted from the Chicago Child-Parent Center rows in `context/context_file.xlsx`. They show how one study can create separate rows for different outcomes and follow-up groups. The description is intentionally detailed enough to explain what the program does and what the study evaluates. Blank cells are intentionally left blank when the context file did not report a value.

```tsv
Program	Description	Location	Population	Year	Study Sample	Program Domain	Study Type	Outcome_Fixed	Outcome	Outcome Domain	Group	Control Baseline	Control Final	Treatment Baseline	Treatment Final	Control Sample Size	Treatment Sample Size	N	Period	Original Unit	Abs Diff	Rel Change	Significance	Confidence Intervals	CI_lower	CI_upper	Standard Error	p value	Source Location	Notes
Chicago Child Parent Center	The Chicago Child-Parent Center is a half-day early childhood education and family-support program serving low-income children in high-poverty, predominantly Black and Hispanic Chicago neighborhoods. The model combines preschool instruction with parental involvement, outreach services, attention to health and nutrition, and optional K-3 school-age continuation for up to six years. This study evaluates long-term outcomes for CPC participants compared with a non-CPC comparison group.	Chicago, Illinois	Low-income children in high-poverty, predominantly Black/Hispanic Chicago neighborhoods where Title I eligible	1985	N=1,539 (CPC=989, Comparison=550)	Education	Quasi-Experimental	Grade retention	Reduced Grade Retention	Education	Pre-school program; by age 15		0.384		0.23	550	989	1539	By age 15	percentage of group	-0.154	-0.401	Significant					0.001	Table 3, pg 12	Values are extracted from Table 3 on pg 12; does not provide baseline for control or treatment.
Chicago Child Parent Center	The Chicago Child-Parent Center is a half-day early childhood education and family-support program serving low-income children in high-poverty, predominantly Black and Hispanic Chicago neighborhoods. The model combines preschool instruction with parental involvement, outreach services, attention to health and nutrition, and optional K-3 school-age continuation for up to six years. This study evaluates long-term outcomes for CPC participants compared with a non-CPC comparison group.	Chicago, Illinois	Low-income children in high-poverty, predominantly Black/Hispanic Chicago neighborhoods where Title I eligible	1985	N=1,539 (CPC=989, Comparison=550)	Education	Quasi-Experimental	Special education placement	Reduced Special Education	Education	Pre-school program; by age 18		0.246		0.144	550	989	1539	By age 18	percentage of group	-0.102	-0.4146	Significant					p ≤ .001	Table 3, pg 12	Values are extracted from Table 3 on pg 12; no CI or standard error was shown in the context file.
Chicago Child Parent Center	The Chicago Child-Parent Center is a half-day early childhood education and family-support program serving low-income children in high-poverty, predominantly Black and Hispanic Chicago neighborhoods. The model combines preschool instruction with parental involvement, outreach services, attention to health and nutrition, and optional K-3 school-age continuation for up to six years. This study evaluates long-term outcomes for CPC participants compared with a non-CPC comparison group.	Chicago, Illinois	Low-income children in high-poverty, predominantly Black/Hispanic Chicago neighborhoods where Title I eligible	1985	N=1,539 (CPC=989, Comparison=550)	Education	Quasi-Experimental	Child maltreatment	Reduced abuse or neglect	Child Welfare	Pre-school program; within age 4 to 17		0.174		0.099	550	989	1539	Age 4 to 17	ever occurred, pct of group	-0.075	-0.431	Significant	90%				<.001	Table 3, pg 12	Values are extracted from Table 3 on pg 12; this outcome comes from a child welfare domain even though the program domain is Education.
```
## Example extraction_source_log.txt Entry

Use this structure for the companion text log. The exact page should come from the PDF being reviewed; the context file example only identified `Table 3`.

```text
Source: Age-26 Cost-Benefit Analysis of the Child-Parent Center Early Education Program

Shared sources for Rows 1-2:
- Program/Description: p. 4, Program Description section — phrase: "half-day child-care program" — supports Program and Description.
- Location/Population: p. 5, Study Sample section — phrase: "low-income children in Chicago" — supports Location and Population.
- Study design: p. 6, Methods section — phrase: "comparison group" — supports Study Type = Quasi-Experimental.
- Study sample: p. 7, Sample section — phrase: "CPC=989, Comparison=550" — supports Study Sample, Treatment Sample Size, Control Sample Size, and N.


Row 1
Program: Chicago Child Parent Center
Outcome: Reduced Grade Retention
Outcome_Fixed mapping used: Grade retention, because "Reduced Grade Retention" maps to Grade retention.
Group/period: Pre-school program; by age 15.

Outcome-specific sources:
- Outcome values: p. 12, Table 3 — phrase: "grade retention by age 15" — supports Treatment Final, Control Final, p value, Original Unit, and Period.
- CI/SE: not found in reviewed source — supports blank CI_lower, CI_upper, and Standard Error.

Numeric source details:
- Control Final = 0.384; p. 12, Table 3 — phrase: "comparison group grade retention rate by age 15."
- Treatment Final = 0.230; p. 12, Table 3 — phrase: "CPC preschool group grade retention rate by age 15."
- p value = .001; p. 12, Table 3 — phrase: "grade retention by age 15."

Calculation:
- Abs Diff = 0.230 - 0.384 = -0.154.
- Rel Change = (0.230 - 0.384) / 0.384 = -0.4010.

Validation concerns:
- Confirm exact PDF page for Table 3.
- Confirm whether values are reported as percentages or proportions.
- Leave CI and SE blank unless reported elsewhere.


Row 2
Program: Chicago Child Parent Center
Outcome: Reduced Special Education
Outcome_Fixed mapping used: Special education placement, because "Reduced Special Education" maps to Special education placement.
Group/period: Pre-school program; by age 18.

Outcome-specific sources:
- Outcome values: p. 12, Table 3 — phrase: "special education by age 18" — supports Treatment Final, Control Final, p value, Original Unit, and Period.
- CI/SE: not found in reviewed source — supports blank CI_lower, CI_upper, and Standard Error.

Numeric source details:
- Control Final = 0.246; p. 12, Table 3 — phrase: "comparison group special education rate by age 18."
- Treatment Final = 0.144; p. 12, Table 3 — phrase: "CPC preschool group special education rate by age 18."
- p value = p ≤ .001; p. 12, Table 3 — phrase: "special education by age 18."

Calculation:
- Abs Diff = 0.144 - 0.246 = -0.102.
- Rel Change = (0.144 - 0.246) / 0.246 = -0.4146.

Validation concerns:
- Confirm exact PDF page for Table 3.
- Confirm whether values are reported as percentages or proportions.
- Leave CI and SE blank unless reported elsewhere.
```

## Final Checklist

1. One Excel workbook only, with one sheet named Extractor_Results.
2. One row per distinct paper/program/outcome/group/period.
3. No invented numbers and no zeros for missing values.
4. All numeric values have Source Location and detailed support in the TXT log.
5. All other extracted values should have a source page and phrase
6. Abs Diff and Rel Change are calculated only when supported by clear raw values.
7. Concerns and validation flags are captured in the TXT log
