# 20. Checking for a Win

There are 17 ship positions in total:

```
5 + 4 + 3 + 3 + 2 = 17
```

The player wins when all 17 have been hit.

We therefore need to count the number of `X` values in the battle grid.

## Counting

A counter can be used:

```python
count = 0
```

Each time the required item is found:

```python
count += 1
```

This means:

> Increase `count` by 1.

## Nested loops

Our board contains rows, and each row contains positions.

We can therefore use:

```python
for row in grid:
    for item in row:
        ...
```

The outer loop processes each row.

The inner loop processes each position within that row.

### Different example

Suppose a school has marks stored by class:

```
Class 1 → marks
Class 2 → marks
Class 3 → marks
```

Nested loops could be used to count how many students received a particular result.

### Practice

Create a 2D list containing several `X` values.

Use nested loops to count the number of `X` values.

### Battleship

Create `check_win()`.

It should:

1. Start a counter at zero.
2. Inspect every row.
3. Inspect every position in every row.
4. Count every `X`.
5. Determine whether the total is 17.
6. Return `True` or `False`.

***

[← Previous: Checking A Player S Attack](19-checking-a-player-s-attack.md) | [Contents](./) | [Next: Boolean Return Values →](21-boolean-return-values.md)
