# Methods Assessment of ICLABEL Accuracy in Labeling and Detection of Artifacts and the Impacts on Pediatric EEG Data Results
This repository contained the data and code associated with the submission to Psychophysiology journal, 
"Reliable but Wrong? Automated Detection of Heart Rate Artifacts as a Source of Bias in Pediatric EEG Data"

The study investigates the impact of inaccurate ICLABEL labels on Pediatric EEG data linear model results.

---

## Repository Structure

```
├── torithesis.Rmd        # Main simulation script (annotated)
├── results/            # Folder where simulation results are saved
└── README.md           # This file
```
---

## Requirements

The script was written in **R (≥ 4.2)**. Install required packages:

```r
install.packages(c(
"haven", "tidyverse", "purrr", "broom"
))
```

---

## Running the Code

Run the main script:

```r
source("torithesis.Rmd")
```

- The script will iterate through all conditions specified in the dataset available upon request given the sensitive nature of our dataset.  
- Results are written to `results/` as `.csv` files.  

---
## Analyses Performed

Multiple Linear Regressions using Pre-treatment Theta Beta Ratio, ACE Score, CHAOS Score, Age, and PCIT condition to predict post-treatment TBR. These models were run to explore a binary PCIT score (engagers and control only; Per-Protocol) and a three category PCIT (engagers, nonengagers, control; Intent to Treat) for those only with heartrate in their EEG data (n=27).

Cohen's D were ran to assess bias between the properly cleaned and improperly cleaned datasets. 

## Output

For each condition:

- **`results/torithesis.html`**  
  Contains output for the full subset and heartrate subset.

---

## Supplementary Materials (Optional)

- A copy of supplementary materials also submitted directly to the journal. 
