---
icon: book-open
---

# Requirements Definition

Let's start at the beginning. What does the battleship game require?

<details>

<summary>Battleship Rules</summary>

#### **Setup**

* Each player gets a two-sided game unit or tray. The horizontal lower section is the **ocean grid** for your ships, and the vertical upper section is the **targeting grid** to track shots against your opponent.&#x20;
* **The Fleet:** Each player places 5 ships on their ocean grid. Standard sizes are:
  * **Carrier:** 5 holes
  * **Battleship:** 4 holes
  * **Destroyer:** 3 holes
  * **Submarine:** 3 holes
  * **Patrol Boat / Destroyer:** 2 holes \[[1](https://www.google.com/goto?url=CAESaQHrOzAV6IymQnGi0-lsi0btv1HMWBMrnlDUW30SLj70a4tjUwyFBHXhLZLdqFG_p-z2GWCa_nympAeSCyYQgNtQNfWDPQnEkmOTE6Pos13vNitAdq3zNf_IqLR0UO4W089JrOpbBPm46w)]
* **Placement Rules:** Ships must be placed horizontally or vertically—never diagonally. They cannot overlap or hang off the edge of the grid. Players cannot see each other's boards.

#### How to Play

1. Players alternate turns calling out one coordinate (e.g., "D-4") representing a target on their upright tracking grid.
2. The opponent checks their ocean grid at that coordinate.
   * If no ship is there, they call **"Miss."** The attacker places a **white peg** on their targeting grid.
   * If a ship occupies that space, they call **"Hit"** and name the ship (e.g., "Hit, Destroyer"). The attacker places a **red peg** on their targeting grid, and the defender places a red peg on their damaged ship.
3. When all holes of a specific ship are filled with red pegs, it is **sunk**, and the owner must announce that the ship has sunk.

Winning the GameThe first player to completely sink all 5 of their opponent's ships wins the game

</details>

**Now before we start, remember, we are NOT making a 2-player version, we are versing a CPU player.**

#### **1. Functional Requirements** (What the system should do)

What must the system actually allow players to **do?** Consider:

* What input do we need from the player?
* What does the program need to do with this input?
* What information do we need to show the player?
* How does the CPU need to function?

#### **2. Non-Functional Requirements** (How the system should work)

Consider what is not required, but would improve the user experience, performance or security.

* What makes a user experience better for a player?
* What level of performance is expected from a game?
* Are there any security issues?



## Example Requirements

**Functional requirements**

* The game must allow player and CPU to place ships.
* The game must allow player and CPU to fire at opposing ships.
* The game must determine whether each shot is a hit or miss.
* The game must determine when a player has won.
* The game must obscure the CPU's grid.&#x20;

**Non-functional requirements**

* The game must be easy to use.
* The game must respond quickly to player input.
* The game must have clear instructions.



