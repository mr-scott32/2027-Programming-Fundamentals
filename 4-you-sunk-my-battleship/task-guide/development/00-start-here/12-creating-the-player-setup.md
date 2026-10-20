# 12. Creating the Player Setup

We now have nearly all of the skills required to create the player's setup.

The function needs to:

```
Create a board
Create a list/dictionary of ships
Process each ship
Ask whether it is horizontal or vertical
Ask for coordinates
Check whether the placement is valid
Place the ship
Repeat if necessary
Display the board
Return the board
```

## New skill: Parameters

A parameter allows information to be passed into a function.

For example:

```python
def display_score(score):
    print(score)
```

The value is supplied when the function is called:

```python
display_score(85)
```

### Different example

```python
def calculate_total(price, quantity):
    total = price * quantity
    print(total)
```

The function receives two pieces of information.

### Battleship

Your placement code needs to know the length of the current ship.

The dictionary already provides this value.

Use that value when determining how many positions the ship occupies.

Build your `setup_player()` function now.

### Test

Before continuing, test:

* a horizontal ship
* a vertical ship
* a ship of a different length
* two ships that do not overlap
* an attempted overlapping placement

***

[← Previous: Placing Different Ships](11-placing-different-ships.md) | [Contents](./) | [Next: Returning Information From A Function →](13-returning-information-from-a-function.md)
