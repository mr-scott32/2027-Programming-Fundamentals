# 14. Creating the CPU's Ships

The player chooses where their ships go.

The CPU should not.

Instead, the CPU should choose positions randomly.

Python's `random` module can generate random numbers.

```python
import random
```

Then:

```python
number = random.randint(1, 10)
```

generates a random integer between 1 and 10.

## Different example

A treasure could appear at a random position on a 10 × 10 map:

```python
x = random.randint(0, 9)
y = random.randint(0, 9)
```

Every time the program runs, a different position may be selected.

### Practice

Generate 10 random coordinates.

Print them.

---

[← Previous: Returning Information From A Function](13-returning-information-from-a-function.md) | [Contents](00-start-here.md) | [Next: Random Ships Must Still Fit →](15-random-ships-must-still-fit.md)
