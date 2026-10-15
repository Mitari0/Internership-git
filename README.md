# Student Data Analysis

This project reads a file of students and works out two things:

- How many male and female students there are
- The average grade point average (GPA) for each

## The three versions


## Before you start

You need Python 3 and Jupyter Notebook (or VS Code with the Jupyter extension). For the numpy and pandas versions, install the libraries:

```bash
pip install numpy pandas
```

## Your data file

The file needs a header row, then one student per line. Two columns are used:

- **gender**, the third column (`male` or `female`)
- **GPA**, the fifth column (the grade point average)

```csv
ID,class,gender,race,GPA,...
1141,A,male,1,73.47,...
1142,A,female,1,71.22,...
```

## How to run

1. Open a notebook.
2. Change `FILE_PATH` at the top to where your file is saved.
3. Run the cell.

## Example output

```text
Male students: 37
Female students: 68
Average male grade point average: 81.85
Average female grade point average: 83.56
```

## How it works

The program goes through the students one at a time. For each one it adds 1 to the count for their gender and adds their grade point average to that gender's total. At the end, total divided by count gives the average.