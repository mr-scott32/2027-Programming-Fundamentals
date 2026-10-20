# 01. Planning the Game

Before writing code, we need to decide what the program needs to do.

A large program is easier to develop when it is divided into smaller tasks. Each task can be placed inside its own **function**.

Our Battleship program will eventually contain functions for:

```
CreateBoard
SetupPlayer
SetupCPU
PlayerTurn
CheckWin
CPUTurn
CheckLose
Main
```

Each function should have one main responsibility.

For example:

```
CreateBoard
    Creates an empty game board.

SetupPlayer
    Allows the player to place their ships.

SetupCPU
    Places the CPU's ships randomly.

PlayerTurn
    Allows the player to attack.

CheckWin
    Checks whether the player has won.

CPUTurn
    Allows the CPU to attack.

CheckLose
    Checks whether the player has lost.

Main
    Controls the overall game.
```

## New skill: Functions

A function is a named section of code that performs a particular task.

For example:

```python
def say_hello():
    print('Hello!')
```

The function does not run just because we have created it.

We call it:

```python
say_hello()
```

## Different example

Imagine a program that needs to display a menu.

```python
def display_menu():
    print('1. Start')
    print('2. Instructions')
    print('3. Quit')

display_menu()
```

The function has one clear job: displaying the menu.

### Practice

Create a function called `display_rules()` that prints three rules for a game.

### Battleship

Before writing `CreateBoard`, write down:

* What does the function need to do?
* What information does it need?
* What should it produce?

***

[← Previous: Start Here](./) | [Contents](./) | [Next: Creating A List →](02-creating-a-list.md)
