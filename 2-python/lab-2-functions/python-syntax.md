---
icon: book-open
---

# Python Syntax

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

### Using Parameters and Return Statements

All of the above pretty much do the same thing, but the last one is really important. With one function it's not that powerful, but imagine we made a game and you had a `player_attack`, `enemy_attack`, and `check_status` function.&#x20;

* `player_attack` would need to receive parameters for player strength, enemy health and enemy defense and return the enemy's health after calculations have been made.
* `enemy_attack` would need to do the same with enemy strength, player health and player defense.
* `check_status` might need to receive damage dealt from `player_attack` and \`enemy\_attack\_ to determine if someone has lost all their health. It would need to return a `True` or `False` value, which can then be used to break the game loop if someone is out of health.
* The main routine would then need to loop the above functions until someone is out of health. It would need to store each of the return values of `player_attack` and `enemy_attack` in a variable and the return value of `check_status` in a variable which can then be checked with an IF statement.

**None of the above is possible to track consistently without effective parameter passing and effective use of return statements, so that we can pass values from function to function.**

**Here is what it might look like:**

<pre class="language-py" data-title="" data-overflow="wrap"><code class="lang-py"># Usually best to declare variables first.
# This can be made cleaner when we learn about classes and objects in Term 2.
player_str = 5
enemy_str = 3
player_def = 2
enemy_def = 1
player_health = 10
enemy_health = 7
status = True # Keeps the game loop going.

def player_attack(p_att, e_def, e_health): # Need player attack and enemy defense / health.
  e_health -= (p_att - e_def)
  print(f'Player attacks! Enemy health is now {e_health}')
  return e_health # returns updated enemy health for external use

def enemy_attack(e_att, p_def, p_health): # Need enemy attack and player defense / health.
  p_health -= (e_att - p_def)
  print(f'Enemy attacks! Player health is now {p_health}')
  return p_health # returns updated player health for external use
  
def check_status(e_health, p_health): # Need enemy and player health to check if game over
  if e_health &#x3C;= 0:
    print('You win!')
    return False # Returns 'False', suggesting status of game is over.
  elif p_health &#x3C;=0:
    print('You lose!')
    return False # Returns 'False', suggesting status of game is over.
  else:
    print('Play on!')
    return True
<strong> 
</strong><strong># Mainline routine - game loop. Runs until status changes to False  
</strong>while status == True:
# We need to reset enemy_health and player_health to the result of attack functions.
# This will update the health after calculations are made in each function.
  enemy_health = player_attack(player_str, enemy_def, enemy_health)
  player_health = enemy_attack(enemy_str, player_def, player_health)
  # returns False if someone drops to 0 health or less
  status = check_status(enemy_health, player_health)  
</code></pre>

### **A Different Game Example**

```py
lives = 3

def player_movement(keypress):
    if keypress.lower() == 'w':
        return 'You jump' # These would be functions normally, but printing for show here.
    elif keypress.lower() == 'a':
        return 'Move left'
    elif keypress.lower() == 'd': 
        return 'Move right'
    elif keypress.lower() == 's': 
        return 'Crouch'
    else:
        return 'Stay idle'

while lives > 0:
    keypress = input('Enter W, A, D or S to move: ')
    print(player_movement(keypress)) # We can also print the return value of a function.
    player_spikes = True #Just to test this out
    
    if player_spikes:
        lives -= 1

print("You lost all 3 lives, you lose!")

```
