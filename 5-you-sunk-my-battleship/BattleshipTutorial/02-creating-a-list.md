# 2. Creating a List

Our board will eventually contain many pieces of information.

Python uses **lists** to store multiple values.

Create an empty list:

```python
items = []
```

Add something to a list using `.append()`:

```python
items.append('Apple')
items.append('Banana')
items.append('Orange')
```

The list now contains:

```text
Apple
Banana
Orange
```

## Different example

A shopping program could create a list of items:

```python
shopping_list = []

shopping_list.append('Milk')
shopping_list.append('Bread')
shopping_list.append('Eggs')
```

## New skill: `for` loops

A `for` loop can repeat instructions a specific number of times.

```python
for i in range(5):
    print('Hello')
```

This prints `Hello` five times.

The variable `i` changes each time the loop repeats.

### Practice

Create an empty list and use a `for` loop to add five `-` symbols to it.

Your list should represent:

```text
- - - - -
```

### Battleship

A Battleship row needs **10 empty positions**.

Create code that produces one row containing ten `-` symbols.

Do not worry about creating the entire board yet.

### Test

Print the row.

You should have ten positions.

---

[← Previous: Planning The Game](01-planning-the-game.md) | [Contents](00-start-here.md) | [Next: Creating A 2D List →](03-creating-a-2d-list.md)
