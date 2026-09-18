---
icon: book-open
---

# main.py

Now that we've got our structure chart and a couple of algorithms, let's start to work through in Python.

{% code title="Main pseudocode:" %}
```
BEGIN

    CPUGrid = SetupCPU()
    PlayerGrid = SetupPlayer()
    BattleGrid = CreateBoard()

    SET GameRunning to TRUE

    WHILE GameRunning = TRUE

        PlayerTurn(BattleGrid, CPUGrid)

        Set WIN to CheckWin(BattleGrid)

        IF Win = TRUE THEN
            OUTPUT "You win!"
            GameRunning = FALSE
        ENDIF

        CPUTurn(PlayerGrid)

        SET lose to CheckLose(PlayerGrid)

        IF Lose = TRUE THEN
            OUTPUT "You lose!"
            GameRunning = FALSE
        ENDIF

    ENDWHILE

END
```
{% endcode %}

```python
def main():
    """Main line - how must it flow?"""
    cpu_grid = setup_cpu()
    player_grid = setup_player()
    battle_grid = create_board()
    game_running = True
    while game_running:
        player_turn(battle_grid, cpu_grid)
        win = check_win(battle_grid)
        if win == True:
            print('You win!')
            break
        cpu_turn(player_grid)
        lose = check_lose(player_grid)
        if lose == True:
            print('You lose :(')
            break
```



