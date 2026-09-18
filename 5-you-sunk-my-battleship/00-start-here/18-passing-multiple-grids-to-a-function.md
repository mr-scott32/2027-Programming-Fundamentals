# 18. Passing Multiple Grids to a Function

Our player-turn function needs two grids:

```
BattleGrid
CPUGrid
```

A function can receive multiple parameters.

For example:

```python
def compare_scores(score1, score2):
    if score1 > score2:
        print('Score 1 wins')
    else:
        print('Score 2 wins')
```

The function receives two values.

### Battleship

Your player-turn function needs to receive:

```
battle_grid
cpu_grid
```

Think carefully about what each grid is used for.

```
CPUGrid
    What ships actually exist?

BattleGrid
    What attacks has the player already made?
```

Build the beginning of `player_turn()`.

***

[← Previous: The Player Needs To Attack](17-the-player-needs-to-attack.md) | [Contents](./) | [Next: Checking A Player S Attack →](19-checking-a-player-s-attack.md)
