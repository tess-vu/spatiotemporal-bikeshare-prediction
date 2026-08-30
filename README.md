# Spatiotemporal Bikeshare Demand Forecasting: An Equity Audit

**Accounting for Sociotemporal Polychronicity Through Culturally-Informed Interaction Terms**

## Research Position

**This is an equity audit study, not a "prediction optimization" project.**

This research critically examines whether standard bikeshare demand forecasting models systematically underperform in historically underserved neighborhoods. Rather than treating racial demographics as a means to "improve" prediction, I am trying to use them as a **diagnostic lens** to reveal structural inequities embedded in conventional modeling approaches. This is an exercise to challenge my own socio-technical naivety as well as the techno-benevolent narrative that algorithms merely need better data to be fair.

## Table of Contents

- [Overview](#overview)
- [Research Questions](#research-questions)
- [Key Findings](#key-findings-wip)
- [Methodology](#methodology)
- [Data Sources](#data-sources)
- [Repository Structure WIP](#repository-structure-wip)
- [Reproducing the Analysis WIP](#reproducing-the-analysis-wip)
- [Results WIP](#results-wip)
- [Critical Reflections WIP](#critical-reflections-wip)

## Overview

### Problem

Urban mobility algorithms implicitly assume that time is culturally neutral where a trip at 8:00 AM means the same thing in every neighborhood. Standard models treat temporal lags ($t-k$) as uniform predictors, encoding what a **monochronic bias**, which is the assumption that linear clock-regulated behavior is universal.

### Research Gap

Despite advances in spatiotemporal modeling (GCNNs, spatial panel models, etc.), the literature rarely asks **for who do these models fail and why?** Demographic variables are typically treated as static intercept shifters rather than as indicators of fundamentally different temporal rhythms shaped by structural inequality.

### This Study

The goal of using 2024 trip data from Philadelphia's Indego bikeshare system is to:

1. Audit whether standard models produce systematically different prediction errors across neighborhoods of varying racial composition.
2. Investigate whether culturally-informed interaction terms (lag × percent non-white) can reveal—not correct—these disparities.
3. Help quantify the equity implications of using "one-size-fits-all" forecasting systems.

## Research Questions

| Techno-Benevolent Frame | Equity Audit Frame |
|----------------|-------------------|
| *"Does race improve prediction?"* | **Does the standard model perform equitably across neighborhoods of different racial compositions?** |
| *"Can polychronic interactions reduce MAE?"* | **Do polychronic interactions expose where and why the standard model systematically underperforms in historically underserved communities?** |

### Hypotheses

**H1 (Equity Audit):** Standard models exhibit systematically higher prediction errors in neighborhoods with higher proportions of non-white residents, reflecting structural inequalities in data coverage and model calibration.

**H2 (Diagnostic):** Introducing polychronic interaction terms reveals that temporal demand signatures differ across neighborhoods, with the largest model improvements concentrated in communities where the standard model performed worst. Note that this is not because race is predictive, but because the standard model was calibrated on majority-white patterns.

## Key Findings WIP

### Model Performance

### Equity Findings

## Methodology

### Study Area
Philadelphia, PA: Indego bikeshare system (253 stations with valid census tract linkages)

### Temporal Granularity
30-minute intervals, full-year 2024 (Q1–Q4)

### Model Hierarchy

| Model | Description | Purpose |
|-------|-------------|---------|
| **Model 1** | Time + Weather | Baseline. |
| **Model 2** | + Temporal Lags | Standard forecasting approach. |
| **Model 3** | + Demographics (main effects) | "Controlling away" race. |
| **Model 4** | + Station Fixed Effects | Accounting for station heterogeneity. |
| **Model 5** | + Rush Hour × Weekend | Operational interactions. |
| **Polychronic** | + Lag × Race interactions. | **Equity diagnostic model.** |

Rather than treating race as a confounding variable to "control away", I would like to think of it as a **moderator of temporal dynamics**. This allows me to ask if the temporal structure of demand varies systematically across neighborhoods? And what does that tell about the standard model's assumptions?

## Data Sources

| Dataset | Source | Description |
|---------|--------|-------------|
| **Indego Trip Data** | [rideindego.com](https://www.rideindego.com/about/data/) | 2024 Q1–Q4, full trip records (1.27M+ trips) |
| **ACS 5-Year Estimates** | [Census API](https://api.census.gov/data/2023/acs/acs5) | Census tract demographics (income, race, transit use) |
| **Weather Data** | [IEM ASOS PHL](https://mesonet.agron.iastate.edu/request/download.phtml?network=PA_ASOS) | Hourly airport observations (temp, precip, wind) |

## Repository Structure WIP

## Reproducing the Analysis WIP

### Prerequisites

### Setup

### Environment Setup

### Run Analysis

## Results WIP

### Model Performance by Quarter

### Equity Audit Findings

### Bias Detection

## Critical Reflections WIP
