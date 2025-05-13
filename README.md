# This code supports the data analysis phase of a single-blind, randomized clinical control trial for insomnia treatment in military Veterans. Repository details will be updated with additional details upon publication.

## File 1: RCT Data Cleaning

### Initial setup and data loading
* Project Directory paths named
* Function creates folder struture for project outputs
* Package libraries imported with conflict preferences declared
* Raw data .csv read in - raw data in sparse, long, longitudinal format output from REDCap

### Longitudinal data cleaning
* Single timepoint measures filtered and renamed in short format
* Double timepoint measures filtered and renamed in short format
* Triple timepoint measures filtered and renamed in short format
* Daily diary timepoint measures filtered and renamed in short format
* All variables combined with merge on participant ID

### Feature engineering and data quality check
* Calculated time difference variables between all timepoints
* Update all variables to proper data types in R
* Calculate descriptive statistics to assess distributions, outliers, and missing data points


## File 2: RCT Confirmation Testing
* Statistical testing of baseline differences between treatment and control group
* T-test (numerical) and Fisher test (categorical)
* Dropout point
* Demographics
* Symptom severity
* Symptom profiles
* Medication use
* Comorbidities
* Daily diary metrics

## File 3: RCT Modeling

### Per Protocol
* Per protocol analysis of primary and secondary aims using linear mixed effects models (group x. time)
* Per protocol moderator analysis using generalized linear model (outcome measure change ~ baseline symptoms values)
* Per protocol mediator analysis using bootstrap linear model for standardized coefficients of variance (outcome measure change ~ symptom change)

### Intent-to-treat
* Data imputed using multiple imputations 
* Primary and secondary aims analysis using linear mized effects models (group x. time)

# Primary Findings
* Active treatment offered statistically significant improvement in symptoms compared to control treatment
* No significant moderators
* Treatment effect mediated by change in depression symptoms and sleep behavioral change
