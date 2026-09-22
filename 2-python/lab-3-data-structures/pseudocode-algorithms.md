---
icon: book-open
---

# Pseudocode Algorithms

### NESA Specifications

Here's an example of a pseudocode algorithm and flowchart going over an array. Even though the same course specifications state that flowcharts are generally not used for anything other than control structures, they included one anyway:

<div align="left"><figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure></div>

### Pseudocode Conventions

The only thing to really be aware of here when comparing the pseudocode with Python, is that in Python the **end value of a range of a For loop is EXCLUSIVE - for instance, `for i in range(5)` will include 0-4, not 5.**

Pseudocode is different - it is **INCLUSIVE** of the end value of a range. For instance, `FOR i = 0 TO 5 STEP 1` will include **0-5.**

This can matter, because if we need to iterate over the **full length of an array / list,** in Python we just put something like `for item in groceries:` , but in pseudocode, we might need to put `FOR item = 0 to LEN(groceries)-1`, as if we did not add minus 1 the inclusive nature of the FOR / NEXT loop would take us beyond the range of the array. For instance, if we had a list of `test_scores` which was `[99, 70, 80, 65, 91]`, but only wanted to display those over 90...

#### In Python:

{% code title="main.py" overflow="wrap" %}
```py
for score in test_scores:
    if score > 90:
        print(score)
```
{% endcode %}

Another way of writing this could be...

{% code title="main.py" overflow="wrap" %}
```python
for i in range(len(test_scores)):
    if test_scores[i] > 90:
        print(test_scores[i])
```
{% endcode %}

The above shows us what is kind of really going on - we're looping over the length of the list, and whilst `i` starts at 0, because Python for loops are **EXCLUSIVE** of the end range value, we do not go outside of the range of the list.

To explain, let's say the list has 5 test values - if we used the full length of test scores, the loop would run **5 times (0-5), becuase we run 0-4 and exclude the 5.**

#### In Pseudocode

{% code title="Mainline Routine" overflow="wrap" %}
```
FOR i = 0 to LEN(test_scores)-1 STEP 1
    IF test_scores[i] > 90 THEN
        DISPLAY test_scores[i]
    ENDIF
NEXT i
```
{% endcode %}

In the above pseudocode, because the for / next loop is **INCLUSIVE** of the end range value, we need to take away one from the length for the end of the range.

Otherwise, let's say the array has 5 test values - if we used the full length of test scores, the loop would run **6 times (0-5),** so we need to take away one from the length so that it becomes **0-4.**&#x20;

***

### 2025 HSC Question

To give you another example, here's a pseudocode algorithm for an array from 2025 HSC Exam:

#### Question

An algorithm is required by a school to rate the risk of a location for school excursions.

A teacher completes a 10-question survey to assess potential hazards for the location. Each question is given a score from 1 (low) to 5 (high), and the scores are stored in a 10-element integer array called _Risks_.

The scores for each question are added to give a total risk score.

The excursion risk is rated as:

* Low (total less than 20)
* Medium (total between 20 – 35)
* High (total above 35).

**Using pseudocode, with a repeat-until loop, write an algorithm to determine the excursion risk rating for a location. You can assume that the scores for the 10 questions are already stored in.**

#### **Answer**

<div align="left"><figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure></div>

