# 27. The Main Game Loop

A game needs to repeat turns.

A Boolean variable can control whether the game is still running:

```python
game_running = True
```

Then:

```python
while game_running:
    ...
```

The game continues until somebody wins.

The overall flow should be:

```text
START

Set up CPU
Set up Player
Create battle grid

WHILE game is running

    Player turn

    Check win

    If player won
        announce winner
        stop game

    CPU turn

    Check lose

    If player lost
        announce loser
        stop game

END
```

Notice that the win and lose checks happen **inside the game loop**.

---

[← Previous: Passing The Results Between Functions](26-passing-the-results-between-functions.md) | [Contents](00-start-here.md) | [Next: Building Main →](28-building-main.md)
