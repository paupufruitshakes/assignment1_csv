Assignment 1 Documentation
==========================


Assignment 1 Overview: 
----------------------

1. Print assignment_1 data using command prompt as:
	1. Default
	2. CSV
	3. HTML Tables
	4. JSON files

2. Print assignment1 data line by line using command prompt as:
	1. Default
	2. CSV
	3. HTML Tables
	4. JSON files

3. Creating new list from assignment1 data using functions: 
	1. Create functions, which return all data from each column
	2. Create a list of all returned values from functions
	3. Duplicate list and change the headings from Rank, State, BTUs to (a, b, c)
	4. Return (print) the list.



Part 1.3 CSV file: Populated a new list using function data:  
------------------------------------------------------------

1. Assignment purpose: 
	Import functions and create a new list, populate with the data from each function.
	Import functions which will create a list with newly labeled headers.

2. Design section:
	Write a script that imports functions to populate a new list. Duplicate the list and change the 
	headings "a, b, c" rather than "Rank, State, BTUs". 

3. Pseudo code: 
	1. Create function parameters to iterate one csv column.
	2. Import csv file.
	3. Create a new list.
	4. Iterate a csv column into list.
	5. Repeat, create a function for each column. 
	6. Import functions and create a loop that iterates data into a list of dictionaries. 
	Dictionaries have keys "Rank, State, BTUs per capita". 
	7. Change dictionary keys from "Rank, State, BTUs per capita" to "a, b, c"

4. Pseudo code lines 1-5:
	1. Wrote a script for three functions.
	2. For each function, created a list and appended a column to list. Had three functions in total "a, b, c" representing column
	headings "Rank, State, BTUs per capita"
	3. The script without the function syntax prints a list with targeted column data. When I write the same script as a function,
	output is:
		Traceback (most recent call last):
		File "<stdin>", line 1, in <module>
		ModuleNotFoundError: No module named 'a'

	Results:

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
			
Attempt 2: Removed annotations, able to call functions in IDLE


		def a():
   		 	import csv
	
   			energy_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				energy_list.append(line[0])

   			print(energy_list) 

   		def b():
   		 	import csv

   			state_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				state_list.append(line[0])

   			print(energy_list) 

   		def c():
   		 	import csv

   			BTU_list = []

   			with open('Assignment1_data.csv', 'r') as f:
   			reader = csv.reader(f, delimiter = ',', quoting = csv.QUOTE_ALL)
   			for line in reader:
   				BTU_list.append(line[0])

   			print(energy_list) 

Pseudo Code line 6-7 steps:
	1. Create a new function with parameters rank, state, BTUs.
	2. Import energy data functions.
	3. Create an empty list.
	4. Create a for loop that iterates function data into the list. Use the same index for each function to create multiple
	dictionaries within the empty list. 
	

	Result:
	
		def energy_consumption(state, rank, BTUs):
		
			from a import function
			from b import function
			from c import function
			
			energy_data = []
			
			for x in range[0, len(a)]:
				{
					state: b(x),
					rank: a(x),
					BTUs: c(x),
				}
		
		
	
