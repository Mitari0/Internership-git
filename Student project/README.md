Requirements

Python 3.8 or newer. No installs needed, just standard library stuff (csv, json, collections).

Running it

If you're running these as separate files or notebook cells, remember each one needs its own imports at the top (csv, json) — they don't carry over between cells.

bash
python filename.py
What's in here

clean_ages — takes a list of ages (some are junk like "N/A" or empty strings) and returns just the valid ones as integers.

word_frequency — counts how many times each word shows up in a sentence. Did it two ways, once by hand and once using Counter because why not.

mean / median / stddev — wrote these from scratch instead of using the statistics module, just for practice.

people.csv stuff — writes a small CSV with some names/ages/cities, then reads it back and does average age + counts people per city.

list comprehensions — even number squares 1-50, and calculating each student's average from a dict of scores.

Dataset class — wraps a list of numbers, has mean/min/max and a normalize function (scales everything 0-1).

DataLoader / CSVLoader / JSONLoader — this is the inheritance one. Both loaders have a .load() method but read different file types, so you can loop through them without caring which is which.

SensorReading — shows how @property works, basically a getter/setter that won't let the value go outside 0-100.

Student / Classroom — classroom holds a list of students, can find the top one or the class average.

Preprocessor / Model / Pipeline — fake mini ML pipeline. normalize -> fit -> predict.

password game — guess the password, 10 tries max, tells you which attempt got it right

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


# NumPy Notes

NumPy lets you work with arrays and numbers fast in Python — basically the base most data/ML libraries like pandas are built on.

## What I covered
- making arrays (ones, zeros, identity)
- slicing/indexing to grab or change parts of an array
- copy() vs just referencing the same array
- determinants (linalg.det)
- min/max/sum with axis 
- reshape()
- sin/cos/tan (radians, not degrees)

## Why it's used
Regular Python lists are slow for big numeric work. NumPy does the same operations way faster since it works on the whole array at once instead of looping through it one by one.

## Where it's used
Pretty much anywhere you're dealing with numbers at scale — data analysis, machine learning, image processing, science/engineering calculations, finance, that kind of thing.



# Pandas

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

# Matplotlib

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