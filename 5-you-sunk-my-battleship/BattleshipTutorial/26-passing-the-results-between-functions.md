# 26. Passing the Results Between Functions

Look at the information produced by the setup functions.

```text
SetupCPU
    ↓
CPUGrid

SetupPlayer
    ↓
PlayerGrid

CreateBoard
    ↓
BattleGrid
```

These values can be stored in variables.

For example:

```python
cpu_grid = setup_cpu()
```

The function creates the grid and returns it.

The returned grid is stored in:

```text
cpu_grid
```

The same principle applies to the player grid and battle grid.

This is one of the most important ideas in the project:

> **Functions can receive information through parameters and send information back using return values.**

---

[← Previous: Bringing Everything Together](25-bringing-everything-together.md) | [Contents](00-start-here.md) | [Next: The Main Game Loop →](27-the-main-game-loop.md)
