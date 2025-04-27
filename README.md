Min-wage-unemployment-
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

Install required packages using:
bash pip install pandas numpy matplotlib seaborn scikit-learn; OR see ipynb/jupyter file for further instructions on downloading through python

Directory Structure:
project/
data/
unemployment rate.csv/
minimum wage data file/
/notebooks/
blog.ipynb
scripts/
model.py/
README.md/

Replication Instructions
1. Data Preparation

Place the minimum wage data file in the data/ directory
Place the unemployment rate CSV file in the data/ directory
Open the analysis notebook or run the script to load and prepare the data:

python# Load the minimum wage data using appropriate seperators
min_wage = pd.read_csv("path/to/minimum_wage_file.csv")

Load the unemployment data using appropriate seperators
unemployment = pd.read_csv(
    "path/to/unemployment rate.csv",
    
2. Data Cleaning and Preprocessing

Clean the minimum wage data:

python# Rename columns for consistency
Convert Year to integer

Clean the unemployment data:

python# Drop unnamed columns
Rename columns for consistency
unemployment = unemployment.rename(columns={
    'Country Name': 'Country',
    'Country Code': 'Country Code',
    'Indicator Name': 'Indicator',
    'Indicator Code': 'Indicator Code})

# Drop rows where all year values are NaN
Transform unemployment data from wide to long format:
Define year range as strings
Melt years into a single column

3. Merge Datasets
python# Find common countries between datasets

4. Model Training and Evaluation
Filter for countries of interest:
Create features and target:

# Define features and target
X = model_data_encoded[['Min_Wage_Percent'] + [col for col in model_data_encoded.columns if col.startswith('Country_')]]
y = model_data_encoded['Unemployment_Rate']

Train and evaluate the model:

python# Split the data
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_squared_error, r2_score
# Scale the features
# Train the Random Forest model
# Make predictions
# Evaluate the model
# Calculate percentage contribution of minimum wage


6. Visualization
python - import matplotlib.pyplot as plt
import seaborn as sns

# Visualize feature importance
Additional Analyses
For more advanced analyses, including permutation importance, partial dependence plots, and minimum wage-only models, refer to the complete notebook in the repository.
