# ML Pipeline for Automated Sleep Staging and PLAS Responsiveness Analysis

**Master's Thesis in Digital Neuroscience**

## Overview

Slow-wave sleep (SWS) plays an important role in memory consolidation and metabolic clearance, but it declines with age and may be particularly impaired in individuals with mild cognitive impairment (MCI). This contributes to a potential *vicious cycle* in which disrupted sleep and neurodegeneration exacerbate one another.

This Master's thesis is embedded in a longitudinal clinical trial investigating **phase-locked auditory stimulation (PLAS)** as a non-invasive approach to enhance slow-wave sleep and potentially support cognitive health in older adults with cognitive impairment. The intervention is delivered in a home environment to capture sleep under ecologically valid conditions.

A major challenge in PLAS research is the substantial **interindividual variability in treatment response**. This project therefore investigates whether machine learning can be used to characterize sleep and identify individuals who are more likely to benefit from PLAS.

## Project Aims

The project consists of two main components:

### 1. Automated Sleep Staging

The first component focuses on implementing an **automated sleep staging pipeline** using single-channel EEG, EMG and EOG.

A machine learning-based approach will be used to classify sleep stages from multi-night home recordings. Automated staging can provide an efficient and consistent alternative to manual scoring and enables the extraction of sleep microstructural features from a large number of recordings.

Potential features include:

* Slow oscillation (SO) power
* SO–spindle coupling strength
* Resultant Vector Length (RVL)
* Coupling directionality / Phase Slope Index (PSI)
* Other macro- and microarchitectural sleep features

### 2. Prediction of PLAS Responsiveness

The second component investigates whether **individual responsiveness to PLAS** can be predicted using supervised machine learning.

Potential predictors include:

* Sleep micro- (and possibly macro-) structural features derived from the sleep staging pipeline
* Clinical characteristics (e.g., age, Montreal Cognitive Assessment score)
* Intervention dosage (e.g., number of stimulation nights)

The ultimate goal is to identify characteristics associated with greater benefit from PLAS and contribute to the development of more **personalized, home-based sleep interventions**.

## Research Pipeline

```text
Home-based sleep recordings
            │
            ▼
     Automated sleep staging
            │
            ▼
   Sleep microstructure features
            │
            ├───────────────┐
            ▼               ▼
  Intervention data    Clinical data
            │               │
            └───────┬───────┘
                    ▼
       Supervised machine learning
                    │
                    ▼
        Prediction of PLAS response
```

## Data

The project uses multi-night home sleep recordings collected as part of a longitudinal clinical trial ([NCT04277104](https://www.humanforschung-schweiz.ch/en/trial-search/study-detail/66026/translate/de/?cHash=105e634800a84f66c64b62dbb39d7474)) involving older adults with cognitive impairment.

**Participant-level clinical and physiological data are not included in this repository.** Access to the underlying data is restricted according to the applicable study, institutional, and data-protection requirements.


## Project Status

🚧 **Work in progress**

The exact research question, methodology, features, and machine learning approaches are still being refined. This repository documents the development of the thesis project and may therefore contain experimental code and analyses.

## Thesis

**Working title:**

> *From automated sleep staging to personalized intervention: How effectively can machine learning utilize microstructural markers to predict individual responsiveness to home-based auditory stimulation in older adults with cognitive impairment?*

**Degree:** MSc Digital Neuroscience

**Institution:** University of Fribourg

**Supervision:** Prof. Björn Rasch (University of Fribourg), Prof. Thomas König (University of Bern) and Korian Wicki (PhD Student, University of Bern)
