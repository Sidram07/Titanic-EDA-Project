# Titanic Exploratory Data Analysis

A beginner-friendly, reproducible analysis of Seaborn's Titanic dataset using Python, pandas, NumPy, Matplotlib, and Seaborn. It follows the InternCircle Project 01 guide: inspect the data, document missing values, clean with reasons, check duplicates and types, compare survival patterns, and report three findings with numbers.

> **About these results:** This is a fresh reference analysis using `seaborn.load_dataset("titanic")`. It is not a copy of your completed Colab notebook or its exact results. The notebook calculates results when you run it.

## Questions

1. Did survival differ by sex?
2. Did passenger class relate to survival?
3. How did survival vary across age bands?

## Files

- `Titanic_EDA_Project_01.ipynb` — guided analysis, from loading to findings
- `requirements.txt` — Python packages
- `.gitignore` — common local and generated files to exclude from Git
- `screenshots/` — optional location for exported charts

## Run in Google Colab

1. Extract this ZIP or upload the notebook to Google Drive.
2. In Colab, choose **File → Upload notebook** and select `Titanic_EDA_Project_01.ipynb`.
3. Choose **Runtime → Run all**. An internet connection is needed to fetch the dataset.
4. Review the generated tables, charts, and three numbered findings.

## Run locally

Use Python 3.10 or newer:

```bash
python -m pip install -r requirements.txt
jupyter notebook Titanic_EDA_Project_01.ipynb
```

## Cleaning decisions

- Fill missing `age` values with the median for the same passenger class and sex, falling back to the overall median if needed.
- Drop `deck` from the analysis copy because it is mostly empty; the notebook reports its exact missing count and percentage first.
- Fill missing `embarked` values with the most common port.
- Report exact duplicate rows before and after cleaning. Do not delete automatically: identical values alone do not prove erroneous records.
- Verify numeric analysis columns and convert category-like fields to pandas categories.

The notebook includes `shape`, `head`, `info`, `describe`, missing-value counts and a chart, grouping and aggregation by sex/class/age band, visualizations, and three dynamically calculated, one-sentence findings with percentages and group sizes. These descriptive patterns do not establish cause.

## Data source

The notebook loads the Titanic dataset distributed with Seaborn via `sns.load_dataset("titanic")` ([documentation](https://seaborn.pydata.org/generated/seaborn.load_dataset.html)). This educational dataset is not a complete historical passenger manifest. This package loads it at runtime and does not bundle a copy.
