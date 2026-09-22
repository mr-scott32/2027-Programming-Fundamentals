---
icon: book-open
---

# Pseudocode Algorithms

### Functions / Subroutines <a href="#id-6.-functions-subroutines" id="id-6.-functions-subroutines"></a>

Now in terms of our programs, to keep everything efficient in Python we create a `main()` function then reference various other functions in `main()`. When considering algorithms, we call this a **mainline** and **subroutines.**

A subroutine is essentially a function which is called into the mainline. The algorithm for the subroutine is referenced in the mainline, but is actually created separately. This is similar to how a Python function can be used in the main() function, but is created in a different area.

This helps to keep our algorithms efficient, readable and useable.

It is important to start complex algorithms with a clear, uncluttered mainline. The mainline should reference required subroutines, the details of which are shown in separate algorithms.

Each subroutine should be concise and correctly make use of further subroutines for detailed logic.

For advice on designing and representing algorithms with flowcharts and pseudocode, please look through the following document.

**Note:** These are directly from NESA, but keep in mind the **Nested IF page is incorrect.**

{% file src="../../.gitbook/assets/Algorithms, Flowcharts, Pseudocode (2).PDF" %}

### Examples

```
BEGIN greet_user
    DISPLAY "Hello!"
END greetUser
```

```
BEGIN
    greet_user
END
```

### **Game Example**

```
BEGIN player_movement(keypress)
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
END player_movement   

BEGIN    
    SET lives to 3
    WHILE health > 0 DO
        GET keypress
        player_movement(keypress)
        IF player_overlaps_spikes THEN
            SUBTRACT 1 FROM health
        ENDIF
    ENDWHILE
    DISPLAY "You lost all 3 lives, you lose!"
END
```



### Robotics Example

#### Flowchart for One Subroutine and Mainline Routine <a href="#flowchart-for-one-subroutine-and-mainline-routine" id="flowchart-for-one-subroutine-and-mainline-routine"></a>

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

```
BEGIN detect_object
    WHILE distance > 100mm
        READ distance
        Drive Forwards
    ENDWHILE
    Turn right 90 degrees
END detect_object


BEGIN
    detect_object
    collect_yellow
    detect_line
    collect_red
    drive_home
END  
```
