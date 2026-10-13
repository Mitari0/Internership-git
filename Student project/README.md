# Student Data Analysis

A small Python project that reads a list of students from a CSV file and tells me two things: how many male and female students there are, and what the average age is for each.

I wrote it without any libraries (no pandas), just plain Python, to practise the basics.

## What you need
- Python 3
- Jupyter Notebook or VS Code with the Jupyter extension

## Your CSV file
It should have a header row and three columns in this order:

```
Name,Age,Gender
```

Gender should be `Male` or `Female`.

## How to run it
1. Open `Student-Data-Analysis.ipynb`.
2. Change `FILE_PATH` at the top to where your CSV is saved.
3. Run the cell.

## What you'll see
```
Male students: 95
Female students: (your number)
Average male age: 22.43
Average female age: 21.68
```

## How it works
It reads the file line by line, drops each age into a list for that gender, then uses `len()` to count and `sum()` to add up and work out the average.

## Pandas

Notes and examples from learning pandas, using a Pokémon dataset as the main practice data.

**What's covered**
- **Series and DataFrames:** creating them from dicts, adding columns and rows, and filtering a Series by value
- **Reading data:** loading CSV and JSON files into a DataFrame
- **Selecting data:** columns, multiple columns, and rows with `loc` (by label) and `iloc` (by position)
- **Searching:** looking up a Pokémon by name, with error handling for names that don't exist
- **Filtering:** conditions such as height and weight thresholds, and combining them with `&` and `|`
- **Aggregation:** `mean`, `sum`, `min`, `max` and `count`, plus `groupby`
- **Data cleaning:** dropping columns, handling missing values (`dropna`, `fillna`), fixing inconsistent values, standardizing text, fixing data types and removing duplicates

**Projects you can build with these skills**
- A Pokémon explorer: search by name, filter by type, height or weight, and find legendary Pokémon
- Comparing stats across groups, such as average height or weight per type
- A data-cleaning pipeline that turns a messy CSV or JSON file into an analysis-ready table
- Record-keeping tools, such as an employee, student or inventory table you can filter and summarize
- Exploratory data analysis (EDA) on any CSV dataset, as a first step before visualization or machine learning

## Matplotlib

Notes from learning data visualization with matplotlib, using small sample data and the Pokémon dataset.

**What's covered**
- Line, bar, pie, scatter and histogram charts
- Styling: titles, labels, colours, grid lines and legends
- Charting pandas data, such as Pokémon counts by type

**What you can build with it**
- A Pokémon type dashboard
- Grade and survey reports
- Charts for exploring any dataset

**Requirements:** Python 3, `pip install matplotlib numpy pandas`, and `data.csv` in the same folder as the notebook.