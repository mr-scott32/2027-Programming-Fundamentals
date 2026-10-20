# 07. Repeating Across Multiple Positions

A ship is not stored in one position.

A ship with a length of 5 occupies five positions.

A `for` loop can process those positions.

For example:

```python
for i in range(5):
    print(i)
```

produces:

```
0
1
2
3
4
```

If our starting column is `3`, we could use:

```python
y_pos + i
```

to represent:

```
3
4
5
6
7
```

This allows a ship to extend across the board.

## Different example

Imagine a character moving five spaces to the right.

If the starting position is 2:

```python
for i in range(5):
    position = 2 + i
    print(position)
```

The positions are:

```
2
3
4
5
6
```

### Practice

Ask the user for a starting position and a length.

Use a loop to print every position occupied by the object.

### Battleship

Use a loop to inspect the positions a ship would occupy.

For a horizontal ship, think carefully about which coordinate needs to change.

For a vertical ship, think carefully about which coordinate needs to change.

***

[← Previous: Getting Coordinates From The Player](06-getting-coordinates-from-the-player.md) | [Contents](./) | [Next: Making Decisions →](08-making-decisions.md)
