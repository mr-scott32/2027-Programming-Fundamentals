# 11. Placing Different Ships

We now have a problem.

Battleship has several ships:

```text
Carrier       5
Battleship    4
Cruiser       3
Submarine     3
Destroyer     2
```

We could write separate code for every ship, but that would create a lot of repetition.

Instead, we can store related information in a **dictionary**.

A dictionary stores values using keys.

For example:

```python
prices = {
    'Bread': 4,
    'Milk': 3,
    'Eggs': 6
}
```

The item is the key.

The number is the value.

---

## Looping through a dictionary

The `.items()` method lets us retrieve both the key and value:

```python
for item, price in prices.items():
    print(item, price)
```

This produces each item and its price.

### Different example

```python
players = {
    'Alex': 25,
    'Jordan': 31,
    'Taylor': 18
}
```

A loop can process every player and their score.

### Practice

Create a dictionary containing three games and their ages.

Use `.items()` to print each game and its age.

### Battleship

Create a dictionary containing all five ships and their lengths.

Then use `.items()` to process each ship.

Your program should now be able to use the **same placement code** for ships of different lengths.

---

[← Previous: Repeating Until Something Works](10-repeating-until-something-works.md) | [Contents](00-start-here.md) | [Next: Creating The Player Setup →](12-creating-the-player-setup.md)
