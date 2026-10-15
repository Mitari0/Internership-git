# Student Data Analysis

This project reads a file of students and works out two things:

- How many male and female students there are
- The average grade point average (GPA) for each

## The three versions

Each version lives on its own branch and gives the same results:

- **Plain Python:** `Student-Data-Analysis.ipynb` (branch `student-data-analysis`)
- **numpy:** `numpy version.ipynb` (branch `numpy-version`)
- **pandas:** `pandas version.ipynb` (branch `pandas-version`)

The plain Python version needs nothing extra. The numpy and pandas versions need their library installed first; see `requirements.txt` in the branch.

## Before you start

You need Python 3 and Jupyter Notebook (or VS Code with the Jupyter extension).

## Your data file

The data is in `students-data.csv`, included in each branch. It has a header row, then one student per line. Two columns are used:

- **gender**, the third column (`male` or `female`)
- **GPA**, the fifth column

```csv
ID,class,gender,race,GPA,...
1141,A,male,1,73.47,...
1142,A,female,1,71.22,...
```

To use your own file, change `FILE_PATH` at the top of the notebook.

## How to run

1. Switch to the branch for the version you want.
2. Open its notebook.
3. Run the cell.

## Example output

```text
Male students: 37
Female students: 68
Average male grade point average: 81.85
Average female grade point average: 83.56
```

## How it works

The program goes through the students one at a time. For each one it adds 1 to the count for their gender and adds their GPA to that gender's total. At the end, total divided by count gives the average.