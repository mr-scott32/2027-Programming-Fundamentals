# 16. Checking Every Position

When the CPU chooses a position, we need to check **every position occupied by the ship**.

We already know how to use:

```python
for i in range(v):
```

But there is a useful Python feature for this particular problem.

## `for...else`

Consider:

```python
for number in numbers:
    if number < 0:
        break
else:
    print('No negative numbers found')
```

The `else` belongs to the **for loop**.

It runs only if the loop finishes without using `break`.

This makes it useful for:

> Check every position. If any position is invalid, break. Otherwise, place the ship.

### Different example

A program searches a list for a missing value.

```python
for item in items:
    if item == 'Missing':
        break
else:
    print('Everything is present')
```

### Practice

Create a list of numbers.

Use `for...else` to determine whether the list contains a negative number.

### Battleship

Use `for...else` when the CPU checks whether every position required by a ship is available.

If a position contains `S`, use `break`.

If the loop finishes without `break`, the ship can be placed.

Build `setup_cpu()`.

### Test

Run the program several times.

Check that:

* all five ships appear
* ships fit on the board
* ships do not overlap
* the positions change between games

***

[← Previous: Random Ships Must Still Fit](15-random-ships-must-still-fit.md) | [Contents](./) | [Next: The Player Needs To Attack →](17-the-player-needs-to-attack.md)
