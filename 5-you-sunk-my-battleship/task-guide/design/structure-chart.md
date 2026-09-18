---
icon: book-open
---

# Structure Chart

You need to create a structure chart which shows **the main routine (main() function) and all subroutines (other functions).** Likely you will not have many control variables or flags **except for the API request, which will control whether or not you can search the data.**

## Example

The following is an example of the rock collection system (not a real API by the way - but it serves for an example of what your system may look like).

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption><p>Example of a Rock Collection System with all subroutines and API Request</p></figcaption></figure>

### Battleship

How do we structure it? What functions / subroutines do we need to include? Are there any control variables?

**Suggested:**

* Battleship System - Mainline routine
  * Setup CPU - subroutine to setup the main CPU board
    * Must return CPU grid as parameter
  * Setup Player - subroutine to setup player grid.
    * Must return player grid as parameter
  * Setup extra board - a board to track player attacks
    * Must return attack grid as parameter
  * Player turn - subroutine for player's turn
    * Must return attack grid as parameter
  * CPU turn - subroutine for CPU's turn
    * Must return player grid as parameter
  * Check Win - subroutine to check if player has won
    * Must return True/False (control variable)
  * Check Lose - subroutine to check if player has lost
    * Must return True/False (control variable)

## Need More Information?

{% content-ref url="../../../charts-and-algorithms/structure-charts/" %}
[structure-charts](../../../charts-and-algorithms/structure-charts/)
{% endcontent-ref %}
