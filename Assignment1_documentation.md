Assignment 1 Documentation
==========================


Assignment 1 Overview: 
----------------------

1. Print assignment_1 data using command prompt as:
	-Default
	-CSV
	-HTML Tables
	-JSON files

2. Print assignment1 data line by line using command prompt as:
	-Default
	-CSV
	-HTML Tables
	-JSON files

3. Creating new list from assignment1 data using functions: 
	-Create functions, which return all data from each column
	-Create a list of all returned values from functions
	-Duplicate list and change the headings from Rank, State, BTUs to (a, b, c)
	-Return (print) the list.



Part 1.3 CSV file: Populated a new list using function data:  
------------------------------------------------------------

1. Assignment purpose: 
	Import functions and create a new list, populate with the data from each function.
	Import functions which will create a list with newly labeled headers.

2. Design section:
Write a script that imports functions to populate a new list. Duplicate the list and change the headings "a, b, c" rather than "Rank, State, BTUs". 

3. Pseudo code: 
	1. Create function parameters to iterate one csv column.
	2. Import csv file.
	3. Create a new list.
	4. Iterate one csv column into list.
	5. Repeat, create a function for each column. 
	6. Use loop and append to iterate data into new list.
	8. Iterate each function into a new list. 
	9. Make a dictionary from new list.
	10. Use dictinary keys to change column headings to "a, b, c" from "Rank, State, BTUs per capita"

4. Steps of what happend:
	1. Wrote a script for three functions.
	2. For each function, created a list and appended a column to list. Had three functions in total "a, b, c" representing column
	headings "Rank, State, BTUs per capita"
	3. The script without the function syntax prints a list with targeted column data. When I write the same script as a function,
	output is:
	
	Traceback (most recent call last):
  	File "<stdin>", line 1, in <module>
	ModuleNotFoundError: No module named


5. Results

Attempt 1:
		def a():
			"""Assignment1_data.csv column 1 Energy Rank"""
   		 	import csv

   			energy_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				energy_list.append(line[0])

   			print(energy_list) 

   		def b():
   		"""Assignment1_data.csv column 2 State Rank"""
   		 	import csv

   			state_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				state_list.append(line[0])

   			print(energy_list) 

   		def c():
   		"""Assignment1_data.csv column 3 BTU per capita"""
   		 	import csv

   			BTU_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				BTU_list.append(line[0])

   			print(energy_list) 
