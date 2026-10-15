Student Data Analysis

This project reads a file of students and works out two things:

how many male and female students there are
the average grade point average for each
The three versions
File	What it uses
Student-Data-Analysis.ipynb	Plain Python
numpy version.ipynb	numpy
pandas version.ipynb	pandas

All three give the same results.

Before you start

You need Python 3 and Jupyter Notebook (or VS Code with the Jupyter extension). For the numpy and pandas versions, install the libraries:

pip install numpy pandas
Your data file

The file needs a header row, then one student per line. Two columns are used:

gender, the third column (male or female)
GPA, the fifth column (the grade point average)
ID,class,gender,race,GPA,...
1141,A,male,1,73.47,...
1142,A,female,1,71.22,...
How to run
Open a notebook.
Change FILE_PATH at the top to where your file is saved.
Run the cell.
Example output
Male students: 37
Female students: 68
Average male grade point average: 81.85
Average female grade point average: 83.56
How it works

The program goes through the students one at a time. For each one it adds 1 to the count for their gender and adds their grade point average to that gender's total. At the end, total divided by count gives the average.