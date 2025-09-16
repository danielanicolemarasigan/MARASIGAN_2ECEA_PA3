# MARASIGAN_2ECEA_PA3

This repository contains python scripts/codes solving the 2 different given problems in my programming assignment on Pandas Python library.

---

## Files
* 'MARSIGAN_2ECEA_PA3.ipynb': This Jupyter Notebook file contains the codes for each problem.
* 'README.md': This file contains the summary of the assignment.
* 'Marasigan_Pandas-P1.py': This Python file contains the codes for problem 1, formatted as a .py file.
* 'Marasigan_Pandas-P1.py': This Python file contains the codes for problem 2, formatted as a .py file.
* 'cars.csv': This csv (spreadsheet) file is to be imported and loaded into the Jupyter Notebook file.


---

## Solutions Overview
### Problem 1

**Problem:**
1. Load the csv (spreadsheet) file, cars.csv, into a data frame named cars using pandas.
2. Display the first five rows and last five rows of the resulting cars.

**Approach:**
Part 1
1. To initialize the program, we import the Pandas library to the program/file.
2. The csv (spreadsheet) file is imported through the read_csv command.
3. This file is loaded and stored into a data frame, named cars.
4. The table is then printed.

<pre>import pandas as pd #Gives the program/file access to the Pandas library
cars = pd.read_csv('cars.csv') #While the csv file being located at the same folder as the ipynb file, it reads 
cars = pd.DataFrame(cars)
cars</pre>

Part 2
1. In displaying the first five rows, we use the .head() syntax.
2. In displaying the last five rows, we use the .tail() syntax.

<pre>
  cars.head() #Displays the first five rows of the resulting cars.
</pre>
<pre>
  cars.tail() #Displays the last five rows of the resulting cars.
</pre>


---

### Problem 2
**Problem:**
Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.
1. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.
2. Display the row that contains the ‘Model’ of ‘Mazda RX4’.
3. Display how many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have
4. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

**Approach:**
Part 1
1. Slicing is used to get the asked portion.
2. In slicing, brackets are used to enclose (1) the starting index, (2) the terminal index, which is excluded, and (3) the increment.
3. In this problem, we start with index 1, end with index 10 (excluded), then have an increment of 2. This is to ensure that the first 5 indices (indices 1, 3, 5, 7, 9) are displayed.

<pre>cars[1:10:2]</pre>

Part 2
1. Subsetting is used to displaying and/or storing specified rows and columns from the program's data frame.
2. Given the car model, the .loc (locate) syntax is used to locate the column, "Model", then finds "Mazda RX4".

<pre>cars.loc[(cars['Model']=='Mazda RX4')]</pre>

Part 3
1. Similar to Part 2, subsetting is used to display data from specific rows and/or columns. Moreover, slicing is used to display particular portions (columns).
2. Given the car model, the .loc (locate) syntax is used to locate the column "Model", then finds "Camaro Z28". Then the columns to be displayed are enclosed in brackets.

<pre>cars.loc[(cars['Model']=='Camaro Z28'),['Model', 'cyl']]</pre>

Part 4
1. Similar to Part 2 and 3, subsetting is used to display data from specific rows and/or columns. Moreover, slicing is used to display particular portions (columns).
2. Given the car model, the .loc (locate) syntax is used to locate the column "Model", then finds "Camaro Z28". Then the columns to be displayed are enclosed in brackets.

<pre>cars.loc[(cars['Model']=='Mazda RX4 Wag'),['Model','cyl','gear']]</pre>
<pre>cars.loc[(cars['Model']=='Ford Pantera L'),['Model','cyl','gear']]</pre>
<pre>cars.loc[(cars['Model']=='Honda Civic'),['Model','cyl','gear']]</pre>
---
## How to View:

The Notebook file may be previewed via Github, or may be imported as an .ipynb file to Jupyter Notebook in order to see the full code with its input & output.
