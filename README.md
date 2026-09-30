Python Practice Scripts

Just a bunch of small Python exercises I did — data cleaning, some basic stats, reading/writing CSV and JSON files, OOP stuff (classes, inheritance, properties), and a simple password guessing game at the end.

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
