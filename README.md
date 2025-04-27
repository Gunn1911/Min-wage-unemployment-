# Min-wage-unemployment-
#This repository contains code and data for analyzing the relationship between minimum wage levels and unemployment rates across Mexico, the United Kingdom, and the United States.
#Project Overview
This project investigates how minimum wage policies (expressed as a percentage of average wages) correlate with unemployment rates. Using Random Forest Regression modeling, the analysis quantifies the contribution of minimum wage levels to unemployment rate variation across different national economies.
Key Findings

Minimum wage levels account for approximately 58.77% of the explained variation in unemployment rates
Country-specific factors account for the remaining 41.23% of the model's explanatory power
The model demonstrates strong predictive ability with an R-squared value of 0.76

Data Sources
This analysis uses two primary datasets:

Minimum Wage Data - Contains minimum wage as a percentage of average wage for various countries
Source: https://data-explorer.oecd.org/vis?df[ds]=DisseminateFinalDMZ&df[id]=DSD_EARNINGS%40MIN2AVE&df[ag]=OECD.ELS.SAE&dq=......&pd=2000%2C&to[TIME_PERIOD]=false&vw=tb

Unemployment Data - Contains unemployment rates for various countries
File: unemployment rate.csv
Source: https://data.worldbank.org/indicator/SL.UEM.1524.ZS

Requirements
To replicate this analysis, you'll need:

Python 3.7 or higher
The following Python libraries:
pandas
numpy
matplotlib
seaborn
scikit-learn
