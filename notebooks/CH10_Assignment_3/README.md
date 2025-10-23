# Assignment 3: Feature Engineering with Period Discretization

## Objective

Build upon your work from Assignment 2 by applying advanced feature engineering techniques, including categorical variables and period discretization to analyze how economic relationships change over time.

## Dataset: FRED Economic Data

- **Location**: `../../data/FRED/`
- **Download Instructions**: See `../../data/FRED/download.ipynb`
- **What it contains**: Economic indicators including unemployment rate, inflation, S&P 500, and more

## Key Concept: Period Discretization

In this assignment, you'll add **categorical period variables** to your analysis to compare how relationships differ across time periods:

- **Pre- and Post-COVID** (before/after 2020-03)
- **Pre- and Post-2020** (before/after 2020-01-01)
- **Economic expansion vs. recession periods**
- **Different presidential administrations**
- **Or any other meaningful time period segmentation**

## Suggested Practical Cases

Extend the cases from Assignment 2 with period discretization:

### Case 1: Unemployment and Inflation Across Time Periods
- **Series**: `UNRATE` (Unemployment Rate), `CORESTICKM159SFRBATL` (Core Inflation)
- **New techniques to apply**:
  - Create categorical variable for pre/post-COVID periods
  - Compare regression coefficients across different periods
  - Analyze how the unemployment-inflation relationship changed
  - Use feature engineering techniques from CH09

### Case 2: Economic Recovery Pattern Comparison
- **Series**: `UNRATE` (Unemployment), `GDP` (Gross Domestic Product)
- **New techniques to apply**:
  - Discretize into expansion vs. recession periods
  - Create lagged features and rolling statistics
  - Compare model performance across different economic regimes

### Case 3: Market Performance in Different Eras
- **Series**: `SP500` (S&P 500 Index)
- **New techniques to apply**:
  - Segment by decade or major market events
  - Create categorical features for different market conditions
  - Build separate models for each time period

## Instructions

1. **Start with your Assignment 2 notebooks** (or copy relevant notebooks from CH07)
2. **Download the FRED data** using the instructions in `../../data/FRED/download.ipynb`
3. **Review techniques** from CH08 (Categorical) and CH09 (Feature Engineering)
4. **Add period discretization**:
   - Create a categorical variable to segment your time series
   - Example: `df['period'] = df.index < '2020-03-01'` then map to 'Pre-COVID' / 'Post-COVID'
5. **Apply feature engineering** techniques from CH09:
   - Create lagged features
   - Calculate rolling statistics
   - Build engineered features specific to your analysis
6. **Compare models** across different time periods

## Getting Started Example

Here's a quick example to get you started:

```python
import pandas as pd

# Load your data
df = fred.get_series('UNRATE')

# Create period discretization
df['period'] = 'Pre-COVID'
df.loc[df.index >= '2020-03-01', 'period'] = 'Post-COVID'

# Now you can analyze separately or use as a categorical feature
pre_covid = df[df['period'] == 'Pre-COVID']
post_covid = df[df['period'] == 'Post-COVID']

# Or use in regression models with categorical encoding
```

## Additional Resources

For more examples and detailed analysis walkthroughs, check out the **article resources** in the LinkedIn Learning course chapter.

## Tips

- Choose meaningful breakpoints that correspond to real economic events
- Compare statistical properties (mean, variance, trends) across periods
- Use visualizations to show how relationships differ across time periods
- Consider whether relationships are stable or change over time

Good luck with your analysis!