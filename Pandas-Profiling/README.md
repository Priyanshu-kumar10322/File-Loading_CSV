# Pandas-Profiling: Automated EDA Report Generator

| Contents                                      |
| --------------------------------------------- |
| [Project Description](#Project-Description)   |
| [Overview](#Overview)                         |
| [Dataset Used](#Dataset-Used)                 |
| [Installation](#Installation)                 |
| [Usage](#Usage)                               |
| [Output](#Output)                             |
| [Key Features](#Key-Features)                 |
| [Requirements](#Requirements)                 |
| [Troubleshooting](#Troubleshooting)           |


## Project Description:

This project demonstrates the power of **ydata-profiling** (formerly pandas-profiling) — an automated Exploratory Data Analysis (EDA) tool that generates comprehensive, interactive HTML reports from datasets with just a few lines of code. Instead of manually writing analysis code, ydata-profiling automatically computes statistical summaries, identifies missing values, detects correlations, and visualizes distributions across all variables.

The project uses the famous **Titanic dataset** to showcase how quickly and efficiently you can gain actionable insights from raw data without writing extensive analysis code.


## Overview:

[#overview](#overview)

**ydata-profiling** automates the repetitive task of data exploration by generating detailed reports that include:

- **Dataset Statistics**: Shape, memory usage, and type information
- **Variable Analysis**: Distribution, uniqueness, missing values, and data types for each column
- **Correlations**: Pearson and Spearman correlation matrices
- **Missing Data Visualization**: Interactive heatmaps showing missing value patterns
- **Alerts & Warnings**: Automatic detection of potential data quality issues
- **Interactive Charts**: Histograms, pie charts, and scatter plots for visual exploration
- **Export Options**: Full reports saved as standalone HTML files


## Dataset Used:

[#dataset-used](#dataset-used)

**Titanic Dataset** — A classic dataset containing passenger information from the RMS Titanic disaster.

**Source**: Local CSV file (`train.csv`)

**Description**: The Titanic dataset includes records of passengers aboard the Titanic, with information about their survival status, demographic details, ticket information, and cabin assignments. This dataset is commonly used for classification and EDA tasks.


## Installation:

[#installation](#installation)

### Step 1: Import Required Libraries

```python
import pandas as pd
import sys as s
```

### Step 2: Check Python Version

```python
s.version
```

### Step 3: Install ydata-profiling

⚠️ **Note**: The `pandas-profiling` package has been deprecated. Use **ydata-profiling** instead:

```bash
pip install ydata-profiling
```

### Step 4: Load Your Dataset

```python
df = pd.read_csv(r"C:\Users\Priyanshu\Downloads\train.csv")
df.head()
```


## Usage:

[#usage](#usage)

### Generate Profile Report

```python
from ydata_profiling import ProfileReport

# Create a profile report for your dataset
profile = ProfileReport(df, title="Titanic Dataset Profile")

# Save the report as an HTML file
profile.to_file("output.html")

# Display the report in Jupyter Notebook (optional)
profile.show()
```

### What Gets Generated

The `ProfileReport` object automatically analyzes:

1. **Dataset Overview**: Total rows, columns, memory usage
2. **Variable Types**: Categorical, numerical, datetime, etc.
3. **Descriptive Statistics**: Mean, median, min, max, quartiles
4. **Missing Data**: Percentage and patterns of null values
5. **Duplicate Analysis**: Identification of duplicate records
6. **Correlation Matrix**: Relationships between numerical variables
7. **Sample Data**: First and last records from your dataset


## Output:

[#output](#output)

### HTML Report (`output.html`)

The generated HTML file is fully interactive and self-contained, allowing you to:

- ✅ Toggle between different variable views
- ✅ Click on column names to expand detailed analysis
- ✅ View interactive visualizations
- ✅ Export insights and statistics
- ✅ Share the report without requiring Python or Jupyter

**Dataset Statistics Preview:**
- Total Records
- Total Variables
- Missing Cells Percentage
- Duplicate Rows
- Memory Usage

**Per-Variable Insights Include:**
- Data type and unique values
- Missing value analysis
- Distribution visualization
- Statistical measures
- Top/bottom values for categorical data


## Key Features:

[#key-features](#key-features)

| Feature | Description |
| --- | --- |
| **Automated Analysis** | No manual coding required for basic EDA |
| **Interactive HTML Reports** | Shareable, standalone HTML files |
| **Comprehensive Statistics** | Complete statistical summaries for all variables |
| **Correlation Detection** | Automatic identification of correlated features |
| **Missing Data Visualization** | Interactive heatmaps of missing value patterns |
| **Data Quality Alerts** | Automatic warnings for potential data issues |
| **Type Inference** | Smart detection of data types (numeric, categorical, datetime) |
| **Performance Optimized** | Handles large datasets efficiently |


## Requirements:

[#requirements](#requirements)

### Python Version
- Python 3.7 or higher

### Dependencies
