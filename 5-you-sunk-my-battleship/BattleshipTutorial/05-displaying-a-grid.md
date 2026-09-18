# 5. Displaying a Grid

Our board is stored correctly, but printing the entire list is not very easy to read.

We can use nested loops to display every position.

For example:

```python
for i in range(3):
    for j in range(3):
        print(grid[i][j], end=' ')
    print()
```

The inner loop prints each position in the row.

The outer loop moves to the next row.

The `end=' '` means that the next value is printed on the same line.

The `print()` after the inner loop moves to the next line.

### Practice

Create a 5 × 5 grid and display it as a square.

### Battleship

Add code to display your Battleship board.

You should now be able to:

1. Create a board.
2. Store it in a variable.
3. Change an individual position.
4. Display the entire board.

---

[← Previous: Accessing Positions In A Grid](04-accessing-positions-in-a-grid.md) | [Contents](00-start-here.md) | [Next: Getting Coordinates From The Player →](06-getting-coordinates-from-the-player.md)
