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

