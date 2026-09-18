# 30. Testing the Complete Game

Do not simply play one game and decide that the program works.

Test individual parts deliberately.

## Board testing

Check that:

* the board has 10 rows
* every row has 10 positions
* every position starts as `-`

## Player setup testing

Check that:

* each ship can be placed horizontally
* each ship can be placed vertically
* ships cannot overlap
* ships fit on the board
* all five ships are placed

## CPU setup testing

Run the program multiple times.

Check that:

* ships appear in different positions
* ships fit on the board
* ships do not overlap

## Player attack testing

Check:

* a hit
* a miss
* attacking the same position twice
* a valid coordinate
* an invalid coordinate

## Win testing

Create a test grid containing exactly 17 `X` values.

Check that:

```text
CheckWin → True
```

Then remove one `X`.

Check that:

```text
CheckWin → False
```

## Lose testing

Perform the same type of testing for `CheckLose`.

---

[← Previous: Calling Main](29-calling-main.md) | [Contents](00-start-here.md) | [Next: Debugging →](31-debugging.md)
