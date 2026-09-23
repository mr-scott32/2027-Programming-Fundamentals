---
icon: book-open
---

# Python Syntax

If you're still learning Python, refer back to this page for Python versions of all the Pseudocode examples from the previous pages:

### Python Algorithms <a href="#pseudocode-building-blocks" id="pseudocode-building-blocks"></a>

#### 1. BEGIN and End <a href="#id-1.-begin-and-end" id="id-1.-begin-and-end"></a>

We don't really need this in Python, you can just start programming.

#### 2. Variables - Sequence <a href="#id-2.-variables-sequence" id="id-2.-variables-sequence"></a>

To create a variable, we name the variable, put an equals symbol and assign the value. For example:

```py
score = 0 # Integer (whole number)
bank_balance = 150.35 # Float (decimal number)
text_message = "Hey!" # String (raw characters)
winning = True # Boolean (True / False value)
```

We create code comments with hashtags (`#`) - they do not impact the code, but allow us to leave messages explaining code.

#### 3. Input and Output - Sequence <a href="#id-3.-input-and-output-sequence" id="id-3.-input-and-output-sequence"></a>

We us `print()` to Output, and `input()` to receive input. We can set variables to receive input.

For example:

```py
name = input('Enter your name: ') # By default input receives a string
print('Welcome ', name)

# Another option to format strings - easier when working with variables:
print(f'Welcome {name}')
```

**Example Program**

```py
# We can set input to receive other data types like integers
age = int(input('Enter age: ')) 
print(f'You are {age} years old.')

```

#### 4. Decision Making (IF statements) - Branching / Selection <a href="#id-4.-decision-making-if-statements-branching-selection" id="id-4.-decision-making-if-statements-branching-selection"></a>

These look quite similar to pseudocode, though it's lower case, you must include a colon (`:`) and you **must** indent (use tab on your keyboard) everything within each IF block.

```py
score = int(input('Enter score: ')
if score >= 50:
    print('You passed!')
else:
    print("Try again")

```

**Example Program**

```python
keypress = input('Enter W, A, D or S to move: ')
if keypress.lower() == 'w':
    print('You jump') # These would be functions normally, but printing for show here.
elif keypress.lower() == 'a':
    print('Move left)
elif keypress.lower() == 'd': 
    print('Move right')
elif keypress.lower() == 's': 
    print('Crouch')
else:
    print('Stay idle')

# Adding .lower() to keypress converts it to lower case - easier to catch simple errors.
```

#### 5. Loops (WHILE / REPEAT / FOR) - Iteration / Repetition <a href="#id-5.-loops-while-repeat-for-iteration-repetition" id="id-5.-loops-while-repeat-for-iteration-repetition"></a>

Python only works with pre-test loops, so we'll only look at While loops and For loops.

**Pre-Test Loop - WHILE**

```py
i = 0
while i < 5:
    print(i)
    i += 1 # this means the same as i = i + 1, but is more efficient
```

The above would display 0, 1, 2, 3, 4, but not 5 as it is a pre-test loop (once i is equal to 5, it stops won't run again).

```python
lives = 3
while lives > 0:
    print("Keep playing")
    lives -= 1 # Means the same lives = lives - 1, but more efficient
```

In the above, once lives are 0 or less, the following code will not display "Keep playing", as the while loop will first check to see if lives are more than zero, then skip past the block once lives are 0 or less.

#### **Break Statements**

While Python does not do post-test loops, you can use 'break' statements to terminate a loop.

```python
lives = 3
while True:
    lives -= 1
    if lives <= 0:
        break
```

In the above, the code effectively does the same thing, but will always run at least once, even if lives start at 0. It will then break the loop once lives are 0 or less, but only after it has run at least once.

#### **Counted Loop - FOR/NEXT**

A counted loop will run for a certain amount of time. This is useful when going over a list / array of items. For now, let's just think in terms of running a certain number of times.

How they work is they have a range (let's say from 0 to 5) and an **iterator variable** (often just declared as 'i'), which gets added to (i.e. iterates) after the code is run each time. Once iterator variable ('i' for instance) reaches the end of the range, the loop ends.

```python
for i in range(5)
    print(i)
```

For the above, the output would be 0, 1, 2, 3, 4, but not 5, as it is pre-test - once i becomes 5, it goes back to start, checks the condition, and confirms that 5 is at the end of the range. As the STEP is 1, i increases by 1 every time the loop is run. But what if we set this higher...

```py
for i in range(0, 5, 2): #1st number is start of range, 2nd is end of range, 3rd is step
    print(i)
```

The above would output 0, 2, 4, as i is increasing by TWO each time.

```python
for level in range (1, 4): #We can start from 1 in the range.
  print(f'Level {level}')
  
  """Remember, to display Level 3 in Python, we had to set the range to 4 as 
  Python for loops EXCLUDE the end of range value"""
```

The above would output **Level 1, Level 2, Level 3,** as the value starts at 1, not 0.

**Example Programs**

```py
lives = 3

while lives > 0:

    keypress = input('Enter W, A, D or S to move: ')
    
    if keypress.lower() == 'w':
        print('You jump') # These would be functions normally, but printing for show here.
    elif keypress.lower() == 'a':
        print('Move left')
    elif keypress.lower() == 'd': 
        print('Move right')
    elif keypress.lower() == 's': 
        print('Crouch')
    else:
        print('Stay idle')
        
    player_spikes = True #Just to test this out
    
    if player_spikes:
        lives -= 1

print("You lost all 3 lives, you lose!")

```

```py
print("You have 3 turns")
for turn in range(3, 0, -1): #We move from 3 down to 0, exclusive of end of range (0).
    print("Have your turn")
    print(f'{turn} turn(s) remaining.')

print("No turns remaining.")

```
