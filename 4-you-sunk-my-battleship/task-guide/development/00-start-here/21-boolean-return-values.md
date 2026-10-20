# 21. Boolean Return Values

We now need the function to tell the main program whether the player has won.

A function can return a Boolean.

For example:

```python
def is_even(number):
    if number % 2 == 0:
        return True
    else:
        return False
```

The function returns either:

```
True
False
```

We can store the result:

```python
result = is_even(8)
```

### Battleship

Your `check_win()` function should return:

```
True
```

when all 17 ship positions have been hit.

Otherwise it should return:

```
False
```

This allows another function to decide what happens next.

***

[← Previous: Checking For A Win](20-checking-for-a-win.md) | [Contents](./) | [Next: Creating The Cpu S Turn →](22-creating-the-cpu-s-turn.md)
