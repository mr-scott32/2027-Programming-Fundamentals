# 09. Stopping a Loop

Sometimes we need to stop a loop before it reaches the end.

Python provides `break`.

For example:

```python
for i in range(10):
    if i == 5:
        break
    
    print(i)
```

The loop stops when `i` reaches 5.

## Different example

Imagine searching for a particular name:

```python
for name in names:
    if name == 'Sam':
        print('Found!')
        break
```

Once the name is found, there is no reason to keep searching.

### Practice

Create a loop that checks five numbers.

If one of the numbers is negative, stop the loop.

### Battleship

When checking the positions a ship would occupy:

> If any position is already occupied, the placement should be rejected.

Use `break` to stop checking once an invalid position is found.

***

[← Previous: Making Decisions](08-making-decisions.md) | [Contents](./) | [Next: Repeating Until Something Works →](10-repeating-until-something-works.md)
