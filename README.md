# Medical Aid in Dying in Oregon

## Overview

This project uses R to describe participation in Oregon’s Death with Dignity Act from 1998 to 2025 and selected characteristics of people who died following medication ingestion in 2025.

The analysis examines annual participation, age, education, underlying illnesses, hospice enrollment, and insurance coverage. It uses public summary data to describe patterns without making claims about individual decisions or causal relationships.

## Objectives

- Describe annual prescription recipients, reported DWDA deaths, and attending physicians.
- Calculate recent annual percentage changes.
- Summarize participant characteristics and underlying illnesses in 2025.
- Identify implications and questions for further research into end-of-life care.

## Data Source

Data were obtained from the Oregon Health Authority’s [2025 Death with Dignity Act Data Summary](https://www.oregon.gov/oha/PH/PROVIDERPARTNERRESOURCES/EVALUATIONRESEARCH/DEATHWITHDIGNITYACT/Documents/year28.pdf).

| Item | Description |
|---|---|
| Annual participation | Table 2, covering 1998–2025 |
| Participant characteristics and illnesses | Selected sections of Table 1 |
| Reporting cutoff | January 23, 2026 |
| Report revision | June 17, 2026 |
| Data type | Publicly available aggregate counts |

Historical counts follow the updated values in the 2025 report. The 2025 characteristic tables describe 400 reported deaths following medication ingestion, rather than all 637 prescription recipients.

## Methods

Published counts were entered into R data frames. Annual prescription and death totals were checked against the source report.

Analyses included counts, percentages, annual percentage changes, and graphical summaries. Annual percentage change was calculated as the difference from the preceding year divided by the preceding year’s count, multiplied by 100.

Percentages exclude unknown responses where appropriate. Calculated percentages may differ slightly from published percentages because of rounding. Published percentages are identified explicitly where reproduced.

## Results

### Annual Participation from 1998 to 2025

| Year | Prescription recipients | Reported DWDA deaths | Attending physicians |
|---|---:|---:|---:|
| 1998 | 24 | 16 | NA |
| 1999 | 33 | 27 | NA |
| 2000 | 39 | 27 | 22 |
| 2001 | 44 | 21 | 33 |
| 2002 | 58 | 38 | 33 |
| 2003 | 68 | 42 | 42 |
| 2004 | 60 | 37 | 40 |
| 2005 | 65 | 38 | 40 |
| 2006 | 65 | 46 | 41 |
| 2007 | 85 | 49 | 46 |
| 2008 | 88 | 60 | 60 |
| 2009 | 95 | 59 | 64 |
| 2010 | 97 | 65 | 59 |
| 2011 | 114 | 71 | 62 |
| 2012 | 116 | 85 | 62 |
| 2013 | 121 | 73 | 62 |
| 2014 | 155 | 105 | 83 |
| 2015 | 218 | 135 | 106 |
| 2016 | 204 | 139 | 101 |
| 2017 | 218 | 158 | 92 |
| 2018 | 261 | 178 | 108 |
| 2019 | 296 | 193 | 113 |
| 2020 | 373 | 259 | 142 |
| 2021 | 384 | 255 | 132 |
| 2022 | 432 | 305 | 144 |
| 2023 | 561 | 389 | 165 |
| 2024 | 609 | 421 | 132 |
| 2025 | 637 | 400 | 155 |
| **Total** | **5,520** | **3,691** | — |

*NA indicates unavailable information. Annual physician counts should not be summed to estimate unique physicians across years.*

Prescription recipients increased from 24 in 1998 to 637 in 2025. Reported DWDA deaths increased from 16 to 400. Both measures showed substantial long-term growth, although neither increased every year.

### Recent Annual Changes

| Year | Prescription recipients | Reported deaths | Prescription change (%) | Death change (%) |
|---|---:|---:|---:|---:|
| 2021 | 384 | 255 | 2.9 | −1.5 |
| 2022 | 432 | 305 | 12.5 | 19.6 |
| 2023 | 561 | 389 | 29.9 | 27.5 |
| 2024 | 609 | 421 | 8.6 | 8.2 |
| 2025 | 637 | 400 | 4.6 | −5.0 |

*Each percentage compares the year with the preceding year.*

Among these five years, 2023 had the largest percentage increases in both measures. From 2024 to 2025, prescription recipients increased by 28, while reported deaths decreased by 21 at the reporting cutoff.

These measures describe different events and may involve different people. Their changes should be interpreted separately.

### Age Distribution in 2025

| Age group | Count | Percent calculated in R |
|---|---:|---:|
| 18–34 | 2 | 0.5 |
| 35–44 | 2 | 0.5 |
| 45–54 | 9 | 2.2 |
| 55–64 | 34 | 8.5 |
| 65–74 | 132 | 33.0 |
| 75–84 | 145 | 36.2 |
| 85+ | 76 | 19.0 |

*Denominator: 400 reported DWDA deaths. Rounded percentages may not sum to 100%.*

The largest age group was 75–84 years. Overall, 353 of 400 participants (88.3%) were age 65 or older. The report gave a median age of 76 years.

### Education in 2025

| Education | Count | Percent of known responses |
|---|---:|---:|
| 8th grade or less | 5 | 1.3 |
| 9th–12th grade, no diploma | 12 | 3.0 |
| High school graduate or GED | 79 | 20.0 |
| Some college | 66 | 16.7 |
| Associate degree | 34 | 8.6 |
| Bachelor’s degree | 92 | 23.3 |
| Master’s degree | 73 | 18.5 |
| Doctorate or professional degree | 34 | 8.6 |

*Denominator: 395 participants with known education. Education was unknown for five participants.*

Among participants with known education, 199 of 395 (50.4%) had a bachelor’s degree or higher. This distribution does not establish whether education was associated with participation.

### Underlying Illnesses in 2025

| Underlying illness | Count | Published percent |
|---|---:|---:|
| Cancer | 245 | 61.3 |
| Neurological disease | 56 | 14.0 |
| Heart/circulatory disease | 45 | 11.3 |
| Respiratory disease | 26 | 6.5 |
| Endocrine/metabolic disease | 12 | 3.0 |
| Genitourinary disease | 4 | 1.0 |
| Gastrointestinal disease | 3 | 0.8 |
| Infectious disease | 2 | 0.5 |
| Other illnesses | 7 | 1.8 |

*Denominator: 400 reported DWDA deaths. Percentages reproduce the source report and may differ slightly from R calculations.*

Cancer was the most frequently reported underlying illness, followed by neurological disease and heart/circulatory disease. Together, these three categories accounted for 346 of 400 reported deaths (86.5%).

### Selected Specific Diagnoses in 2025

| Broad category | Specific diagnosis | Count | Published percent of all 400 deaths |
|---|---|---:|---:|
| Cancer | Lung and bronchus cancer | 32 | 8.0 |
| Cancer | Pancreatic cancer | 24 | 6.0 |
| Cancer | Brain cancer | 18 | 4.5 |
| Cancer | Breast cancer | 17 | 4.3 |
| Cancer | Prostate cancer | 15 | 3.8 |
| Cancer | Colon cancer | 13 | 3.3 |
| Neurological disease | Amyotrophic lateral sclerosis (ALS) | 30 | 7.5 |

*These diagnoses are included within the broad illness categories above. They are selected diagnoses, not a complete breakdown, and should not be added again to the overall illness totals.*

The report also combined some diagnoses into broader groups, including lymphoma and leukemia (17) and female genital organ cancers (21). Individual diagnoses within these combined groups cannot be separated using the published table.

For several noncancer categories, the report provided examples rather than separate diagnosis counts: COPD for respiratory disease, diabetes for endocrine/metabolic disease, kidney disease for genitourinary disease, liver disease for gastrointestinal disease, and HIV/AIDS for infectious disease. These examples should not be assigned to every person in those categories.

The reported neurological total was 56, while its displayed ALS and other neurological subcategories summed to 55. The main-category value was retained; the discrepancy requires clarification before treating the subcategories as a complete breakdown.

### Hospice Enrollment in 2025

| Hospice status | Count | Percent calculated in R |
|---|---:|---:|
| Enrolled | 367 | 91.8 |
| Not enrolled | 33 | 8.2 |

*Denominator: 400 participants. No hospice responses were unknown.*

Most participants were enrolled in hospice. Hospice enrollment and medical aid in dying frequently coexisted in this population.

### Insurance in 2025

| Insurance | Count | Percent of known responses |
|---|---:|---:|
| Private | 65 | 21.5 |
| Medicare, Medicaid, or other governmental | 238 | 78.5 |
| None | 0 | 0.0 |

*Denominator: 303 participants with known insurance. Insurance was unknown for 97 of 400 participants (24.3%).*

Governmental coverage accounted for most known insurance. No uninsured participants were recorded among known responses, but missing information prevents extending that conclusion to all participants.

## Important Findings and Implications

| Finding | Implication for further research | Interpretation boundary |
|---|---|---|
| Reported participation grew substantially over time. | Examine how participation evolved alongside end-of-life services and policy changes. | Counts do not account for population growth or establish a causal policy effect. |
| Most participants were older adults. | Investigate end-of-life communication and care planning among older adults. | Age distributions alone do not establish age-specific participation rates. |
| Cancer was the most common underlying illness. | Compare disease-specific patterns with an appropriate terminally ill population. | The analysis cannot determine whether people with cancer were more likely to participate. |
| ALS was identified among 30 participants. | Further work could examine experiences across neurological diagnoses. | These counts do not explain individuals’ reasons for participation. |
| Most participants were enrolled in hospice. | Examine how hospice care and medical aid in dying intersect. | Enrollment does not measure care quality, duration, or adequacy. |
| Insurance information was missing for 24.3% of participants. | Assess missingness when studying coverage and access. | Insurance coverage alone does not establish affordability or access. |

## Limitations

- **Aggregate data:** Characteristics cannot be linked across tables to identify individual predictors. For example, this analysis cannot determine the ages or insurance status of the participants with cancer.
- **Different annual cohorts:** Deaths may involve prescriptions written in earlier years. Annual deaths divided by annual prescriptions do not estimate the probability of medication use.
- **Incomplete follow-up and revisions:** Counts reflect the reporting cutoff and may change in subsequent reports.
- **Changes over time:** Reporting practices and eligibility changes, including removal of Oregon’s residency requirement in 2023, affect comparisons.
- **Missing responses:** Unknown values were excluded from relevant percentages and documented separately.
- **Diagnosis detail:** Some illnesses were reported only as broad or combined categories.
- **No comparison population:** Participant characteristics do not establish unequal access or differences in participation likelihood.
- **Generalizability:** Findings describe Oregon’s reported experience and should not be generalized to the entire United States.

## Conclusion

Reported participation in Oregon’s Death with Dignity Act increased substantially from 1998 to 2025. Among reported deaths in 2025, most participants were older adults, cancer was the most common underlying illness, and hospice enrollment was frequent.

The project provides a reproducible descriptive analysis of public surveillance data. Its findings support further questions about disease-specific patterns and end-of-life care, while the available data cannot explain individual decisions or establish causal relationships.

## Future Research

Potential extensions include:

- Comparing participant characteristics with those of people dying from similar terminal illnesses.
- Examining historical changes in underlying illnesses and hospice enrollment using comparable annual measures.
- Describing reported end-of-life concerns.
- Investigating reporting completeness and missing information.

## Software and Reproducibility

R was used for data preparation, descriptive calculations, and visualization. The `pdftools` package was used to extract text from the source PDF.

The analysis script and extracted datasets should be read alongside the source report to verify counts, denominators, and reporting definitions.

## Author

Reshika Rimal

[Professional website](https://reshikarimal.com/)
