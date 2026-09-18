---
icon: book-open
---

# Creating a Player Grid

This is possibly the hardest part. This is because we need to:

* Create the grid
* Place each ship&#x20;
  * Horizontal or vertical?
  * Do we provide starting or end space? Or both?
  * How do we represent ships in the grid?
  * How do we make sure all get placed?
  * How do we handle errors?
* Print grid
* Return the grid so other modules can access it when needed

Before we start though, you will need to consider how to access and change values in a matrix. The following code will show you how to add to your matrix program to change a value at a specific position entered by the user.

{% code title="matrix_change.py" %}
```py
# Matrix Creation
matrix = []                         # Create an empty list to store the rows
for i in range(5):                  # Repeat 5 times to create 5 rows
    row = []                        # Create an empty list for the current row
    for j in range(5):              # Repeat 5 times to create 5 columns
        row.append('-')             # Add a '-' to the current row
    matrix.append(row)              # Add the completed row to the matrix


# Get Coordinates
x_pos = int(input('Enter x coordinate from 0 to 4: '))  # Get the row position from the user
y_pos = int(input('Enter y coordinate from 0 to 4: '))  # Get the column position from the user

matrix[x_pos][y_pos] = 'X'          # Access the chosen row and column and change it to 'X'


# Matrix Print
for i in range(5):                  # Repeat for each row
    for j in range(5):              # Repeat for each column in the current row
        print(matrix[i][j], end=' ') # Access and print the current matrix element
    print()                         # Move to the next line after each row
```
{% endcode %}

**But what if we wanted to change more than one at a time?**

**We can use a 'for' loop.**

{% code title="matrix.py" %}
```python
# Matrix Creation
matrix = []                         # Create an empty list to store the rows

for i in range(5):                  # Repeat 5 times to create 5 rows
    row = []                        # Create an empty list for the current row

    for j in range(5):              # Repeat 5 times to create 5 columns
        row.append('-')             # Add a '-' to the current row

    matrix.append(row)              # Add the completed row to the matrix


# Get Coordinates
x_pos = int(input('Enter x coordinate from 0 to 4: ')) # Get the row position from the user
y_pos = int(input('Enter y coordinate from 0 to 4: ')) # Get the column position from the user

for i in range(5):                  # Check each position needed for the placement
    if matrix[x_pos][y_pos+i] == 'X' or y_pos > 9: # Check if the position is already occupied 
                                                    # or outside the board
        print('Invalid placement!') # Tell the user that the placement is invalid
        break                       # Stop checking the placement
    else:
        for i in range(v):      # Repeat for the length of the ship
            matrix[x_pos][y_pos+i] = 'X'   # Place an 'X' at each position occupied by the ship
            placement = True    # Record that the ship has been placed successfully


# Matrix Print
for i in range(5):          # Repeat for each row
    for j in range(5):              # Repeat for each column in the current row
        print(matrix[i][j], end=' ') # Access and print the current matrix element
    print()                         # Move to the next line after each row
```
{% endcode %}

## What to do

* You need to create a function - call it something like `setup_player()`.
* You will need to set a variable to store the return value of `create_grid()`
* You will need to ask the user the following for each ship and add each ship to the grid. You can choose the character, but I used 'S' for ship.
  * Vertical / horizontal placement
  * Starting x and y position for each ship placement
  * Place the ship downwards / rightwards (depending on vertical / horizontal) for as many spaces as the ship is long:
    * Carrier: 5 spaces
    * Battleship: 4 spaces
    * Cruiser: 3 spaces
    * Submarine: 3 spaces
    * Destroyer: 2 spaces
* You will need to **return** this grid at the end of the function so it is accessible to other functions.
* Test your function - you can print your matrix before you return the grid, but later will remove this.

**Try your best at the above and test the function.**

At this stage your instinct is probably to use ongoing IF / ELIF / ELSE statements to place each ship, and this is fine - we'll look at optimisation in the next section. Just have a go.
