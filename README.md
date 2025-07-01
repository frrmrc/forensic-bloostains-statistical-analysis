![Statistical Analysis](https://img.shields.io/badge/Method-Statistical%20Analysis-blue)
![Forensic Analysis](https://img.shields.io/badge/Domain-Forensic%20Analysis-red)
![ImageJ](https://img.shields.io/badge/Tool-ImageJ-green)
![Excel](https://img.shields.io/badge/Analysis-Excel-orange)
![Academic Project](https://img.shields.io/badge/Type-Academic%20Project-purple)
# Statistical Analysis of Blood Dispersion in Backspatter
**Disclaimer** 

This is the first project I worked on at ITS and I created it for the Statistics Fundamentals exam (February 2025).
I started working on it around December 2024 without any experience in Data Analysis, which is why the analysis may appear somewhat basic and not carried out with the best tools.
I still consider it to be a well-structured project of considerable depth that can offer interesting insights for future analyses.
It would be interesting to do clustering and classification tasks considering that the original dataset is very well done and quite rich (for the topic).

## Project Overview

Forensic analysis of blood backspatter when a projectile hits a body, focusing on the relationship between shooting distance, dispersion and stain size.

**Course:** Statistics Fundamentals  
**Date:** February 2025  

## Objectives

- Examine the relationship between **shooting distance** and **spatter characteristics**
- Compare dispersion patterns between different firearms
- Analyze the effect of environmental conditions (temperature, humidity)

## Dataset and Methodology

### Dataset used
**Disclaimer**: _The original dataset consists of 68 experiments conducted under different circumstances, I selected 16 to maintain a certain coherence and focus only on some variables_
- **16 scans** of the supports used as 'target surface' relating to 16 experiments. [Download the portion of dataset I used](https://www.kaggle.com/datasets/marcoferrarini/bpa-scans/data)
- **Source:** [A data set of bloodstain patterns for teaching and research in bloodstain pattern analysis: Gunshot backspatters](https://www.sciencedirect.com/science/article/pii/S2352340918314689?via%3Dihub#s0010) 
- **Original experimental conditions:**
  - Porcine blood with anticoagulant (10ml per test)
  - Tested distances (intended as distance between the paper sheet and the blood container): 30, 60, 90, 120 cm
  - Weapons: Smith & Wesson 9mm and Rock River Arms .223"

### My analytical contribution
- **Digital processing** of scans with [ImageJ](https://imagej.net/ij/)
- **Quantitative extraction** of measurements from images
- **Statistical analysis** of extracted data

### Variables extracted with ImageJ
- **Count** of stains per image
- **Area measurement** (individual stains and total covered area)
- **Spatial coordinates** (x,y position of each stain)

### Environmental conditions
- **Pistol (H):** T: 18°C ±2, RH: 70% ±5
- **Rifle (R):** T: 14.5°C ±1, RH: 55% ±5
- *Documented exceptions for specific experiments*

## Main Results

### Statistical correlations identified

**Pistol (low energy):**
- Covariance (distance, n° stains): -95.390,6
- Covariance (distance, average area): -1,39443

**Rifle (high energy):**
- Covariance (distance, n° stains): -107.812
- Covariance (distance, average area): -11,9196
- Greater fragmentation compared to pistol

### Identified patterns
- **Distance ↗ = Number of stains ↘, Average area ↗**
- **Weapon power ↗ = Fragmentation ↗**
- **Environmental conditions** significantly influence patterns

## Tools and Techniques

- **ImageJ:** Processing and quantitative analysis of scans
  - Stain segmentation
  - Morphometric parameter measurement
  - Spatial coordinate extraction
- **Excel:** Statistical analysis of extracted data
  - Covariance and correlation calculations
  - Data aggregation by experimental condition
  - Comparative graphs for result interpretation

## Repository Structure

```
forensic-bloodstain-analysis/
├── README.md
├── analysis/
│   ├──statistical_analysis_rifles.xlsx
│   └──statistical_analysis_guns.xlsx
└── presentation/
    └── bloodstain_analysis_presentation.pdf

```

## Research Questions Addressed

1. **How does stain distribution change with distance?**
   - Inverse relationship statistically confirmed
   
2. **Do the two weapons produce different patterns?**
   - Rifle shows greater fragmentation and dispersion,
   - Covariances (distance, _other variable_) have more "extreme" values in the case of the rifle
   
3. **Effect of environmental conditions?**
   - Temperature and humidity have some influence

## Skills Demonstrated

- **Scientific image processing** with ImageJ
- **Statistical analysis** of experimental datasets
- **Quantitative interpretation** of physical phenomena
- **Scientific communication** of technical results
- **Rigorous methodology** in data management (thresholds, bias)

================================================================
## Take a look at the pdf in the presentation folder!
