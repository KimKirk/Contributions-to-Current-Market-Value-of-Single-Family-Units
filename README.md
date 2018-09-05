# Contributions-to-Current-Market-Value-of-Single-Family-Units
- Finance: Housing
- Inferential data analysis was conducted using multivariate linear regression to determine factors that influence current market value of single family housing units for 2013.
- All files are self-contained analysis reports that include necessary variables. 

## Processing Instructions:
- Data Analysis is in pdf. Here: https://drive.google.com/file/d/1s8KiauTb_czfBtc8nFSTezJrqVk33zky/view?usp=sharing 
- Data Analysis Report is in pdf.
- Codebook is in pdf.

## Steps to Transformation:
### Data was tidied by: 
- All data points for VALUE variable less than $1000.00 were removed per stakeholder input.
- NULL values represented 2% of the data. All NULL values were removed per stakeholder input. Missing values were missing because the original data source has odd-numbered years in 1985-2009 and "selected only records representing completed interviews for occupied and vacant units, excluding usual residence elsewhere (URE) and noninterview records." per HADS documentation file. https://www.huduser.gov/portal/datasets/hads/HADS_doc.pdf
- Houses, apartments, and flats were housing unit types included in the analysis per stakeholder input.
- Single family housing units included in the analysis per stakeholder input.
- Owner occupied, vacant for sale, and sold but not occupied housing units included in the analysis per stakeholder input.

1. Dataset was downloaded from host website: https://www.huduser.gov/portal/datasets/hads/hads.html
2. Data was cleaned to include only single-family houses, flats, apartments with Fair Market Value of at Least $1000.00 owned in 2013 as this was the subset that stakeholders wanted to focus on.
3. VALUE was determined to be the outcome variable.
4. BEDRMS, LMED, FMR, BUILT, ROOMS, UTILITY, REGION, METRO3, OTHERCOST, ZINC2, AGE, ZADEQ, PER, VALUE were determined to be the predictor variables.
5. VALUE, OTHERCOST, ZINC2, LMED, FMR had exponential distributions and a natural logarithmic transformation was applied to better approximate a normal distribution.
6. New variables created include:
  - LN_VALUE
  - LN_OTHERCOST
  - LN_ZINC2
  - LN_LMED
  - LN_FMR 
7. Worksheets were created to hold four categories for the analysis:
  - Summary Report identifies and answers the business question/what was measured
  - Descriptive Statistics identifies and calculates descriptive statistics
  - Graphs displays histograms, scatterplots, bar graphs
  - Statistical Tests holds results for statistical tests
