# 4. Accessing Positions in a Grid

We need to be able to find individual positions on our board.

Python uses indexes to access list positions.

For example:

```python
items = ['A', 'B', 'C']
```

The positions are:

```text
Index:    0    1    2
          A    B    C
```

So:

```python
items[0]
```

gives:

```text
A
```

A 2D list uses two indexes:

```python
grid[row][column]
```

For example:

```python
grid[2][4]
```

means:

> Row 2, column 4.

Remember that Python starts counting at **0**.

---

## Different example

Imagine a cinema seating plan:

```text
A B C
D E F
G H I
```

The value in row 1, column 2 is:

```python
seats[1][2]
```

### Practice

Create a 3 × 3 grid containing letters.

Print one specific position using two indexes.

Then change that position to `X`.

### Battleship

Use your board and access individual positions.

For example, experiment with:

```python
grid[2][5]
```

Change a position to `S`.

Print the board and confirm that the correct position changed.

---

[← Previous: Creating A 2D List](03-creating-a-2d-list.md) | [Contents](00-start-here.md) | [Next: Displaying A Grid →](05-displaying-a-grid.md)
