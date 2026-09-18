# 24. Handling Invalid Input

So far, we have assumed that the user enters numbers correctly.

What happens if they enter:

```
hello
```

instead of:

```
5
```

This can cause a Python error when using `int()`.

Python provides `try` and `except` for handling errors.

For example:

```python
try:
    number = int(input('Enter a number: '))
except:
    print('Please enter a number')
```

Python attempts the code inside `try`.

If an error occurs, the `except` code runs.

## Different example

```python
try:
    age = int(input('Enter your age: '))
    print(age)
except:
    print('That was not a valid number.')
```

### Practice

Create a program that asks for a number and handles a non-number input.

### Battleship

Use error handling where coordinate input could cause the program to fail.

Your program should respond with an appropriate message rather than crashing.

***

[← Previous: Checking For A Loss](23-checking-for-a-loss.md) | [Contents](./) | [Next: Bringing Everything Together →](25-bringing-everything-together.md)
