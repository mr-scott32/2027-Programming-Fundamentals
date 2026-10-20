# 28. Building Main

Now create your `main()` function.

It should call the other functions in the correct order.

Your program should follow this structure:

```
main
│
├── setup_cpu
│
├── setup_player
│
├── create_board
│
└── while game is running
    │
    ├── player_turn
    │
    ├── check_win
    │
    ├── cpu_turn
    │
    └── check_lose
```

Do not put all of the game logic inside `main()`.

The purpose of your functions is to keep the individual tasks separate.

***

[← Previous: The Main Game Loop](27-the-main-game-loop.md) | [Contents](./) | [Next: Calling Main →](29-calling-main.md)
