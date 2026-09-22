---
icon: book-open
---

# Pseudocode Algorithms

### What Is Pseudocode? <a href="#what-is-pseudocode" id="what-is-pseudocode"></a>

**Pseudocode** is a way to plan your program **before you write real code**. It’s not a programming language — it's like writing instructions in plain English using code-like logic.

You use **pseudocode** to describe:

* What the program **should do**
* What steps to follow
* What logic or decisions are involved

***

**Why Use Pseudocode?**

* ✅ It helps you **think through the logic** before you write code
* ✅ It’s easier to understand than real code
* ✅ It’s not tied to any specific programming language
* ✅ It helps teams **communicate ideas clearly**



### Pseudocode Building Blocks <a href="#pseudocode-building-blocks" id="pseudocode-building-blocks"></a>

#### 1. BEGIN and End <a href="#id-1.-begin-and-end" id="id-1.-begin-and-end"></a>

Every program has a BEGIN and end.

```
BEGIN
  ...
END
```

#### 2. Variables - Sequence <a href="#id-2.-variables-sequence" id="id-2.-variables-sequence"></a>

Use `SET` to create and store values.

```
SET score TO 0
```

#### 3. Input and Output - Sequence <a href="#id-3.-input-and-output-sequence" id="id-3.-input-and-output-sequence"></a>

Use `GET` to get info, and `DISPLAY` to show info.

```
GET name
DISPLAY "Welcome", name
```

**Example Program**

```
BEGIN 
    GET age
    DISPLAY "You are", age, "old!"
END
```

#### 4. Decision Making (IF statements) - Branching / Selection <a href="#id-4.-decision-making-if-statements-branching-selection" id="id-4.-decision-making-if-statements-branching-selection"></a>

```
IF score >= 50 THEN
    DISPLAY "You passed!"
ELSE
    DISPLAY "Try again"
ENDIF
```

**Example Program**

```
BEGIN player_movement 
    GET keypress 
    IF keypress is W THEN 
        jump 
    ELSEIF keypress is A THEN 
        move_left 
    ELSEIF keypress is D THEN 
        move_right 
    ELSEIF keypress is S THEN 
        crouch 
    ELSE stay_idle 
    ENDIF 
END player_movement
```

#### 5. Loops (WHILE / REPEAT / FOR) - Iteration / Repetition <a href="#id-5.-loops-while-repeat-for-iteration-repetition" id="id-5.-loops-while-repeat-for-iteration-repetition"></a>

**Pre-Test Loop - WHILE**

Pre-test loops tesat the condition **before** the block of code runs, then continue to run until the condition is no longer true.

<a class="button secondary">Copy</a>

```
i = 0
WHILE i < 5
    DISPLAY i
    i = i + 1
ENDWHILE
```

The above would display 0, 1, 2, 3, 4, but not 5 as it is a pre-test loop (once i is equal to 5, it stops won't run again).

<a class="button secondary">Copy</a>

```
WHILE lives > 0 DO
    DISPLAY "Keep playing"
    SUBTRACT 1 FROM lives
ENDWHILE
```

In the above, once lives are 0 or less, the following code will not display "Keep playing", as the while loop will first check to see if lives are more than zero, then skip past the block once lives are 0 or less.

#### **Post-Test Loop - REPEAT**

Post-test loops are a bit different. They will always run the code at least once, then test the condition at **the end of the block of code.** A REPEAT UNTIL loop actually runs until a condition BECOMES true.

<a class="button secondary">Copy</a>

```
i = 0
REPEAT 
    DISPLAY i
    i = i + 1
UNTIL i > 5
```

The above would show 0, 1, 2, 3, 4, 5, as it is tested at the end of the loop, not at the start.

<a class="button secondary">Copy</a>

```
lives = 3
REPEAT
    DISPLAY "Keep playing"
    SUBTRACT 1 FROM lives
UNTIL lives <= 0
```

In the above, the code effectively does the same thing, but will always run at least once. So even if lives are at 0 before the first runthrough, it will run.

#### **Counted Loop - FOR/NEXT**

A counted loop will run for a certain amount of time. This is useful when going over a list / array of items. For now, let's just think in terms of running a certain number of times.

How they work is they have a range (let's see from 0 to 3) and an **iterator variable** (often just declared as 'i'), which gets added to (i.e. iterates) after the code is run each time. Once iterator variable ('i' for instance) reaches the end of the range, the loop ends.

As we mostly use Python at this school, we'll call this a **pre-test loop** - it gets tested BEFORE each time the code runs.

```
FOR i = 0 TO 5 STEP 1
    DISPLAY i
NEXT i
```

For the above, the output would be 0, 1, 2, 3, 4, but not 5, as it is pre-test - once i becomes 5, it goes back to start, checks the condition, and confirms that 5 is at the end of the range. As the STEP is 1, i increases by 1 every time the loop is run. But what if we set this higher...

```
FOR i = 0 TO 5 STEP 2
    DISPLAY i
NEXT i 
```

The above would output 0, 2, 4, as i is increasing by TWO each time.

```
FOR level = 1 TO 4 STEP 1
    DISPLAY "Level", level
NEXT level
```

The above would output **Level 1, Level 2, Level 3,** as the value starts at 1, not 0.

**Example Programs**

```
BEGIN platformer_game
    SET lives to 3
    WHILE health > 0 DO
        GET keypress
        IF keypress is W THEN
            jump
        ELSEIF keypress is A THEN
            move_left
        ELSEIF keypress is D THEN
            move_right
        ELSEIF keypress is S THEN
            crouch
        ELSE 
            stay_idle
        ENDIF
    
        IF player_overlaps_spikes THEN
            SUBTRACT 1 FROM lives
        ENDIF
    ENDWHILE
    DISPLAY "You lost all 3 lives, you lose!"
END
```

```
BEGIN turns
    DISPLAY "You have 3 turns"
    FOR turn FROM 0 to 3 STEP 1
        DISPLAY "Have your turn"
        Display turn, " turn(s) remaining."
    NEXT turn
    DISPLAY "No turns remaining."
END turns
```

