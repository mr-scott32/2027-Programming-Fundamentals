---
icon: book-open
---

# Creating the Grid



First, we need to generate a 10x10 grid for Battleship. This will be created in something called a **Matrix or a 2D Array.** In Python, this is effectively a list of lists - rather than just a single rows of values, there are multiple rows and columns.

The following will create a 5x5 matrix:

{% code title="matrix.py" %}
```python
# Matrix Creation
matrix = []     # Create an empty list to store the rows
for i in range(5):  # Repeat 5 times to create 5 rows
    row = []        # Create an empty list for the current row
    for j in range(5):  # Repeat 5 times to create 5 columns
        row.append('-') # Add a '-' to the current row
    matrix.append(row)  # Add the completed row to the matrix


# Matrix Print
for i in range(5):                      # Repeat for each row
    for j in range(5):                  # Repeat for each column in the current row
        print(matrix[i][j], end=' ')    # Access and print the current matrix element
    print()                             # Move to the next line after each row
```
{% endcode %}

* **Outer loop** → controls the **rows**
* **Inner loop** → controls the **columns**
* `matrix[i][j]` → accesses the element at **row `i`, column `j`**
* `end=' '` → keeps elements on the **same line**
* `print()` → moves to the **next row**



## What to Do

Firstly, **DO NOT JUST COPY/PASTE, TYPE IT ALL OUT.** This is a **LEARNING PROCESS.**

* You need to create a function - call it something like `create_grid()`.
* You will need a 10x10 grid and include the dashes.
* You will need to **return** this grid at the end of the function so it is accessible to other functions.
* Test your function - you can print your matrix before you return the grid, but later will remove this.

