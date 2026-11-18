DATA DICTIONARY

Project

Pharmacoepidemiological Analysis of Polypharmacy and Multimorbidity Using NHANES Data.

1. Introduction

This document describes the variables used in the NHANES datasets selected for this project.

Three major datasets are being explored:

1. Demographics (DEMO)
2. Medical Conditions (MCQ)
3. Prescription Medications (RX)

The participant identification variable SEQN is used to link records across datasets.

2. Demographic Variables (DEMO)

Variable| Description| Research relevance
SEQN| Participant identification number| Dataset linking
RIDAGEYR| Age in years| Age distribution
RIAGENDR| Sex| Sex-based comparisons
RIDRETH3| Race and ethnicity| Population characteristics

3. Medical Condition Variables (MCQ)

The Medical Conditions Questionnaire contains information about participants' reported medical conditions.

Variables being investigated include:

Variable| Description
SEQN| Participant identification number
MCQ010| Asthma-related questionnaire item
MCQ160A| Arthritis
MCQ160B| Congestive heart failure
MCQ160C| Coronary heart disease
MCQ160D| Angina
MCQ160E| Heart attack
MCQ160F| Stroke
MCQ160G| Thyroid problem
MCQ160H| Chronic bronchitis
MCQ160I| Liver condition
MCQ160J| Thyroid cancer

Note: Variable meanings and eligible chronic conditions must be verified against the NHANES documentation for the selected survey cycle before analysis.

4. Prescription Medication Variables (RX)

Variable| Description| Research relevance
SEQN| Participant identification number| Dataset linking
RXDUSE| Prescription medication use indicator| Medication use
RXDDRUG| Prescription medication name| Drug identification
RXDDRGID| Prescription drug identifier| Drug identification
RXDRSD1| First reported reason for medication use| Medication indication

Additional prescription variables will be documented after reviewing the official NHANES codebook.

5. Derived Research Variables

The following variables are planned for creation during data processing:

Derived variable| Description
Medication_Count| Number of eligible prescription medications per participant
Polypharmacy_Category| Medication burden classification
Multimorbidity_Count| Number of eligible chronic conditions
Multimorbidity_Status| Presence or absence of multimorbidity

6. Medication Burden Classification

Category| Definition
No medication use| Zero reported prescription medications
No polypharmacy| 1–4 medications
Polypharmacy| 5–9 medications
Hyperpolypharmacy| 10 or more medications

7. Data Processing

Python libraries used:

- Pandas
- NumPy
- Matplotlib

Data processing includes:

- Dataset inspection
- Missing-value assessment
- Duplicate participant identification
- Dataset merging using SEQN
- Participant-level medication counting
- Classification of medication burden

8. Data Quality Considerations

The following checks will be performed:

1. Participant ID consistency.
2. Duplicate records.
3. Missing medication identifiers.
4. Medication-count validation.
5. Missing clinical information.
6. Verification of variable coding and definitions.

9. References

National Health and Nutrition Examination Survey (NHANES).

Official website: https://www.cdc.gov/nchs/nhanes/

NHANES documentation and codebooks will be used to verify all variable definitions.

10. Document Status

Working document. Variable definitions and derived variables will be updated after verification against the official NHANES documentation.
