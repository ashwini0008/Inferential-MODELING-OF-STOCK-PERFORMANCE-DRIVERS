# Inferential Modeling of Stock Performance Drivers

Hey there! This project dives into understanding what really drives stock performance in the Indian market, specifically looking at companies in the Nifty 500 index. Through statistical analysis and inferential modeling, I've tried to uncover patterns between company characteristics and their stock returns.

## What's This About?

I wanted to explore whether certain financial metrics and company attributes could help explain stock performance. The main question was: Do factors like company age, sales growth, leverage, and profitability actually matter when it comes to stock returns? And if they do, how much?

## The Analysis

The notebook (`Nifty500Analysis.ipymb`) contains the full analysis, which includes:

### Data Preparation
- Started with financial data for Nifty 500 companies (April 2023)
- Cleaned the dataset by removing outliers (trimmed at 1st and 99th percentiles)
- Applied quantile normalization to handle non-normal distributions in financial data

### Key Variables Analyzed
- **Market Metrics**: Market Capitalization, Stock Returns (%), Sales Growth (%)
- **Financial Health**: Total Debt, Leverage (%), Book Value per Share
- **Profitability**: Profit After Tax, EPS, Total Expenses
- **Company Profile**: Company Age, R&D Expenses, Beta
- **Age Groups**: Categorized companies into Young, Mid-aged, and Mature

### Statistical Methods Used

1. **Exploratory Data Analysis**
   - Distribution analysis and skewness calculations
   - Q-Q plots to check normality
   - Correlation analysis and VIF calculations for multicollinearity

2. **MANOVA (Multivariate Analysis of Variance)**
   - Tested whether company age groups differ in their stock returns and sales growth
   - Used multiple test statistics: Pillai's trace, Wilks' lambda, Hotelling-Lawley trace, Roy's greatest root
   - Followed up with post-hoc pairwise comparisons

3. **Box's M Test**
   - Checked homogeneity of covariance matrices across age groups

## Main Findings

Without getting too technical, here's what I found:

- There are statistically significant differences in how companies of different ages perform
- The relationship between sales growth and stock returns varies by company maturity
- Younger companies tend to show different patterns compared to mature ones
- The analysis revealed some interesting non-linear relationships that traditional methods might miss

## Technical Setup

The analysis was done in Google Colab, which made it easy to work with Python libraries like:
- pandas and numpy for data manipulation
- matplotlib and seaborn for visualizations
- scipy and statsmodels for statistical tests
- sklearn for data preprocessing

## How to Use This

If you want to replicate or extend this analysis:

1. Open the `Nifty500Analysis.ipymb` notebook in Google Colab or Jupyter
2. Upload your own Nifty 500 dataset (or use similar stock data)
3. The notebook is structured sequentially - just run the cells in order
4. Each section has inline comments explaining what's happening

**Note**: You'll need to adjust file paths if you're running this locally instead of in Colab.

## Data Structure

The analysis expects data with these columns:
- Company incorporation year and age
- Market capitalization and stock prices
- Financial statements data (sales, profit, expenses, debt)
- Beta values
- Age category indicators (Young/Mid/Mature)

## Limitations

A few things to keep in mind:
- This is a snapshot analysis (April 2023 data)
- Market conditions change, so patterns might shift over time
- The dataset was trimmed to remove extreme outliers, which could affect edge cases
- Some assumptions about normality and homogeneity might not hold perfectly


## Author

**Ashwini**

Feel free to explore the notebook and reach out if you have questions or suggestions. This was a learning journey, and I'm sure there's more to discover in this dataset!

