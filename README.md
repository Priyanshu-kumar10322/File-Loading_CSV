# File-Loading_CSV

| Contents                         |
| ---------                        |
| Introduction                     |
| Loading Methods                  |
| Encoding Handling                |
| Quick Reference                  |

## Introduction:

Loading CSV files is one of the most fundamental tasks in data science and Python programming. Whether you're working with data locally on your machine, fetching from remote URLs, or pulling from GitHub repositories, understanding the different methods and their nuances is crucial. This notebook provides a comprehensive guide to loading CSV files efficiently and handling common issues that arise in real-world scenarios.

## Loading Methods:

## Method 1: Loading from Local Files

The most straightforward approach to load CSV files stored on your computer.

Parameters:

1. `filepath_or_buffer` : Path to the CSV file
2. `sep` : Delimiter used in the file (default: ',')
3. `header` : Row number to use as column names (default: 0)
4. `index_col` : Column to use as index

## Method 2: Loading from URLs

Load CSV files directly from web addresses without downloading them first.

Note: Ensure the URL points to the raw content, not the GitHub webpage.

## Encoding Handling:

Character encoding issues are common when working with CSV files from different sources. Here's how to handle them:

Common encodings used in CSV files:

1. `UTF-8`      - Universal, supports all languages (default)
2. `Latin-1`    - Western European characters
3. `ISO-8859-1` - Similar to Latin-1
4. `CP1252`     - Windows encoding
5. `ASCII`      - Basic English characters only

## Quick Reference

1. `Loadfromfile`         - pd.read_csv('file.csv')
2. `Load from URL`        -  pd.read_csv('https://...')
3. `Specify encoding`     -  pd.read_csv('file.csv', encoding='latin-1')
4. `Select columns`       - pd.read_csv('file.csv', usecols=['col1', 'col2'])
5. `Skip rows`            - pd.read_csv('file.csv', skiprows=5)
6. `Read chunks`          - pd.read_csv('file.csv', chunksize=1000)Set
7. `index`                - pd.read_csv('file.csv', index_col=0)
8. `Custom delimiter`     - pd.read_csv('file.csv', sep=';')
