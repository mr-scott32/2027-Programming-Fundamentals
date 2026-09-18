# 6. Getting Coordinates from the Player

A player needs to tell the program where they want to place a ship.

We can use `input()`.

```python
name = input('Enter your name: ')
```

`input()` produces text.

If we need a number, we can convert the input using `int()`:

```python
age = int(input('Enter your age: '))
```

## Different example

A game might ask:

```python
x = int(input('Enter the X coordinate: '))
y = int(input('Enter the Y coordinate: '))
```

The player could enter:

```text
2
5
```

The variables now contain integers.

### Practice

Write a program that asks the user for:

* a row
* a column

Then print both values.

### Battleship

Add coordinate input to your ship-placement program.

You need:

```text
x_pos
y_pos
```

These will represent the starting position of a ship.

---

[← Previous: Displaying A Grid](05-displaying-a-grid.md) | [Contents](00-start-here.md) | [Next: Repeating Across Multiple Positions →](07-repeating-across-multiple-positions.md)
