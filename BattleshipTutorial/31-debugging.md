# 31. Debugging

When your program does not work, do not immediately rewrite it.

First identify **which function is causing the problem**.

For example:

```text
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

---

[← Previous: Testing The Complete Game](30-testing-the-complete-game.md) | [Contents](00-start-here.md) | [Next: Important Python Skills You Have Used →](32-important-python-skills-you-have-used.md)
