# 22. Creating the CPU's Turn

The CPU now needs to attack the player's ship grid.

The basic process is similar to the player's turn:

```
Choose coordinates
        ↓
Check the player's grid
        ↓
Hit or miss
        ↓
Change the grid
```

The major difference is that the CPU does not use `input()`.

Instead, it generates coordinates randomly.

### Battleship

Create `cpu_turn()`.

It should:

* generate a random row
* generate a random column
* check whether that position has already been attacked
* determine hit or miss
* update the player's grid
* finish the CPU turn

Use the skills you have already learned rather than creating a completely new approach.

***

[← Previous: Boolean Return Values](21-boolean-return-values.md) | [Contents](./) | [Next: Checking For A Loss →](23-checking-for-a-loss.md)
