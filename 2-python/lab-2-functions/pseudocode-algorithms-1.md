---
icon: book-open
---

# Pseudocode Algorithms

### Function Examples in Python <a href="#id-6.-functions-subroutines" id="id-6.-functions-subroutines"></a>



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
        READ keypress
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
