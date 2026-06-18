---
title: Investing in Flourishing Extractor Knowledge Base
Created by: Shams Sadhin
Last Modified: June 17, 2026

---

# Investing in Flourishing Extraction and Validation Knowledge Base

One-page instructions for extracting intervention study evidence into a simplified Excel file and validating that Excel file against the source PDF.

Use this page for a two-step workflow: first create the `Extractor_Results` Excel sheet, then validate that Excel file against the same PDF and produce one memo-sized TXT validation report.

## Project Overview

The Investing in Flourishing literature review extracts structured evidence from intervention studies and reports. The focus is programs for children from prenatal through age 3 for the children and caregiver across multiple social domains such as  healthcare, education, child welfare, employment, and criminal justice outcomes that support the evidence base.

The goal is to capture program details, study design, population, outcomes, baseline/final values, treatment/control values, sample sizes, uncertainty terms, source locations, and effect size calculations which can later support validation, meta-analysis, and simulations.

## Simple Output Schema

Create one Excel workbook with one sheet named `Extractor_Results`. Use these columns in this exact order:

`Program | Description | Location | Population | Year | Study Sample | Program Domain | Study Type | Outcome_Fixed | Outcome | Outcome Domain | Group | Control Baseline | Control Final | Treatment Baseline | Treatment Final | Control Sample Size | Treatment Sample Size | N | Period | Original Unit | Abs Diff | Rel Change | Significance | Confidence Intervals | CI_lower | CI_upper | Standard Error | p value | Source Location | Notes`

Validation is handled after extraction. The validation agent checks the completed Excel file against the PDF and writes one combined memo-style TXT report.

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

## Validation Report TXT File

Create the TXT validation report only after the Excel extraction exists. The validation agent receives two inputs: one source PDF and one Excel workbook with a sheet named `Extractor_Results`.

The validation agent checks every row and every field against the PDF, but the report should be memo-sized and issue-focused. It should not list every field that is correct. Summarize supported rows/fields in 2-3 sentences, then focus on key issues, rows needing correction, rows needing human review, calculation problems, source-location problems, and Outcome_Fixed mapping problems.

### Validation Report Goals

- Confirm whether each row correctly represents the PDF.
- Check every field: Program, Description, Location, Population, Year, Study Sample, Program Domain, Study Type, Outcome_Fixed, Outcome, Outcome Domain, Group, Control Baseline, Control Final, Treatment Baseline, Treatment Final, Control Sample Size, Treatment Sample Size, N, Period, Original Unit, Abs Diff, Rel Change, Significance, Confidence Intervals, CI_lower, CI_upper, Standard Error, p value, Source Location, and Notes.
- Recalculate Abs Diff and Rel Change where the source values support calculation.
- Check that missing numeric values are blank rather than zero.
- Check that modeled estimates are not treated as directly calculated raw effects unless the Notes clearly explain the choice.
- Check that Outcome_Fixed comes from the Outcome_Fixed Mapping table. If no clear mapping exists, leaving Outcome_Fixed blank is acceptable when explained.
- Raise only meaningful issues in the report. Do not produce a long field-by-field list of supported values.

### Validation Decisions

Use these decision labels when discussing issues:

| Decision | Meaning |
|---|---|
| Supported | The value matches the PDF or is a reasonable supported summary. |
| Incorrect | The value conflicts with the PDF. |
| Missing | The PDF reports the value but the Excel field is blank. |
| Not reported | The PDF does not report the value and the Excel handling is appropriate. |
| Ambiguous | The source is unclear or multiple interpretations are possible. |
| Needs human review | The issue cannot be resolved confidently from the PDF alone. |

### Memo-Sized Validation Report Format

Use this format for `validation_report.txt`:

```text
PDF reviewed: [PDF filename]
Excel file reviewed: [Excel filename] (sheet: Extractor_Results)
Number of rows checked: [count]
Overall validation status: Pass / Pass with concerns / Needs correction
Summary: [2-3 sentences. State whether the extraction is broadly faithful, what is generally supported, and the main issues needing attention.]

1. Overall Assessment
[Short paragraph. Mention rows checked, source sections/tables reviewed, and whether the workbook is usable. Summarize what is broadly supported without listing every correct field.]

2. Key Issues Requiring Correction

Issue 1
- Row(s): [row numbers]
- Field(s): [field names]
- Extracted value: [value in Excel]
- Validator finding: [Incorrect / Ambiguous / Needs human review / Schema risk]
- Evidence/Source location: [page, table, figure, section, and concise source explanation]
- Recommended fix: [specific correction or review action]
- Confidence: High / Medium / Low

Issue 2
- Row(s): ...
- Field(s): ...
- Extracted value: ...
- Validator finding: ...
- Evidence/Source location: ...
- Recommended fix: ...
- Confidence: ...

3. Row-Level Concerns
[Group rows by issue pattern. For example: "Rows 1-6 are broadly supported..." or "Rows 7-10 have correct outcome values but the Period field reuses language from a different outcome type." Only discuss rows with concerns or useful caveats.]

4. Calculation Check
[Report whether Abs Diff and Rel Change are correct. Include examples only for high-risk or representative rows. If calculations are broadly correct, say that briefly. If modeled estimates are stored in Abs Diff, explain the schema risk.]

5. Outcome Mapping Check
[Report whether Outcome_Fixed values match the mapping table. Mention blanks that are acceptable because no mapping exists, and identify blanks that should be mapped.]

Rows fully supported: [row numbers or summary]
Rows needing correction: [row numbers]
Rows needing human review: [row numbers]
Common issue patterns: [short list]
Recommended next steps: [numbered action list]
```

### Example Validation Report Style

This example shows the level of detail and tone expected. Adapt the structure to the actual PDF and Excel file being validated.

```text
PDF reviewed: New York State Healthy Neighborhoods Program pdf.pdf
Excel file reviewed: healthy_neighborhoods_extractor_results.xlsx (sheet: Extractor_Results)
Number of rows checked: 12
Overall validation status: Pass with concerns
Summary: The extraction is broadly faithful to the source article. Program description, setting, study design, subgroup definitions, sample sizes, core outcome values, source locations, and most outcome mappings are supported. The main corrections concern the Period field for medication rows and the way modeled cost-savings rows use Abs Diff to store a benefit estimate rather than a directly calculated effect size.

1. Overall Assessment
The workbook is broadly usable. All 12 rows were checked against the PDF, including the abstract, methods/study-sample sections, Tables 2-4, discussion, and the Outcome_Fixed mapping. Most text summaries are reasonable, most numeric values match the PDF, and the simple pre-post calculations for rows based on the medical encounter and medication-use tables are correct.

2. Key Issues Requiring Correction

Issue 1
- Row(s): 7-10
- Field(s): Period
- Extracted value: "91-365 days after initial visit; encounter changes annualized to 12 months"
- Validator finding: Incorrect / partly unsupported for medication rows.
- Evidence/Source location: Methods describe annualized change for medical encounters, while medication use is measured as past-week quick-relief use or daily controller-medication use at initial visit and revisit.
- Recommended fix: Revise Period to reflect initial vs revisit among participants revisited 91-365 days after the initial visit, with medication use measured for the past week.
- Confidence: High

Issue 2
- Row(s): 11-12
- Field(s): Abs Diff; Period
- Extracted value: Abs Diff stores dollar savings estimates.
- Validator finding: Needs human review / schema risk. The dollar amounts are supported, but they are modeled payer benefits rather than direct treatment-final minus treatment-baseline effects.
- Evidence/Source location: Cost-benefit table and methods explain that benefits are calculated by multiplying utilization and medication-use changes by Medicaid unit costs.
- Recommended fix: Keep these rows only if modeled economic-benefit rows are allowed. If retained, clarify that Abs Diff contains a modeled benefit estimate. If the schema expects only raw or directly calculated effects, leave Abs Diff blank and preserve savings in Notes.
- Confidence: Medium

3. Row-Level Concerns
Rows 1-6 are broadly supported. Program, sample, subgroup, baseline/final means, N, source location, and p-values match the paper. Rows 7-10 have supported outcome values and sample sizes, but the Period field should be corrected. Rows 11-12 are supported as modeled savings rows, but they are high-risk schema rows.

4. Calculation Check
For rows 1-10, calculations are correct under a single-arm pre-post convention using Treatment Final - Treatment Baseline for Abs Diff and dividing by Treatment Baseline for Rel Change. No clear recalculation check applies to modeled savings rows because the PDF reports modeled dollar benefits rather than directly computed raw effects.

5. Outcome Mapping Check
Outcome_Fixed mappings are broadly appropriate where mapped. Blank Outcome_Fixed values are acceptable when the mapping table does not contain a clear standardized label for the source outcome wording.

Rows fully supported: Rows with no material issues after existing note caveats.
Rows needing correction: Rows 7-10.
Rows needing human review: Rows 11-12.
Common issue patterns: reused Period language; modeled economic estimates stored in Abs Diff.
Recommended next steps: Correct Period for medication rows; review modeled cost-savings encoding; preserve concise notes explaining p-value and modeling caveats.
```

## Final Checklist

### Extraction Checklist

1. One Excel workbook only, with one sheet named Extractor_Results.
2. One row per distinct paper/program/outcome/group/period.
3. No invented numbers and no zeros for missing values.
4. All numeric values have Source Location.
5. Abs Diff and Rel Change are calculated only when supported by clear raw values.
6. Notes are concise and capture important caveats.

### Validation Checklist

1. Check every row and field in the Excel file against the PDF.
2. Produce one combined TXT validation report for the Excel file.
3. Keep the report memo-sized and issue-focused.
4. Summarize supported rows briefly instead of listing every correct field.
5. Raise key issues with row numbers, fields, evidence locations, recommended fixes, and confidence.
6. Include calculation and Outcome_Fixed mapping checks.
