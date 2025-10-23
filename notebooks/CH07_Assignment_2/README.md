# Assignment 2: Apply Advanced Techniques to FRED Economic Data

## Objective

Practice the advanced time series analysis techniques you've learned in chapters 4-6 by applying them to real-world economic data from FRED (Federal Reserve Economic Data).

## Dataset: FRED Economic Data

- **Location**: `../../data/FRED/`
- **Download Instructions**: See `../../data/FRED/download.ipynb`
- **What it contains**: Economic indicators including unemployment rate, inflation, S&P 500, and more

## Suggested Practical Cases

Choose one or more of these practical scenarios to work on:

### Case 1: Unemployment and Inflation Analysis
- **Series**: `UNRATE` (Unemployment Rate), `CORESTICKM159SFRBATL` (Core Inflation)
- **Techniques to apply**:
  - Compare multiple time series using pivot/join operations
  - Analyze correlation between unemployment and inflation
  - Apply simple forecasting methods to predict future trends

### Case 2: Economic Recovery Patterns
- **Series**: `UNRATE` (Unemployment), `GDP` (Gross Domestic Product)
- **Techniques to apply**:
  - Resample to different frequencies (monthly to quarterly)
  - Compare recovery patterns across different time periods
  - Forecast economic indicators

### Case 3: Market Performance Analysis
- **Series**: `SP500` (S&P 500 Index)
- **Techniques to apply**:
  - Calculate rolling statistics and returns
  - Resample to weekly/monthly frequencies
  - Apply simple forecasting methods

## Instructions

1. **Download the FRED data** using the instructions in `../../data/FRED/download.ipynb`
2. **Copy relevant notebooks** from chapters 4-6 into this folder
3. **Choose a practical case** from the suggestions above (or create your own)
4. **Modify the notebooks** to work with FRED data instead of the original datasets
5. **Apply the techniques** you've learned:
   - Pivot/join operations to compare multiple series
   - Resampling to different time frequencies
   - Simple forecasting methods

## Additional Resources

For more examples and detailed analysis walkthroughs, check out the **article resources** in the LinkedIn Learning course chapter.

## Tips

- FRED data is already clean and well-structured, making it easier to focus on analysis techniques
- Each economic indicator has different frequencies (daily, monthly, quarterly) - experiment with resampling
- Try combining multiple indicators to discover interesting relationships

Good luck with your analysis!
