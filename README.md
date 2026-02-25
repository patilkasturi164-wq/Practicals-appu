# Practicals-appu
App practicals
practical 1
a. Write a python code to demonstrate concatenating tuples to nested tuples.
Code:
# Define two simple tuples
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
# Concatenate them into a nested tuple
nested_tuple = (tuple1, tuple2)
# Print the result
print("First Tuple:", tuple1)
print("Second Tuple:", tuple2)
print("Nested Tuple after Concatenation:", nested_tuple)
Output:
First Tuple: (1, 2, 3)
Second Tuple: (4, 5, 6)
Nested Tuple after Concatenation: ((1, 2, 3), (4, 5, 6))
b. Write a python code to sort the nested tuple using sorted() function.
# Define a nested tuple
nested_tuple = ((3, 4), (1, 2), (5, 0), (2, 3))
# Use sorted() to sort based on the first element of each inner tuple
sorted_nested = sorted(nested_tuple)
# Print results
print("Original Nested Tuple:", nested_tuple)
print("Sorted Nested Tuple:", sorted_nested)
Output:
Original Nested Tuple: ((3, 4), (1, 2), (5, 0), (2, 3))
Sorted Nested Tuple: [(1, 2), (2, 3), (3, 4), (5, 0)]
c. Write a python code to demonstrate unpacking of nested tuples.
# Define a nested tuple
nested_tuple = ((1, 2), (3, 4), (5, 6))
# Unpack the nested tuple
(a1, a2), (b1, b2), (c1, c2) = nested_tuple
# Print unpacked values
print("First inner tuple elements:", a1, a2)
print("Second inner tuple elements:", b1, b2)
print("Third inner tuple elements:", c1, c2)
Output:
First inner tuple elements: 1 2
Second inner tuple elements: 3 4
Third inner tuple elements: 5 6


practical 2
Write a Python code to Find the size of Tuples.
Code:
# Define a tuple
my_tuple = (10, 20, 30, 40, 50)
# Find the size (number of elements) in the tuple
size = len(my_tuple)
# Print the result
print("The tuple is:", my_tuple)
print("Size of the tuple:", size)
Output:
The tuple is: (10, 20, 30, 40, 50)
Size of the tuple: 5
b. Write a Python code Find sum of tuple elements.
Code:
# Define a nested tuple
nested_tuple = ((1, 2), (3, 4))
# Flatten and sum
total = sum(sum(inner) for inner in nested_tuple)
print("Sum of all nested tuple elements:", total)
Output:
Sum of all nested tuple elements: 10
c. Write a Python code to remove duplicate element from tuple.
Code:
# Define a tuple with duplicate elements
my_tuple = (1, 2, 3, 2, 4, 1, 5, 3)
# Remove duplicates by converting to a set, then back to a tuple
unique_tuple = tuple(se
t(my_tuple))
# Print results
print("Original Tuple:", my_tuple)
print("Tuple after removing duplicates:", unique_tuple)


practical 3
a. Write a python code to retrieve data from HTML file.
Code:
HTML Code:
<!DOCTYPE html>
<html>
<head>
 <title>Sample HTML Page</title>
</head>
<body>
 <h1>Welcome to My Website</h1>
 <p>This is a paragraph.</p>
 <p>This is another paragraph.</p>
 <a href="https://example.com">Example Link</a>
 <a href="https://openai.com">OpenAI Link</a>
</body>
</html>
Library install : pip install beautifulsoup4
from bs4 import BeautifulSoup
# Read the HTML file
with open('sample.html', 'r', encoding='utf-8') as file:
 html_content = file.read()
# Parse the HTML
soup = BeautifulSoup(html_content, 'html.parser')
# Retrieve the title
title = soup.title.text
print("Title of the page:", title)
# Retrieve all paragraphs
paragraphs = soup.find_all('p')
print("\nParagraphs:")
for p in paragraphs:
 print(p.text)
# Retrieve all links (anchor tags)
links = soup.find_all('a')
print("\nLinks:")
for link in links:
 print(link.get('href'))
 ://openai.com
b. Write a python code to reading and writing text, CSV files
Code:
# Writing to a text file
with open('example.txt', 'w') as file:
 file.write("Hello, this is a text file.\n")
 file.write("Welcome to Python file handling.\n")
# Reading from a text file
with open('example.txt', 'r') as file:
 content = file.read()
 print("Contents of the text file:")
 print(content)
CSV file:
import csv
# Writing to a CSV file
data = [
 ["Name", "Age", "City"],
 ["Alice", 25, "New York"],
 ["Bob", 30, "Los Angeles"],
 ["Charlie", 22, "Chicago"]
 ]
 # Write CSV
with open('example.csv', 'w', newline='') as file:
 writer = csv.writer(file)
 writer.writerows(data)
# Reading from a CSV file
with open('example.csv', 'r') as file:
 reader = csv.reader(file)
 print("Contents of the CSV file:")
 for row in reader:
 print(row)
Output:
For Text File:
Contents of the text file:
Hello, this is a text file.
Welcome to Python file handling.
For CSV File:
Contents of the CSV file:
['Name', 'Age', 'City']
['Alice', '25', 'New York']
['Bob', '30', 'Los Angeles']
['Charlie', '22', 'Chicago']


practical 4
a. Write a python code on a simple GUI application using
buttons,textbox etc.
Code:
import tkinter as tk
def show_message():
name = entry.get()
label_result.config(text="Hello , Anita!!" + name)
# Create main window
window = tk.Tk()
window.title("Simple GUI")
# Label
label = tk.Label(window, text="Enter your name:")
label.pack()
# Textbox
entry = tk.Entry(window)
entry.pack()
# Button
button = tk.Button(window, text="Click Me", command=show_message)
button.pack()
# Result Label
label_result = tk.Label(window, text="")
label_result.pack()
# Run the application
window.mainloop()
b. Create a simple Flask app that displays "Hello, Flask!" on the
Homepage.
Code:
from flask import Flask
app = Flask(__name__)
@app.route('/')
def home():
 return "Hello, Flask!"
if __name__ == "__main__":
 app.run(debug=True)
 c. Create a webpage where a user enters their name, and the app
displays a personalized greeting.
from flask import Flask, request
app = Flask(__name__)
@app.route('/', methods=['GET', 'POST'])
def greet():
 if request.method == 'POST':
 name = request.form['name']
 return "Hello, " + name
 return '''
 <form method="post">
 Enter your name: <input type="text" name="name">
 <input type="submit">
 </form>
 '''
if __name__ == "__main__":
 app.run(debug=True)

 
 practical 5
 a. Python code to create NumPy basics
Code:
import numpy as np
# Basic NumPy array
arr = np.array([1, 2, 3, 4, 5])
print("Array:", arr)
print("Type:", type(arr))
print("Shape:", arr.shape)
print("Dimension:", arr.ndim)
print("Data Type:", arr.dtype)
Output:
Array: [1 2 3 4 5]
Type: <class 'numpy.ndarray'>
Shape: (5,)
Dimension: 1
Data Type: int64
b. Write a python code to create Numpy.
import numpy as np
# Array from list
a = np.array([10, 20, 30])
# Array of zeros
b = np.zeros((2, 2))
# Array of ones
c = np.ones((2, 3))
# Array with random values
d = np.random.rand(3, 3)
print("Array a:", a)
print("Zeros array:\n", b)
print("Ones array:\n", c)
print("Random array:\n", d)

 
practical 6
a. Find Minimum Element in Array using Numpy
import numpy as np
Create a numpy array
arr = np.array([12, 5, 7, 9, 1, 4])
#Find the minimum element
min_element = np.min(arr)
print("Minimum Element:", min_element)
b. Find Mean of Every Numpy Array in the Given List
import numpy as np
#List of numpy arrays
array_list = [np.array([1, 2, 3]), np.array([4, 5, 6]), np.array([7, 8, 9])]
#Calculate mean of each array
means = [np.mean(arr) for arr in array_list]
print("Means:", means)
c. Reverse Numpy Array
import numpy as np
#Create a numpy array
arr = np.array([1, 2, 3, 4, 5])
#Reverse the array
reversed_arr = np.flip(arr)
print("Reversed Array:", reversed_arr)
d. Add Rows and Columns in Numpy Array
import numpy as np
#Create a numpy array
arr = np.array([[1, 2], [3, 4]])
#Add a row
arr_with_row = np.vstack((arr, [5, 6]))
$Add a column
arr_with_col = np.hstack((arr, [[5], [6]]))
print("Array with added row:\n", arr_with_row)
print("Array with added column:\n", arr_with_c


practical 7
1. Python code to demonstrate basic operations on a single array
import numpy as np
# Create an array
arr = np.array([10, 20, 30, 40, 50])
# Basic operations
print("Original Array:", arr)
print("Array Length:", len(arr))
print("Max Value:", arr.max())
print("Min Value:", arr.min())
print("Sum of Elements:", arr.sum())
print("Mean (Average):", arr.mean())
2. Python code to create an array with 10 elements and slice 1st to 5th elements
import numpy as np
# Create array with 10 elements
arr = np.array([5, 12, 18, 25, 30, 35, 40, 45, 50, 55])
# Slice 1st to 5th element (index 0 to 4)
sliced_arr = arr[0:5]
print("Original Array:", arr)
print("Sliced Array (1st to 5th):", sliced_arr)
O/P:
Original Array: [ 5 12 18 25 30 35 40 45 50 55]
Sliced Array (1st to 5th): [ 5 12 18 25 30]
3. Python code to sort an array alphabetically
import numpy as np
# Create an array of strings
arr = np.array(["banana", "apple", "grapes", "mango", "cherry"])
# Sorting array alphabetically
sorted_arr = np.sort(arr)
print("Original Array:", arr)
print("Sorted Array:", sorted_arr)
O/P:
Original Array: ['banana' 'apple' 'grapes' 'mango' 'cherry']
Sorted Array: ['apple' 'banana' 'cherry' 'grapes' 'mango'] 


  Practical no.9
1. Select rows from DataFrame using relational and logical operators
Example: Select rows where Age > 25 AND Salary < 50000
import pandas as pd
# Create a sample DataFrame
data = {
 'Name': ['Amit', 'Riya', 'John', 'Sara', 'Rahul'],
 'Age': [22, 28, 35, 19, 42],
 'Salary': [30000, 45000, 60000, 25000, 48000]
}
df = pd.DataFrame(data)
# Relational + logical operators
selected_rows = df[(df['Age'] > 25) & (df['Salary'] < 50000)]
print("Original DataFrame:\n", df)
print("\nSelected Rows (Age>25 AND Salary<50000):\n", selected_rows)
2. Python code to filter duplicate rows in a DataFrame
Example: Remove duplicate rows
import pandas as pd
# Sample DataFrame with duplicates
data = {
 'Name': ['Amit', 'Riya', 'John', 'Amit', 'Riya'],
 'Marks': [85, 92, 78, 85, 92]
}
df = pd.DataFrame(data)
# Remove duplicate rows
df_no_duplicates = df.drop_duplicates()
print("Original DataFrame:\n", df)
print("\nDataFrame After Removing Duplicates:\n", df_no_duplicates)


practical 8
a. Write a python code to demonstrate importing pandas libraries
and create data frame object.
Code:
import pandas as pd
# Creating a simple DataFrame
data = {
 "Name": ["Amit", "Neha", "Rahul"],
 "Age": [21, 22, 20],
 "Marks": [85, 90, 78]
}
df = pd.DataFrame(data)
print("DataFrame:")
print(df)
b. Write a Python code to create pandas series from a dictionary of
values and ndarray.
Code:
import pandas as pd
import numpy as np
# Series from Dictionary
dict_data = {"A": 10, "B": 20, "C": 30}
series_dict = pd.Series(dict_data)
print("Series from Dictionary:")
print(series_dict)
# Series from ndarray
array_data = np.array([100, 200, 300])
series_array = pd.Series(array_data)
print("\nSeries from ndarray:")
print(series_array)
c. Write a Python code to perform arithmetic operations on two
pandas series.
Code:
import pandas as pd
s1 = pd.Series([10, 20, 30, 40])
s2 = pd.Series([5, 10, 15, 20])
print("Addition:")
print(s1 + s2)
print("\nSubtraction:")
print(s1 - s2)
print("\nMultiplication:")
print(s1 * s2)
print("\nDivision:")
print(s1 / s2)
d. Write a Python code to add some data in existing series.
Code:
import pandas as pd
# Create initial Series
s = pd.Series([10, 20, 30], index=["A", "B", "C"])
print("Original Series:")
print(s)
# Adding new data
s["D"] = 40
print("\nUpdated Series:")
print(s)


practical 10
a. Write a code to import and export data between pandas and csv files.
Step 1:
Create .CSV file eg. Hi ,How are you?
Step 2:
Import the file or Save in your drive.
Step 3:
Code:
import pandas as pd
# ----- Import data from a CSV file -----
# Reading data from a CSV file
data = pd.read_csv("input_data.csv")
print("Data imported from CSV file:")
print(data)
# ----- Export data to a new CSV file -----
# Writing data to another CSV file
data.to_csv("output_data.csv", index=False)
print("\nData successfully exported to output_data.csv")
b. Read employee.csv file to create dataframe and perform following
operations:
i) Display Name, Gender and department of employee.
ii) Display first 5 and last 5 records from employee.csv
import pandas as pd
# Read employee.csv file
df = pd.read_csv("employee.csv")
print("Employee Data:")
print(df)
# i) Display Name, Gender and Department columns
print("\nName, Gender and Department of employees:")
print(df[["Name", "Gender", "Department"]])
# ii) Display first 5 records
print("\nFirst 5 records:")
print(df.head())
# Display last 5 records
print("\nLast 5 records:")
print(df.tail())
