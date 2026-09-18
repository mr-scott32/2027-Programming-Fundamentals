# 13. Returning Information from a Function

Our setup function creates a board.

Another part of the program will need to use that board.

This is where `return` is important.

For example:

```python
def get_name():
    name = input('Enter your name: ')
    return name
```

We can store the returned value:

```python
player_name = get_name()
```

## Different example

```python
def calculate_area(length, width):
    area = length * width
    return area
```

Then:

```python
room_area = calculate_area(5, 4)
```

`room_area` now contains the returned value.

### Battleship

Your `setup_player()` function needs to return the completed player grid.

Think about the data flow:

```
SetupPlayer
     ↓
PlayerGrid
```

The next part of the program can then store the returned grid.

***

[← Previous: Creating The Player Setup](12-creating-the-player-setup.md) | [Contents](./) | [Next: Creating The Cpu S Ships →](14-creating-the-cpu-s-ships.md)
