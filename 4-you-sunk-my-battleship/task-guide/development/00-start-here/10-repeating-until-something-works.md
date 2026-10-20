# 10. Repeating Until Something Works

Suppose a player enters an invalid ship placement.

We don't want the program to simply move on to the next ship.

We want it to ask again.

This is where a `while` loop is useful.

```python
valid = False

while valid == False:
    print('Try again')
```

The loop continues while the condition is true.

Eventually, something inside the loop must change the condition.

For example:

```python
valid = False

while valid == False:
    answer = input('Enter Y to continue: ')

    if answer == 'Y':
        valid = True
```

## Why use a Boolean?

A Boolean stores either:

```
True
False
```

This makes it useful for controlling loops.

### Practice

Create a program that repeatedly asks the user to enter a number between 1 and 5.

Stop asking when they enter a valid number.

### Battleship

Use a Boolean variable such as:

```python
placement = False
```

Continue asking for coordinates while the placement is invalid.

Once a valid placement has been made, change the variable so the loop ends.

***

[← Previous: Stopping A Loop](09-stopping-a-loop.md) | [Contents](./) | [Next: Placing Different Ships →](11-placing-different-ships.md)
