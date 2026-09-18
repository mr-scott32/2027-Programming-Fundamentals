# 15. Random Ships Must Still Fit

Randomly choosing a starting position is not enough.

Imagine a 5-space ship starts in column 8.

It would need:

```text
8 9 10 11 12
```

which does not fit.

We therefore need to restrict the possible starting position.

For a ship of length `v` on a 10-position row, the starting coordinate needs to account for the ship's length.

For example, a length of 5 can start at:

```text
0 1 2 3 4 5
```

but not 6, 7, 8 or 9.

### Practice

For a board of 10 positions, work out the largest possible starting position for:

```text
Length 2
Length 3
Length 4
Length 5
```

### Battleship

Use the ship length when generating the CPU's starting coordinate.

The CPU should:

1. Randomly choose horizontal or vertical.
2. Randomly choose a valid starting coordinate.
3. Check whether the positions are already occupied.
4. If they are occupied, try again.
5. Otherwise, place the ship.

---

[← Previous: Creating The Cpu S Ships](14-creating-the-cpu-s-ships.md) | [Contents](00-start-here.md) | [Next: Checking Every Position →](16-checking-every-position.md)
