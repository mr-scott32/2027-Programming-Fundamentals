# My Solution

{% code title="main.py" %}
```py
def create_board():
    """Start here - need to create matrix to house the grid. How do we do so? 
    How many lines do we need? What symbol to use to represent?"""

    grid = []
    for i in range(10):
        row = []
        for j in range(10):
            row.append('-')

        grid.append(row)
    return grid
```
{% endcode %}
