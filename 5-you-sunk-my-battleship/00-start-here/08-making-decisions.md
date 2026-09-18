# 08. Making Decisions

We now need to determine whether a ship can be placed.

Python uses `if` statements to make decisions.

```python
if score >= 50:
    print('Pass')
```

We can also use `else`:

```python
if score >= 50:
    print('Pass')
else:
    print('Fail')
```

We can combine conditions using logical operators.

For example:

```python
if age >= 13 and age <= 17:
    print('Teenager')
```

We can use `or` when either condition can be true:

```python
if answer == 'Y' or answer == 'y':
    print('Yes')
```

## Different example

A game character can enter a door only if they have a key:

```python
if has_key == True:
    print('Door opens')
else:
    print('Door remains locked')
```

### Practice

Write a program that checks whether a number is between 1 and 10.

### Battleship

When placing a ship, check whether each position already contains a ship.

If it does, the placement is invalid.

If it does not, the ship can potentially be placed.

***

[← Previous: Repeating Across Multiple Positions](07-repeating-across-multiple-positions.md) | [Contents](./) | [Next: Stopping A Loop →](09-stopping-a-loop.md)
