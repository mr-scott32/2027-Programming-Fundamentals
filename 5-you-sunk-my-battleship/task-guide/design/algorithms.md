---
icon: book-open
---

# Algorithms

You will need to plan out your **main routine** and then **at least 2 subroutines** using flowcharts and pseudocode. You do **not** need to represent all subroutines from your structure chart, but **do** need to include them all in your **main routine.**

## Example: Rock Collection System

<figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

{% code title="Rock Collect Pseudocode" %}
```
BEGIN main()
    choice = 0
    WHILE choice is not 5
        INPUT choice
        IF choice is 1 THEN
            AddRock
            IF API Request Valid THEN
                SearchRock
            ELSE
                DISPLAY 'Error'
            ENDIF
        ELSEIF choice is 2 THEN
            ViewCollection
        ELSEIF choice is 3 THEN
            CompareRocks
        ELIF choice is 4 THEN
            RemoveRock
        ELSE
            DISPLAY 'Problem between chair and keyboard'
        ENDIF
    ENDWHILE
END main()    
        
```
{% endcode %}

### Battleship Example

{% code title="Mainline Routine" %}
```
BEGIN

    CPUGrid = SetupCPU()
    PlayerGrid = SetupPlayer()
    BattleGrid = CreateBoard()

    SET GameRunning to TRUE

    WHILE GameRunning = TRUE

        PlayerTurn(BattleGrid, CPUGrid)

        Set WIN to CheckWin(BattleGrid)

        IF Win = TRUE THEN
            OUTPUT "You win!"
            GameRunning = FALSE
        ENDIF

        CPUTurn(PlayerGrid)

        SET lose to CheckLose(PlayerGrid)

        IF Lose = TRUE THEN
            OUTPUT "You lose!"
            GameRunning = FALSE
        ENDIF

    ENDWHILE

END
```
{% endcode %}

{% code title="CreateBoard()" %}
```
BEGIN CreateBoard

    Grid = []

    FOR I = 1 TO 10 STEP 1

        Row = []

        FOR J = 1 TO 10
            APPEND "-" TO Row
        NEXT J

        APPEND Row TO Grid

    NEXT I

    RETURN Grid

END CreateBoard
```
{% endcode %}

## Need More Information?

{% content-ref url="../../../charts-and-algorithms/algorithms-flowcharts-pseudocode/" %}
[algorithms-flowcharts-pseudocode](../../../charts-and-algorithms/algorithms-flowcharts-pseudocode/)
{% endcontent-ref %}
