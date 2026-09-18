# 19. Checking a Player's Attack

The player enters:

```text
x coordinate
y coordinate
```

The program uses those coordinates to look at the CPU grid.

If the CPU grid contains a ship:

```text
Hit
```

Otherwise:

```text
Miss
```

The program then changes the battle grid.

For example:

```text
X
```

for a hit and:

```text
O
```

for a miss.

## Combining conditions

We also need to prevent the player from attacking the same position twice.

A condition can contain several checks:

```python
if condition1 and condition2:
    ...
```

or:

```python
if condition1 or condition2:
    ...
```

### Practice

Create a small grid.

Ask the user for a coordinate.

Check whether the position contains `X`.

If it does, print that the position has already been selected.

### Battleship

Complete the logic for `player_turn()`.

It should:

1. Display the battle grid.
2. Ask for coordinates.
3. Check the CPU grid.
4. Determine hit or miss.
5. Update the battle grid.
6. Prevent the same position being selected again.
7. Finish the player's turn after a valid attack.

---

[← Previous: Passing Multiple Grids To A Function](18-passing-multiple-grids-to-a-function.md) | [Contents](00-start-here.md) | [Next: Checking For A Win →](20-checking-for-a-win.md)
