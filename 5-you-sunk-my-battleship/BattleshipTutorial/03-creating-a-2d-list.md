# 3. Creating a 2D List

One row is not enough for Battleship.

A Battleship board has:

```text
10 rows
10 columns
```

This means we need a **list containing lists**.

This is called a **two-dimensional list**, or **2D list**.

For example:

```python
grid = []

row = ['-', '-', '-']
grid.append(row)
```

Now `grid` contains one row.

We can create many rows using a loop:

```python
grid = []

for i in range(3):
    row = []
    
    for j in range(3):
        row.append('-')
    
    grid.append(row)
```

This produces a 3 × 3 grid.

## Why are there two loops?

The outer loop creates the rows.

The inner loop creates the positions inside each row.

Think about it as:

```text
Create row
    Create position
    Create position
    Create position

Create row
    Create position
    Create position
    Create position

Create row
    Create position
    Create position
    Create position
```

### Practice

Create a 4 × 4 grid containing `-` symbols.

Print the resulting list.

### Battleship

Now create your `create_board()` function.

It should:

* create an empty list for the board
* create 10 rows
* put 10 `-` symbols into each row
* add each row to the board
* return the completed board

You should now have your first completed Battleship function.

---

[← Previous: Creating A List](02-creating-a-list.md) | [Contents](00-start-here.md) | [Next: Accessing Positions In A Grid →](04-accessing-positions-in-a-grid.md)
