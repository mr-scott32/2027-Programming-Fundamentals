---
icon: book-open
---

# Pseudocode Algorithms

### Greet User <a href="#id-6.-functions-subroutines" id="id-6.-functions-subroutines"></a>

```py
def greet_user():
    print("Hello!")
    
greet_user()
```

What if we add parameters? We can have it so functions require parameters which need to be filled in each time the function is called. This is generally better practice as it allows us to feed variables into our functions.

{% code title="" overflow="wrap" %}
```python
def greet_user(username): # When function is called the username needs to be provided.
    print(f"Hello {username}!")

user = input('Enter username: ')
greet_user(user) #This will feed in our above input into the function.
```
{% endcode %}

However, what if I wanted to grab a variable from my function and use it somewhere else? Well, that's where return statements come in.

{% code title="" overflow="wrap" %}
```python
def greet_user(username): 
    greeting = f"Hello {username}!"
    return greeting # This will return greeting as a value I can store in a variable.

user = input('Enter username: ')

# This will store my return value from the function into the greeting variable.
greeting = greet_user(user) 
print(greeting)
```
{% endcode %}

All of the above pretty much do the same thing, but the last one is really important. With one function it's not that powerful, but imagine we made a game and you had a `player_attack`, `enemy_attack`, `damage_calculation`, `player_health` and `enemy_health` function.&#x20;

* `player_attack` would need to feed attack values to the `damage_calculation` function and return how much damage was caused (armour, enemy defenses, etc).
* `enemy_attack` would need to do the same.
* `enemy_health` might need to receive damage dealt from `player_attack` and determine if the enemy has health remaining. `player_health` and `enemy_attack` may work in a similar way.

**None of the above is possible to track consistently without effective parameter passing and effective use of return statements, so that we can pass values from function to function.**

### **A Different Game Example**

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
