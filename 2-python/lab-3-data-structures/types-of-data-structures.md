---
icon: book-open
---

# Types of Data Structures

Read through the following to get a sense of the different kinds of data structures you can use in Python. Lists and dictionaries are the most common you would use in Python. A key difference to note, however, is that **arrays are slightly more efficient than lists in terms of file size, but can only store one data type - lists can store multiple data types.**

## **Single-dimensional array**

To create a single-dimensional array using NumPy:

```python
import numpy as np

# Create a 1D array
single_dimensional = np.array([1, 2, 3, 4, 5])

# Print the entire array
print("Array:", single_dimensional)

# Access elements by index
print("First element:", single_dimensional[0])
print("Last element:", single_dimensional[-1])

# Basic operations
sum_of_elements = np.sum(single_dimensional)
mean_of_elements = np.mean(single_dimensional)

print("Sum of elements:", sum_of_elements)
print("Mean of elements:", mean_of_elements)
```

These are basic arrays that store a sequence of values of the same type. They are efficient for storing and manipulating numerical data due to their compact memory layout. In Python, the `array` module allows for the creation of single-dimensional arrays, providing operations for adding, removing, and modifying elements while ensuring all items are of the same data type, like integers ('i' type code). This efficiency makes them suitable for tasks where memory usage is a concern and operations on large datasets are needed.

**Usage**: Used when memory efficiency is crucial, often in numerical operations.

***

## **Multi-dimensional array**

```python
import numpy as np

# Creating a 2D array (matrix) using NumPy
numpy_matrix = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])

# Accessing elements
print(numpy_matrix[0, 1])  # Output: 2 (row 0, column 1)
print(numpy_matrix[2, 0])  # Output: 7 (row 2, column 0)

# Performing operations (example: element-wise addition)
another_matrix = np.array([[10, 11, 12], [13, 14, 15], [16, 17, 18]])
result_matrix = numpy_matrix + another_matrix
print(result_matrix)
```

Multi-dimensional arrays are arrays with more than one dimension, such as 2D, 3D, and beyond. They are used to represent matrices or tensors, making them essential in fields like machine learning, image processing, and any application dealing with complex data sets. In Python, NumPy is the most popular library for handling multi-dimensional arrays. It offers powerful capabilities for matrix operations, data manipulation, and numerical computations efficiently. Using multi-dimensional arrays, you can perform operations such as addition, multiplication, and transposition across dimensions, facilitating sophisticated data analysis and scientific computation tasks.

**Usage**: Used in scientific computing and data analysis for matrix operations.

***

## **Lists**

```python
# Create a list
my_list = [1, 2, 3, 4, 5]
```

Lists are a fundamental data structure in Python, used for storing collections of items. They are versatile and dynamic, allowing you to store elements of varying data types in a single list. Lists are mutable, meaning their content can be changed, including adding, removing, or modifying elements. They maintain the order of items as inserted and support a variety of operations, such as slicing, iteration, and membership testing. Lists are particularly useful for representing sequences of data and for iterating over elements in a structured way.

#### Modifying Lists

To effectively manage lists in Python, you can remove elements, pop elements, and iterate through lists to search for specific values.

* **Remove**: Use `remove(value)` to delete the first occurrence of a value.
* **Pop**: Use `pop(index)` to remove and return an item by its index.
* **For Loop**: Iterate over the list with a `for` loop to find or process specific items.

```python
# Example of creating and using a list
fruits = ['apple', 'banana', 'cherry']
fruits.append('orange')  # Adding an item
print(fruits[1])  # Accessing an item by index

# Remove an item by value
fruits.remove('banana')  # Removes the first occurrence of 'banana'

# Pop an item by index
popped_fruit = fruits.pop(2)  # Removes and returns the item at index 2

# Use a for loop to find a value
for fruit in fruits:
    if fruit == 'cherry':
        print("Cherry found!")
```

**Usage**: Versatile dynamic arrays used for storing an ordered collection of items.

***

## **Trees**

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

# Example usage:
# Create the root node
root = Node(10)

# Add child nodes
root.left = Node(5)
root.right = Node(15)

# Add more children
root.left.left = Node(2)
root.left.right = Node(7)
root.right.right = Node(20)

# This creates a simple binary tree structure:
#        10
#       /  \
#      5    15
#     / \    \
#    2   7    20

print(root.right.right data) # Would print node 20
```

Trees are hierarchical data structures consisting of nodes connected by edges. Each tree starts with a root node and can have any number of child nodes. Trees are particularly useful for representing hierarchical data such as file systems, organisational structures, and syntax trees.

The basic component of a tree in Python is typically represented by a `Node` class. Each node contains data and pointers to its left and right children if it's a binary tree (a tree where each node has at most two children).

Here's a simple implementation of a binary tree in Python:

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

# Create root node
root = Node(10)

# Add child nodes
root.left = Node(5)
root.right = Node(15)
```

In this example, we create a binary tree with a root node of value `10` and child nodes `5` and `15`. Trees can be traversed in various ways, such as in-order, pre-order, and post-order, which are essential for many algorithms and applications in computer science.

**Usage**: Used in hierarchical data structures and databases (like representing syntax trees).

***

## **Stacks**

```python
# Create a stack
stack = []

# Push elements
stack.append('a')
stack.append('b')

# Pop elements
stack.pop()
```

A stack is a linear data structure that follows a Last In, First Out (LIFO) principle, where the last element added to the stack is the first one to be removed. In Python, stacks can be implemented using lists, where the `append()` method is used to add an element to the top of the stack and the `pop()` method is used to remove the last element added. Stacks are useful in various applications, such as navigating backward in web browsers, parsing expressions, and in recursive algorithms.

Consider a simple scenario in a text editor where you want to implement an undo mechanism. Each change made by the user can be pushed onto a stack. When the user wants to undo an action, the last change can be popped from the stack and reversed:

```python
# Create a stack for undo operations
undo_stack = []

# Record an action
undo_stack.append("type 'hello'")

# Undo the last action
last_action = undo_stack.pop()
print(f"Undoing action: {last_action}")
```

**Usage**: Used in scenarios like the undo mechanism in text editors.

***

## Dictionaries

Dictionaries in Python are collections of key-value pairs, where each key is unique. They offer a way to store data that can be easily searched by key, providing an efficient method for organising and accessing data. For example:

```python
# Create a dictionary
person = {
    'name': 'Alice',
    'age': 30,
    'occupation': 'Engineer'
}

# Access a value by key
print(person['name'])  # Output: Alice

# Add a new key-value pair
person['city'] = 'New York'

# Remove a key-value pair
del person['age']

# Iterate through key-value pairs in the dictionary
for key, value in person.items():
    print(f"{key}: {value}")
```

**Usage**: Dictionaries are powerful for managing structured data and are extensively used in scenarios that require quick data retrieval by key, such as databases and configuration settings.

## **Hash Tables**&#x20;

**Not used in Python really - more common in C languages.**&#x20;

Hash tables are data structures that provide an efficient way to store and retrieve data through key-value pairs. They operate by taking a key, computing its hash code, and using the hash to determine the key's index in an array, allowing for fast data access. In many programming languages, dictionaries are implemented using hash tables, providing the same efficiency in lookups and insertions.

#### Differences between Hash Tables and Dictionaries

* **Implementation**: While hash tables are a lower-level concept involving hash functions and handling collisions, dictionaries are abstract data types that often use hash tables internally.
* **Language Specific**: Dictionaries as implemented in Python are high-level interfaces built upon hash tables, offering built-in functionality and flexible syntax. Not all languages implement dictionaries in the same way or provide them as built-in types.
* **Features**: Dictionaries often come with additional features like dynamic resizing, ordering (from Python 3.7+ dictionaries maintain insertion order), and automatic handling of collisions, which are not intrinsic to basic hash table implementations.

## Records

Records are a composite data structure that groups together related fields, typically representing an entity or item with multiple attributes. Each field in a record can be of a different data type, allowing for complex data representations under a single structure.

**Usage:** Records are used to group together related fields of data for an entity, allowing for structured and complex data representations.

#### Python Example

In Python, a common way to represent records is by using classes or named tuples. Below is an example using a class to define a record for a `Book`:

```python
class Book:
    def __init__(self, title, author, year, isbn):
        self.title = title
        self.author = author
        self.year = year
        self.isbn = isbn

# Example usage
my_book = Book("1984", "George Orwell", 1949, "0451524934")
print(my_book.title)  # Output: 1984
```

Named tuples provide an efficient way to create simple records in Python. They are similar to regular tuples but allow for field access by name for improved readability.

```python
from collections import namedtuple

# Define a Book named tuple with fields: title, author, year, and isbn
Book = namedtuple('Book', ['title', 'author', 'year', 'isbn'])

# Example usage
my_book = Book(title="1984", author="George Orwell", year=1949, isbn="0451524934")
print(my_book.title)  # Output: 1984
```

This approach maintains simplicity while providing clear access to the attributes of the record.

For more information on tuples, see the following link:

{% embed url="https://www.w3schools.com/python/python_tuples.asp" %}

## Sequential Files

Sequential files are a type of file storage that organizes data in a sequence, much like a list. This structure is optimized for reading and writing data in a linear order. When accessing data in sequential files, the system typically starts at the beginning and processes each record one by one. This method is efficient for processes that need to read all records, but less so for random access. Sequential files are often used for tasks such as logging, where data is appended in the order it is generated.

```python
# Open a file in write mode
with open("logfile.txt", "w") as file:
    # Writing data sequentially
    file.write("Log entry 1: Starting the application.\n")
    file.write("Log entry 2: Application is running.\n")
    file.write("Log entry 3: Application is exiting.\n")

# Open the file in read mode to display contents
with open("logfile.txt", "r") as file:
    for line in file:
        print(line.strip())
```

