# 17. The Player Needs to Attack

The player now has a grid and the CPU has a hidden grid.

We need another grid to show the player what has happened during the battle.

For example:

```text
- - - - -
- - O - -
- - - X -
- - - - -
- - - - -
```

Here:

```text
X = hit
O = miss
- = not yet selected
```

The player's battle grid therefore stores the results of their attacks.

The CPU grid stores the CPU's ships.

---

[← Previous: Checking Every Position](16-checking-every-position.md) | [Contents](00-start-here.md) | [Next: Passing Multiple Grids To A Function →](18-passing-multiple-grids-to-a-function.md)
