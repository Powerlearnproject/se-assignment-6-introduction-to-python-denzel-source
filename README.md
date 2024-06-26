
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

Python is a high-level, general-purpose programming language known for its:
Readability:  Its syntax is clear and concise, resembling natural language, making it easier to learn and write compared to more complex languages.
Versatility:  Python can be used for various tasks, including web development, data science, machine learning, scripting, and automation.
Large Standard Library:  Python comes with a rich collection of built-in modules and libraries that provide functionalities for common programming needs.
Strong Community:  Python boasts a vast and active community that contributes to its extensive libraries and resources.


Its popularity stems from its user-friendliness and wide range of applications. Examples include:
Web Development where frameworks like Django and Flask power many web applications.
Data Science and Machine Learning:Libraries like NumPy, Pandas and Scikit-learn are essential tools in these fields.
Scientific Computing,python's readability and powerful libraries make it ideal for scientific calculations and simulations.
Automation and Scripting:Python is often used to automate repetitive tasks and control workflows.

2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.

Download the installer:In windows,visit https://www.python.org/downloads/ and download the appropriate installer for windows 10 or  11.
Run the installer and follow the on-screen instructions.
Verify installation: Open a terminal/command prompt and type python --version  to check the installed version.

Virtual Environments:Virtual environments isolate project dependencies, preventing conflicts.
Use the command python -m pip install virtualenv to install the virtual environment and source projectname/scripts/activate to activate the virtual environment.

3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.

A simple Python program that prints "Hello, World!":
print("Hello, World!")

Basic Syntax Elements:
print(): A function used to display output on the console.
"Hello, World!": A string literal enclosed in double quotes.
Indentation (though not strictly required for this single line) is essential in Python for defining code blocks.

4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.

Basic Data Types:
int: Integers (whole numbers) - e.g., 10, -5
float: Floating-point numbers (decimals) - e.g., 3.14, -2.5
str: Strings (sequences of characters) - e.g., "Hello", 'World!' (single quotes also work)
bool: Boolean values (True or False)
list: Ordered collections of elements (can hold various data types) - e.g., [1, "apple", 3.5]
tuple: Immutable ordered collections (elements cannot be changed) - e.g., (1, "apple", 3.5)
dict: Unordered collections of key-value pairs (flexible data structure) - e.g., {"name": "Alice", "age": 30}

age = 25  # Integer variable
message = "I am " + str(age) + " years old."  # String variable with concatenation
is_adult = age >= 18  # Boolean variable

print(message)
print(f"Is adult: {is_adult}")
5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.

Conditional Statements (if-else):
x = 10
y = 5

if x > y:
    print(f"{x} is greater than {y}")
else:
    print(f"{x} is not greater than {y}")

    Loops (for loop):
fruits = ["apple", "banana", "orange"]

for fruit in fruits:
    print(fruit)


6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.

Functions: Reusable blocks of code that perform specific tasks. They promote modularity and code organization.

Why are functions Useful?
Code Reusability: Write code once and use it multiple times in your program or different projects.
Modularity: Break down complex programs into smaller, manageable functions.
Maintainability: Easier to understand, test and modify code when it's well-structured with functions.
Example Function:
def sum_numbers(num1, num2):
  """This function takes two numbers as arguments and returns their sum."""
  total = num1 + num2
  return total
# Call the function with arguments
result = sum_numbers(10, 20)
print(f"The sum is: {result}")

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.

Lists: Ordered, mutable collections of elements enclosed in square brackets []. Elements can be of different data types.

Dictionaries: Unordered collections of key-value pairs enclosed in curly braces {}. Keys are unique and must be immutable (strings, numbers, tuples). Values can be any data type.

Script Example:
# Create a list of numbers
numbers = [1, 5, 8, 3]

# Access elements by index (starts from 0)
first_number = numbers[0]
print(f"First number: {first_number}")

# Modify elements by index
numbers[2] = 12  # Change the third element

# Loop through elements
for number in numbers:
  print(number)

# Create a dictionary with key-value pairs
person = {"name": "Bob", "age": 35, "city": "New York"}

# Access values by key
name = person["name"]
print(f"Name: {name}")

# Add new key-value pair
person["occupation"] = "Software Engineer"

# Loop through key-value pairs
for key, value in person.items():
  print(f"{key}: {value}")

8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

Exception Handling:  A mechanism for dealing with errors (exceptions) that occur during program execution. It prevents unexpected program termination and allows for graceful error handling.

try-except-finally Blocks:
def divide(num1, num2):
  try:
    result = num1 / num2
    return result
  except ZeroDivisionError:
    print("Error: Cannot divide by zero")
  finally:
    print("This block always executes, regardless of exceptions")

# Call the function with valid and invalid arguments
result = divide(10, 2)
print(f"Result: {result}")

result = divide(10, 0)  # This will trigger the ZeroDivisionError exception. 

9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.

Modules:  Reusable Python files containing functions, classes, and variables. They extend Python's functionality.

Packages:  Collections of modules organized in a hierarchical structure. They provide a way to manage related functionalities.

Importing Modules:
import math  # Import the math module

# Use functions from the imported module
pi = math.pi
print(f"Pi value: {pi}")
10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.

Reading from Files:
# Open a file in read mode ("r")
with open("data.txt", "r") as file:
  # Read the entire file content as a string
  contents = file.read()
  print(contents)

Writing to Files:
# Open a file in write mode ("w") (existing file will be overwritten)
with open("output.txt", "w") as file:
  # Write a string to the file
  file.write("This is written to the file.")

# Open a file in append mode ("a") (adds content to the end of the file)
with open("output.txt", "a") as file:
  file.write("\nMore text appended.")

  # References
https://docs.python.org/ - Official Python Documentation
https://www.w3schools.com/python/ - Python Tutorial on W3Schools

# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


