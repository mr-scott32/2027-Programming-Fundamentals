# 31. Debugging

When your program does not work, do not immediately rewrite it.

First identify **which function is causing the problem**.

For example:

```
The board is wrong
    ↓
Check CreateBoard

Ships overlap
    ↓
Check SetupPlayer or SetupCPU

Player attacks the wrong position
    ↓
Check PlayerTurn

Winner is detected incorrectly
    ↓
Check CheckWin

CPU attacks incorrectly
    ↓
Check CPUTurn
```

You can also temporarily print variables.

For example:

```python
print(x_pos)
print(y_pos)
```

This lets you see what values the program is actually using.

***

[← Previous: Testing The Complete Game](../../development/00-start-here/30-testing-the-complete-game.md) | [Contents](../../development/00-start-here/) | [Next: Important Python Skills You Have Used →](../../development/00-start-here/32-important-python-skills-you-have-used.md)
