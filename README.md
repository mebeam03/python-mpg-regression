# Automotive Fuel Efficiency Analysis

**Python | Pandas | SciPy | Seaborn | Linear Regression**

## Project Overview

This project uses Python to examine the relationship between vehicle characteristics and fuel efficiency. Using an automotive MPG dataset, I developed two simple linear regression models to evaluate how horsepower and vehicle model year relate to miles per gallon (MPG).

The objective was to determine whether each variable was statistically significant, compare how much variation in MPG each model explained, and generate predictions based on the regression equations.

## Tools & Libraries

- **Python:** Data analysis and predictive modeling
- **Pandas:** CSV loading and data manipulation
- **SciPy:** Linear regression and statistical testing
- **Seaborn:** Regression plots and data visualization

## Methodology

The dataset was imported from a CSV file into a Pandas DataFrame. Two independent simple linear regression models were created using SciPy's `linregress()` function:

1. **Horsepower vs. MPG:** Examined the relationship between engine horsepower and fuel efficiency.
2. **Model Year vs. MPG:** Examined how fuel efficiency changed across vehicle model years.

Each model was evaluated using four statistics:

- **R²:** Percentage of variation in MPG explained by the model
- **P-value:** Statistical significance of the relationship
- **Slope:** Expected change in MPG for a one-unit increase in the predictor
- **Intercept:** Predicted MPG when the predictor equals zero

Regression plots were generated using Seaborn to visualize the relationships.

## Results

| Metric | Horsepower Model | Model Year Model |
|---|---|---|
| R² | 0.61 | 0.34 |
| Slope | -0.16 | 1.23 |
| Intercept | 39.94 | -70.01 |
| Statistical Significance | p < 0.05 | p < 0.05 |
| Prediction | 125 HP = 20.2 MPG | 1984 = 33.3 MPG |

### Model 1: Horsepower vs. MPG

The horsepower model explained approximately **61% of the variation in MPG**. The negative slope indicates that vehicles with higher horsepower generally have lower fuel efficiency.

The relationship was statistically significant (p < 0.05), suggesting that horsepower is a meaningful predictor of MPG within this dataset.

Using the regression equation, a vehicle with 125 horsepower was predicted to achieve approximately **20.2 MPG**.

### Model 2: Model Year vs. MPG

The model year explained approximately **34% of the variation in MPG**. The positive slope indicates that newer vehicles generally achieved better fuel efficiency.

Although the relationship was statistically significant (p < 0.05), the lower R² suggests that model year alone explains less variation in MPG than horsepower.

The model predicted approximately **33.3 MPG for a vehicle manufactured in 1984**. This estimate should be interpreted cautiously if 1984 falls outside the dataset's observed years.
