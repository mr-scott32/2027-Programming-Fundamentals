---
icon: book-open
---

# Data Types

### What Are Data Types?

A **data type** defines the kind of information that can be stored in a variable and the operations that can be performed on it. Programming languages use different data types to represent information such as text, numbers, dates and logical values.

Choosing the correct data type is important because it determines how data is stored, processed and manipulated. For example, a person's age should be stored as an integer, while their name should be stored as a string.

Different programming languages support different data types. Some languages require programmers to declare the data type of a variable before using it. However, **Python automatically determines the data type based on the value assigned to a variable**.

For example:

```
name = "Alex"
age = 16
height = 1.75
is_student = True
```

Python automatically recognises that `name` is a string, `age` is an integer, `height` is a floating-point number and `is_student` is a Boolean.

***

### Character (Char) and String

A **character (char)** is a data type used to represent a single character, such as a letter, number, punctuation mark or symbol. For example, `'A'`, `'7'` and `'!'` are all characters.

A **string** is a sequence of characters used to represent text. Strings can contain letters, numbers, spaces and special characters. For example, `"Hello World"` and `"Student123"` are strings.

The main difference is that a character stores a single character, while a string can store multiple characters.

#### Characters and Strings in Python

Python does not have a separate `char` data type. Instead, individual characters and sequences of characters are both represented using the **`str` data type**.

```
grade = "A"
student_name = "Alexander"
student_id = "S12345"
```

In this example, all three variables are strings, even though `grade` contains only one character.

Python also allows programmers to access individual characters within a string using **indexing**.

```
name = "Alexander"

print(name[0])  # Output: A
print(name[2])  # Output: e
```

Python starts counting character positions from `0`, meaning the first character is at index `0`.

Although strings can contain numbers, those numbers are treated as text rather than numerical values.

```
number = "25"
```

The value `"25"` is a string, not an integer, because it is enclosed in quotation marks.

***

### Boolean

A **Boolean** is a data type that represents one of two possible logical values: **True or False**.

Boolean values are commonly used when a program needs to make decisions, check conditions or control repetition. For example, a program might use a Boolean to determine whether a user is logged in, whether a game has ended or whether a password is correct.

#### Booleans in Python

Python uses the **`bool` data type** to represent Boolean values.

```
is_logged_in = True
game_over = False
```

Boolean values can also be produced by comparisons.

```
age = 17

can_drive = age >= 17

print(can_drive)  # Output: True
```

In this example, Python evaluates the expression `age >= 17`. Because the condition is satisfied, the variable `can_drive` stores `True`.

**Important:** Python requires Boolean values to begin with a capital letter (`True` and `False`). Unlike strings, Boolean values are not enclosed in quotation marks.

***

### Real

A **real number** is a number that can contain a fractional or decimal component. Real numbers include values such as `3.14`, `-12.75` and `0.5`.

In mathematics, real numbers include both rational and irrational numbers. However, computers cannot represent every possible real number exactly because they have limited memory.

Programming languages therefore typically represent real numbers using **floating-point data types**, which store approximations of numerical values.

Real numbers are commonly used for measurements, scientific calculations, averages and other situations where whole numbers are insufficient.

#### Real Numbers in Python

Python does not have a separate built-in data type called `real`. Instead, it typically uses the **`float` data type**.

```
temperature = 23.5
average_mark = 78.25
distance = 12.75
```

Python recognises these values as floating-point numbers.

Floating-point numbers can sometimes produce small rounding errors because many decimal values cannot be represented exactly in binary.

```
result = 0.1 + 0.2

print(result)  # Output: 0.30000000000000004
```

This is a limitation of floating-point representation rather than an error in Python's calculations.

### Single Precision Floating Point

A **single precision floating-point number** is a specific method of representing real numbers using **32 bits (4 bytes)** of memory.

Floating-point numbers are stored using three components:

* **Sign:** Determines whether the number is positive or negative.
* **Exponent:** Determines the scale or magnitude of the number.
* **Significand (mantissa):** Stores the significant digits of the number.

Single precision floating-point numbers generally provide approximately **6–9 significant decimal digits** of precision.

For example, the number `3.14159265` may be stored approximately as `3.1415927` using single precision.

Single precision is useful when memory efficiency is important, particularly in graphics processing, simulations and applications that process large amounts of numerical data.

#### Single Precision in Python

Python's built-in **`float` data type normally uses double precision (64 bits)** rather than single precision.

Double precision provides approximately 15–17 significant decimal digits, allowing numbers to be represented with greater accuracy.

Python does not provide a separate built-in single precision numeric type for ordinary calculations. However, specialised libraries such as NumPy support 32-bit floating-point numbers.

For example:

```
import numpy as np

number = np.float32(3.14159265)

print(number)
```

This creates a single precision floating-point value.

**Key difference:** Both real numbers and single precision floating-point numbers represent values with decimal components. However, _real_ describes a general category of numbers, while _single precision_ describes a specific computer representation with a defined amount of memory and precision.

***

### Integer

An **integer** is a data type used to represent whole numbers without a fractional or decimal component.

Integers can be positive, negative or zero. Examples include `25`, `-10` and `0`.

Integers are commonly used for counting, indexing, storing quantities and representing values that cannot contain fractions, such as the number of students in a classroom.

#### Integers in Python

Python uses the **`int` data type** to represent integers.

```
student_age = 16
score = 250
lives_remaining = 3
```

Integers can be used in mathematical operations.

```
score = 100

score = score + 50

print(score)  # Output: 150
```

Unlike many programming languages that use fixed-size integers, Python integers can grow to accommodate very large numbers, provided sufficient memory is available.

It is important to distinguish between integers and floating-point numbers.

```
number1 = 10
number2 = 10.0
```

Although both variables represent the same numerical value, `number1` is an integer (`int`), while `number2` is a floating-point number (`float`).

***

### Date and Time

**Date and time data types** are used to represent calendar dates, times of day or combinations of both.

These data types allow programs to store and manipulate information such as birthdays, appointment times, deadlines and timestamps.

Dates generally contain a year, month and day, while times contain hours, minutes, seconds and sometimes smaller units.

Unlike ordinary strings, specialised date and time data types allow programmers to perform calculations, such as determining the number of days between two dates.

#### Date and Time in Python

Python does not have built-in date and time data types in the same way it has `int`, `str` and `bool`. Instead, Python provides a standard library module called **`datetime`**.

This module includes several useful data types:

* `date` — Represents a calendar date.
* `time` — Represents a time of day.
* `datetime` — Represents both a date and a time.
* `timedelta` — Represents a duration or difference between dates or times.

For example:

```
from datetime import date, time, datetime

birthday = date(2010, 5, 15)

lesson_start = time(9, 30)

appointment = datetime(2026, 10, 20, 14, 45)

print(birthday)       # Output: 2010-05-15
print(lesson_start)   # Output: 09:30:00
print(appointment)    # Output: 2026-10-20 14:45:00
```

Python can also calculate the difference between two dates.

```
from datetime import date

start_date = date(2026, 10, 1)
end_date = date(2026, 10, 15)

difference = end_date - start_date

print(difference.days)  # Output: 14
```

This makes date and time data types more useful than simply storing dates as strings.

For example, `"15/10/2026"` is a string, while `date(2026, 10, 15)` creates an actual date object that Python can use in date calculations.

***

### Summary of Standard Data Types

The following table compares standard programming data types with their Python equivalents.

| Standard Data Type                  | Description                                                           | Python Equivalent                                    | Example in Python                |
| ----------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------- | -------------------------------- |
| **Char (Character)**                | Stores a single character, such as a letter, digit or symbol.         | `str`                                                | `grade = "A"`                    |
| **String**                          | Stores a sequence of characters representing text.                    | `str`                                                | `name = "Alex"`                  |
| **Boolean**                         | Stores one of two logical values: True or False.                      | `bool`                                               | `is_active = True`               |
| **Real**                            | Represents numbers that may contain decimal or fractional components. | `float`                                              | `temperature = 23.5`             |
| **Single Precision Floating Point** | Represents approximate real numbers using 32 bits of memory.          | No built-in equivalent; `numpy.float32` can be used. | `np.float32(3.14)`               |
| **Integer**                         | Stores positive or negative whole numbers, including zero.            | `int`                                                | `score = 100`                    |
| **Date**                            | Stores a calendar date, including the day, month and year.            | `datetime.date`                                      | `date(2026, 10, 15)`             |
| **Time**                            | Stores a time of day, including hours, minutes and seconds.           | `datetime.time`                                      | `time(14, 30)`                   |
| **Date and Time**                   | Stores a combination of a calendar date and time.                     | `datetime.datetime`                                  | `datetime(2026, 10, 15, 14, 30)` |
