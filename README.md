# python-task-today
# Python Assignments

This repository contains 10 beginner-level Python assignments covering loops, recursion, lambda functions, lists, strings, dictionaries, sets, and the math library.

---

## 1. Print All Prime Numbers Between Input Range

### Problem

Print all prime numbers between the given starting and ending range.

### Code

```python
start = int(input("Enter start range: "))
end = int(input("Enter end range: "))

print("Prime numbers:")

for num in range(start, end + 1):

    if num < 2:
        continue

    prime = True

    for i in range(2, num):
        if num % i == 0:
            prime = False
            break

    if prime:
        print(num, end=" ")
```

<img width="327" height="173" alt="image" src="https://github.com/user-attachments/assets/4937f3d4-9803-4755-9e96-130691144736" />


### Concepts Used

* `for` loop
* Nested loop
* `if-else`
* Modulus operator `%`
* Boolean variable

---

# 2. Factorial Using Recursion

### Problem

Calculate the factorial of a number using recursion.

### Code

```python
def factorial(n):

    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)


n = int(input("Enter a number: "))

print("Factorial:", factorial(n))
```

<img width="302" height="62" alt="image" src="https://github.com/user-attachments/assets/39a49f78-ac89-4775-a311-d89eda7ad961" />


### Logic

```text
factorial(5)
= 5 × factorial(4)
= 5 × 4 × factorial(3)
= 5 × 4 × 3 × factorial(2)
= 5 × 4 × 3 × 2 × factorial(1)
= 120
```

### Concepts Used

* Function
* Recursion
* Base condition
* Return statement

---

# 3. Square of Numbers Using Lambda

### Problem

Find the square of a number using a lambda function.

### Code

```python
square = lambda x: x * x

n = int(input("Enter a number: "))

print("Square:", square(n))
```

<img width="257" height="65" alt="image" src="https://github.com/user-attachments/assets/0d8dde20-81f0-4f63-b28d-53c2d257d1c6" />


### Concepts Used

* Lambda function
* Function call
* Multiplication

---

# 4. Find the Second Largest Element in a List

### Problem

Find the second-largest distinct element in a list.

### Code

```python
numbers = [10, 20, 20, 30, 40, 40, 50]

unique_numbers = list(set(numbers))

unique_numbers.sort()

print("Second largest:", unique_numbers[-2])
```

<img width="296" height="40" alt="image" src="https://github.com/user-attachments/assets/70bb98fd-875f-4d56-855f-d0979eae0f45" />


### Logic

```text
list
  ↓
set()
  ↓
remove duplicates
  ↓
list()
  ↓
sort()
  ↓
[-2]
  ↓
second largest
```

### Concepts Used

* List
* Set
* Type conversion
* Sorting
* Negative indexing

---

# 5. Count Frequency of Characters in a String

### Problem

Count how many times each character appears in a string.

### Code

```python
text = input("Enter a string: ")

frequency = {}

for char in text:

    if char in frequency:
        frequency[char] += 1
    else:
        frequency[char] = 1

print("Character frequency:")

for char, count in frequency.items():
    print(char, ":", count)
```
<img width="511" height="60" alt="image" src="https://github.com/user-attachments/assets/56c31bd0-51e7-402b-a980-42a10286e3c9" />


### Logic

For every character:

```text
Is the character already in the dictionary?

YES → increase its count by 1

NO → create the character with count 1
```

### Concepts Used

* String
* Dictionary
* `for` loop
* `if-else`
* Dictionary methods

---

# 6. Calculate Area of a Circle Using Math Library

### Problem

Calculate the area of a circle using Python's `math` library.

### Code

```python
import math

radius = float(input("Enter radius: "))

area = math.pi * radius ** 2

print("Area of circle:", area)
```
<img width="427" height="52" alt="image" src="https://github.com/user-attachments/assets/f52dd50a-8294-4679-b9ba-955fcd2abcb6" />


### Formula

```text
Area = π × r²
```

### Concepts Used

* `math` library
* `math.pi`
* User input
* Exponent operator `**`

---

# 7. Reverse a String Without Using Built-in Reverse

### Problem

Reverse a string without using `reverse()` or slicing.

### Code

```python
text = input("Enter a string: ")

reverse = ""

for i in range(len(text) - 1, -1, -1):
    reverse += text[i]

print("Reversed string:", reverse)
```
<img width="352" height="42" alt="image" src="https://github.com/user-attachments/assets/ce4b2403-9d78-4a66-98ab-2053e408ebe0" />


### Logic

For the string:

```text
hello
```

Indexes:

```text
h   e   l   l   o
0   1   2   3   4
```

Start from index `4` and move backwards:

```text
4 → o
3 → l
2 → l
1 → e
0 → h
```

Result:

```text
olleh
```

### Concepts Used

* String indexing
* `len()`
* `range()`
* Reverse traversal
* String concatenation

---

# 8. Remove Duplicates from a List

### Problem

Remove duplicate elements from a list.

### Code

```python
numbers = [10, 20, 20, 30, 40, 40, 50]

result = []

for num in numbers:

    if num not in result:
        result.append(num)

print("Original list:", numbers)
print("List without duplicates:", result)
```

<img width="273" height="31" alt="image" src="https://github.com/user-attachments/assets/9956360d-15ed-4d35-8dc3-65e2f5b0832f" />


### Logic

```text
10 → not present → add
20 → not present → add
20 → already present → skip
30 → not present → add
40 → not present → add
40 → already present → skip
50 → not present → add
```

### Concepts Used

* List
* `not in`
* `append()`
* Loop
* Conditional statement

---

# 9. Merge Two Dictionaries

### Problem

Merge two dictionaries into a single dictionary.

### Code

```python
dict1 = {
    "name": "Deva",
    "age": 21
}

dict2 = {
    "course": "AI & ML",
    "college": "Saveetha Engineering College"
}

merged = dict1.copy()

for key, value in dict2.items():
    merged[key] = value

print("Merged dictionary:")
print(merged)
```

<img width="377" height="35" alt="image" src="https://github.com/user-attachments/assets/e013fd9a-02ff-4401-951c-33f0d6bbff39" />


### Logic

First copy `dict1`:

```python
merged = dict1.copy()
```

Then take each key-value pair from `dict2`:

```python
for key, value in dict2.items():
```

and add it to `merged`:

```python
merged[key] = value
```

### Concepts Used

* Dictionary
* `copy()`
* `items()`
* Key-value pairs
* Loop

---

# 10. Fibonacci Series Using Recursion

### Problem

Generate the Fibonacci series using recursion.

### Code

```python
def fibonacci(n):

    if n == 0:
        return 0

    if n == 1:
        return 1

    return fibonacci(n - 1) + fibonacci(n - 2)


n = int(input("Enter number of terms: "))

print("Fibonacci series:")

for i in range(n):
    print(fibonacci(i), end=" ")
```

<img width="406" height="52" alt="image" src="https://github.com/user-attachments/assets/9ebf7d13-9fe3-4923-aea0-a2a7d39a7749" />


### Logic

The Fibonacci rule is:

```text
F(0) = 0
F(1) = 1

F(n) = F(n-1) + F(n-2)
```

For example:

```text
F(2) = F(1) + F(0)
     = 1 + 0
     = 1

F(3) = F(2) + F(1)
     = 1 + 1
     = 2

F(4) = F(3) + F(2)
     = 2 + 1
     = 3
```

So the series becomes:

```text
0 1 1 2 3 5 8 13 ...
```

### Concepts Used

* Function
* Recursion
* Base condition
* `for` loop
* Return statement

---

# Concepts Covered

| No. | Assignment          | Main Concept          |
| --- | ------------------- | --------------------- |
| 1   | Prime Numbers       | Loops and Conditions  |
| 2   | Factorial           | Recursion             |
| 3   | Square              | Lambda                |
| 4   | Second Largest      | List, Set and Sorting |
| 5   | Character Frequency | Dictionary            |
| 6   | Circle Area         | Math Library          |
| 7   | Reverse String      | String Indexing       |
| 8   | Remove Duplicates   | List and Membership   |
| 9   | Merge Dictionaries  | Dictionary Traversal  |
| 10  | Fibonacci           | Recursion             |

---

# How to Run

Clone or download this repository and run the required Python file.

```bash
python filename.py
```

Example:

```bash
python 01_prime_numbers.py
```

---

# Learning Objective

These assignments are designed to strengthen fundamental Python programming skills, problem-solving ability, logical thinking, and understanding of basic data structures and programming techniques.
