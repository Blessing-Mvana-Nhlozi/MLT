# Trends of Thermal Structure in the MLT Region Using SABER Observations Over Sutherland, South Africa

## Project Overview

This MSc project investigates the **thermal structure trends in the Mesosphere-Lower Thermosphere (MLT) region** using **SABER (Sounding of the Atmosphere using Broadband Emission Radiometry)** observations over **Sutherland, South Africa**. The study aims to understand long-term temperature trends, vertical structure variability, and the influence of climate and solar drivers in a Southern Hemisphere mid-latitude location that is underrepresented in current MLT research.

## Project Structure

```

MLT/
│
├── Data/
│   ├── raw/       # Original SABER datasets
│   └── processed/ # Cleaned and aggregated data
│
├── Code/
│   ├── notebooks/ # Jupyter notebooks for exploration and analysis
│   └── scripts/   # Python scripts and utilities
│
├── Plots/
│   ├── exploratory/ # Initial visualizations
│   └── final/       # Publication-ready figures
│
├── docs/          # Documentation, notes, references
│
└── README.md      # Project description and instructions

```
## Problem Statement

Despite SABER’s long-term MLT temperature data, there is a **knowledge gap** in understanding localized trends in the Southern Hemisphere, particularly over Sutherland. Most MLT studies focus on Northern Hemisphere mid-latitudes or equatorial regions, limiting our understanding of hemispheric asymmetries, regional climate sensitivity, and wave-mean flow interactions in the South African context.

Traditional statistical methods (e.g., linear regression, Mann-Kendall, Sen’s slope) are widely used but often fail to capture **nonlinear, multiscale variability** driven by climate oscillations like ENSO, QBO, and solar-geomagnetic activity. Deep Learning (DL) techniques, such as LSTM and CNNs, have shown promise in atmospheric time-series forecasting, but their application to SABER datasets and integration with physical constraints via **Physics-Incorporated Neural Networks (PINN)** remains underexplored.

This study addresses two main challenges:  
1. Closing the spatial and hemispheric data gap in MLT trend analysis.  
2. Exploring the effectiveness of DL techniques alongside traditional statistical models for forecasting MLT temperatures and understanding their response to dynamic climate drivers.

## Aim and Objectives

**Aim:**  
To investigate the trend and variability of the thermal structure of the MLT region using TIMED/SABER satellite measurements.

**Objectives:**  
1. Analyze the vertical structure of MLT temperature trends across different altitudes, identifying altitude-dependent patterns.  
2. Quantify long-term temperature trends over Sutherland using **Innovative Trend Analysis (ITA)** and non-parametric methods (Mann-Kendall, Sen’s slope).  
3. Simulate and project MLT temperature evolution using the **Trend-Run Method**.  
4. Evaluate the influence of climate and solar drivers: **F10.7 solar flux, QBO, and ENSO**.  
5. Explore DL models (LSTM, CNN) for forecasting MLT temperatures and uncovering nonlinear relationships with climate drivers.

## Research Questions

1. What are the long-term trends and variabilities in MLT temperature over Sutherland?  
2. How do climate drivers modulate MLT temperature variability?  
3. Can statistical and DL models effectively simulate and forecast MLT temperatures?  
4. How well do DL models capture nonlinear dynamics in MLT temperature evolution?

## Study Area

The study focuses on **Sutherland, South Africa (32.38°S, 20.81°E)**, located on the Karoo semi-arid plateau at ~1,450 m elevation. Sutherland is known for clear skies, low atmospheric pollution, and minimal representation in MLT climatology studies, making it ideal for localized analysis.

## Data and Instrumentation

**SABER Instrument:**  
- Aboard NASA's **TIMED satellite** since 2002.  
- Measures **infrared emissions from CO₂** in the upper atmosphere, providing vertical temperature profiles.  

**Atmospheric Drivers Considered:**  
- **Solar activity (F10.7 index)**: Modulates upper-atmosphere heating.  
- **Quasi-Biennial Oscillation (QBO)**: Periodic equatorial stratospheric wind reversals (~28 months).  
- **El Niño–Southern Oscillation (ENSO)**: Influences interannual temperature variability.  

## Methodology

### Statistical Trend Detection
- **Mann-Kendall (MK) Test:** Detects monotonic trends.  
- **Sequential MK (S-MK) Test:** Identifies onset points of trends.  
- **Sen’s Slope Estimator:** Quantifies trend magnitude.  

### Trend Simulation
- **Trend-Run Model & Multiple Linear Regression (MLR)** applied to deseasonalized SABER temperatures.  
- Allows decomposition of variability and evaluation against observed data.

### Physics-Incorporated Deep Learning (PINN)
- Implements **LSTM or MLP networks** constrained by physical laws (e.g., energy conservation).  
- Networks trained with Bayesian regularization, dropout, early stopping, and L2 regularization.  
- Common activation functions: **tanh, ReLU**.  
- Incorporates climate drivers (F10.7, Kp index) into the training process.

### Computational Tools
- **Python libraries**: `pandas`, `xarray`, `numpy`, `scipy`, `statsmodels`, `matplotlib`, `seaborn`, `TensorFlow`.  
- Facilitates preprocessing, trend analysis, visualization, and DL modeling.





## Model

![Temperature Time-Height Heatmap](plots/model/Temperature%20Time-Height%20Heatmap%20(2).png)
