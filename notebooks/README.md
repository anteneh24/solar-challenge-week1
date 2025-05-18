# Solar Data Analysis Project

### Project Overview

#### 1. Data Profiling

- Use `df.describe()` to get numerical summaries
- Use `df.isna().sum()` to check for missing values
- Flag columns with >5% missing data

#### 2. Outlier Detection & Basic Cleaning

- Use Z-score method to flag extreme values:

  - Columns: `GHI`, `DNI`, `DHI`, `ModA`, `ModB`, `WS`, `WSgust`
  - Flag rows where `|Z| > 3`

- Handle missing values:

  - Drop rows or impute using column median

- Save cleaned dataset to `data/sierraleone_clean.csv`

#### 3. Time Series Analysis

- Plot `GHI`, `DNI`, `DHI`, `Tamb` against `Timestamp`
- Analyze monthly trends, daily patterns, and spikes

#### 4. Cleaning Impact Assessment

- Compare average `ModA` & `ModB` before vs. after cleaning
- Use group-by flag to visualize changes

#### 5. Correlation & Relationship Exploration

- Heatmap for correlation among:

  - `GHI`, `DNI`, `DHI`, `TModA`, `TModB`

- Scatter plots:

  - `WS`, `WSgust`, `WD` vs. `GHI`
  - `RH` vs. `Tamb`, `RH` vs. `GHI`

#### 6. Wind & Distribution Analysis

- Wind rose for wind direction (WD) and speed (WS)
- Histograms for `GHI` and `WS`

#### 7. Temperature & Humidity Analysis

- Study how relative humidity (RH) affects temperature and radiation

#### 8. Bubble Chart

- Plot `GHI` vs `Tamb` with bubble size = `RH` or `BP`
