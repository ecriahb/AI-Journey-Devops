# Python Lesson 03 — 21-02-26

## 1. Lesson Overview

This session is a beginner-friendly introduction to Python for the AI/ML journey. The instructor focuses on getting the environment ready, understanding basic Python syntax, writing simple code in Jupyter Notebook, handling common errors, variables and data types, conditional/loop statements, and Python lists.

> **Source:** Prepared from the provided lesson transcript. The instructor's explanations are treated as the primary source.

---

## 2. What the Instructor Covered

### Environment and Jupyter Notebook
- Install **Anaconda** / Python as per the training installation instructions.
- Open **Anaconda Navigator**.
- Launch **Jupyter Notebook**.
- In Jupyter, use **File → New → Notebook** to create a Python notebook.
- Jupyter cells can be used for Markdown or executable Python code.
- The instructor also explained that the cell execution number shows the order in which cells were run.
- If a cell keeps running, a `*` can appear; the instructor suggested restarting the kernel when required.

### Why Python?
The instructor highlighted Python because it is:
- Easy to learn and understand.
- Versatile.
- Widely used in AI/data science.
- Supported by a large community, libraries and frameworks.

### Python Basics
- Syntax and semantics.
- Comments.
- Variables and assignment.
- Basic data types.
- Dynamic typing / type inference.
- `print()` and `type()`.
- Conditional statements.
- `for` loop.
- Lists.
- List indexing and negative indexing.
- Modifying list elements.
- List methods: `append()`, `remove()`, `sort()`.
- List slicing, including `start:stop:step` and reverse slicing.

---

# 3. Jupyter Notebook Basics

Jupyter provides different cell types. The instructor used **Markdown** for headings/explanations and **Code** cells for Python.

### Markdown
A Markdown cell is useful for documentation and headings.

Examples discussed:
```text
# Python Basics
## Variables
### Lists
```

More `#` symbols create smaller heading levels.

### Code Cell
A Code cell is used to execute Python statements.

### Markdown vs Python Comment
- Markdown is used to document the notebook in a readable way.
- A Python single-line comment starts with `#` inside a Python code cell.

---

# 4. Comments

## Single-Line Comment
A single-line comment starts with `#`.

```python
# This is a comment
2 + 2  # addition
```

Python ignores the comment part during execution.

## Multi-Line Comment / Documentation Style
The instructor demonstrated triple quotes for writing multiple lines of text/comment-like content:

```python
"""
This is a multiline block.
It can contain multiple lines.
"""
```

The session mainly used this to demonstrate multiline text/commenting in the notebook.

---

# 5. Syntax and Semantics

## Syntax
The instructor explained syntax as the set of rules that defines which combinations of symbols are correctly structured in a programming language.

Example:
```python
if age > 18:
    print("Adult")
```

The colon and indentation are part of the required Python structure here.

## Semantics
Semantics refers to the **meaning** of a statement or expression.

Example from the session:
```python
x = 5
y = 10
z = x + y
```

Meaning:
- `x` stores `5`.
- `y` stores `10`.
- `z` stores the result of `x + y`, i.e. `15`.

**Easy way to remember:**
- Syntax = Is the code written correctly?
- Semantics = What does the correctly written code mean/do?

---

# 6. Indentation

Indentation is very important in Python because it defines the block of code belonging to a statement such as `if` or `for`.

Example:
```python
if True:
    print("This is inside the condition")
```

The instructor demonstrated that removing the indentation changes the relationship between statements.

Python commonly uses **4 spaces** for indentation.

---

# 7. Common Errors Discussed

The instructor specifically discussed three common errors:

### 1. Indentation Error
Occurs when indentation does not match the expected code block.

### 2. Syntax Error
Occurs when the code does not follow Python's syntax rules.

Example discussed: forgetting the colon after a condition.

```python
if age > 18
    print("Adult")
```

### 3. Name Error
Occurs when Python cannot find a defined name/variable.

```python
print(A)
```

If `A` has not been defined, Python raises a `NameError`.

### Error-reading tip
The instructor emphasized looking at the last/error message line because it helps identify what went wrong.

---

# 8. `print()` Function

The instructor introduced `print()` as a basic built-in function.

```python
print("Welcome to Python")
```

Output:
```text
Welcome to Python
```

Important point:
- Functions are followed by parentheses `()`.
- Text is written inside quotes.

The instructor also noted that using `print()` often gives a cleaner, more readable output in the notebook.

---

# 9. Strings

Text values are written inside quotes.

Examples:
```python
name = "Alex"
fruit = 'Apple'
```

The instructor discussed single and double quotes and noted that the choice can matter when the text itself contains quote characters.

---

# 10. Variables and Assignment

A variable is used to store a value.

Example:
```python
my_variable = 10
```

The instructor explained the assignment concept as:

**Right-hand side → value being assigned**

**Left-hand side → variable receiving the value**

Example:
```python
x = 5
y = 10
z = x + y
```

`z` becomes `15`.

### Case Sensitivity
Python is case-sensitive.

```python
my_variable = 10
```

and

```python
My_Variable
```

are different names.

---

# 11. Basic Data Types

The instructor demonstrated these basic values:

| Example | Type |
|---|---|
| `5` | Integer (`int`) |
| `3.14` | Floating-point (`float`) |
| `"Alex"` | String (`str`) |

Use `type()` to check a value's type:

```python
a = 5
b = 3.14
c = "Alex"

print(type(a))
print(type(b))
print(type(c))
```

---

# 12. Dynamic Typing / Type Inference

The instructor explained that Python is dynamically typed and automatically infers the type from the assigned value.

Example:
```python
x = 10
x = "Hello"
```

The variable does not require an explicit type declaration in these examples.

**Key idea:** Python determines the value's type from what is assigned.

---

# 13. Conditional Statements

The instructor introduced `if` as a conditional statement, similar to rule-based decision making.

Example:
```python
age = 30

if age >= 18:
    print("Adult")
```

Important syntax:
- Condition is followed by `:`.
- The code inside the condition is indented.

The instructor also used `True`/`False` examples to demonstrate how the condition controls execution.

---

# 14. `for` Loop

A `for` loop can iterate through the values of a list.

Example based on the instructor's demonstration:

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Output:
```text
apple
banana
cherry
```

Conceptually:
1. First iteration: `fruit = "apple"`
2. Second iteration: `fruit = "banana"`
3. Third iteration: `fruit = "cherry"`

The instructor highlighted that the loop automatically goes through the list one value at a time.

---

# 15. Lists

The instructor described a list as a Python collection of items that can contain different types of values.

Lists are **mutable**, meaning their contents can be changed after creation.

### Creating a List

```python
fruits = ["apple", "banana", "cherry"]
```

Square brackets `[]` are used to create a list, and values are separated by commas.

---

# 16. List Indexing

Python uses **zero-based indexing**.

For:
```python
fruits = ["apple", "banana", "cherry"]
```

Indexes are:

| Value | Index |
|---|---:|
| apple | 0 |
| banana | 1 |
| cherry | 2 |

Access an element using square brackets:

```python
print(fruits[0])
print(fruits[1])
print(fruits[2])
```

---

# 17. Negative Indexing

Python can also access list elements from right to left using negative indexes.

For:
```python
fruits = ["apple", "banana", "cherry"]
```

| Value | Negative Index |
|---|---:|
| cherry | -1 |
| banana | -2 |
| apple | -3 |

Example:
```python
print(fruits[-1])
```

This accesses the last item.

---

# 18. Modifying List Elements

Because lists are mutable, an element can be replaced by assigning a new value to its index.

Example:
```python
fruits = ["apple", "banana", "cherry"]
fruits[0] = "blueberry"

print(fruits)
```

The first element is replaced.

The instructor also asked learners to practice changing another element such as `cherry`.

---

# 19. List Methods

The instructor introduced built-in methods for manipulating lists.

## `append()`
Adds an item to the end of the list.

```python
fruits.append("orange")
```

## `remove()`
Removes the first occurrence of the specified item.

```python
fruits.remove("blueberry")
```

## `sort()`
Sorts the list. The instructor demonstrated default ascending order and reverse sorting.

```python
fruits.sort()
```

Reverse order:
```python
fruits.sort(reverse=True)
```

### Function vs Method — Instructor's Explanation
- A function is called directly, such as `print(...)`.
- A method is associated with an object/data, such as `fruits.append(...)`.

---

# 20. List Slicing

Slicing is used when you want a **portion of a list**, rather than one individual element.

General form discussed:

```python
list[start:stop:step]
```

### Important Rule
The `stop` index is **not included**.

Example:
```python
fruits[0:2]
```

This returns indexes `0` and `1`.

### Leaving Start or Stop Blank

```python
fruits[:2]
```

Means start from the beginning and stop before index `2`.

```python
fruits[1:]
```

Means start from index `1` and continue to the end.

### Step
The third part controls the jump/step.

```python
numbers[start:stop:step]
```

The instructor demonstrated negative steps for moving from right to left.

Example concept:
```python
numbers[4:1:-1]
```

This starts at index `4`, moves backward, and does not include index `1`.

### Reverse a List with Slicing
A negative step can be used to traverse a list in reverse direction.

```python
numbers[::-1]
```

The session mainly focused on understanding the relationship between **start, stop and step** and why a negative step is required when moving backward.

---

# 21. Data Structures Mentioned

The instructor introduced the idea of Python data structures and said the session would explore **lists** and another structure referred to in the transcript as "two" (likely the instructor's pronunciation/transcription of tuple).

However, the provided transcript primarily contains the detailed explanation of **lists, list methods and list slicing**. A detailed tuple explanation is not supported by this transcript, so it is intentionally not added here as instructor-covered content.

The instructor also mentioned **list comprehension**, but the provided transcript does not contain a complete explanation or practical demonstration of it. It should therefore be studied in a later lesson rather than assumed to be covered here.

---

# 22. Practical Examples — Consolidated

## Variables
```python
name = "Alex"
age = 30
salary = 50000.50

print(name)
print(age)
print(salary)
```

## Type Checking
```python
print(type(age))
print(type(salary))
print(type(name))
```

## Condition
```python
if age >= 18:
    print("Adult")
```

## List + Loop
```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

## Modify
```python
fruits[0] = "blueberry"
```

## Append
```python
fruits.append("orange")
```

## Remove
```python
fruits.remove("blueberry")
```

## Sort
```python
fruits.sort()
fruits.sort(reverse=True)
```

## Slice
```python
print(fruits[0:2])
print(fruits[1:])
print(fruits[:2])
```

---

# 23. What You MUST Know ⭐

1. How to create and run a Python notebook in Jupyter.
2. Difference between Markdown and Code cells.
3. Python comments using `#`.
4. Meaning of syntax vs semantics.
5. Importance of indentation.
6. Common errors: `IndentationError`, `SyntaxError`, `NameError`.
7. Variables and assignment: `left = right`.
8. Python is case-sensitive.
9. Basic types: `int`, `float`, `str`.
10. `type()` and `print()`.
11. Python's dynamic typing/type inference concept.
12. Basic `if` statement.
13. Basic `for` loop.
14. Lists and their mutability.
15. Zero-based indexing.
16. Negative indexing.
17. Modifying list elements.
18. `append()`, `remove()`, `sort()`.
19. Slicing: `start:stop:step`.
20. The stop index is excluded in slicing.

---

# 24. What You Can Keep Light

For this lesson, do not over-focus on:
- Python history details.
- Advanced Jupyter features.
- Advanced slicing tricks.
- Tuple internals — it was only mentioned, not properly explained in the supplied transcript.
- List comprehension — mentioned, but not fully taught in the supplied transcript.

First become comfortable with variables, conditions, loops, lists, indexing and slicing.

---

# 25. DevOps / MLOps Connection

This lesson is foundational for the later MLOps/AI work.

### Python + DevOps
Python can be used for:
- Automation scripts.
- API interaction.
- Cloud automation.
- Kubernetes/Azure operational tooling.
- Log processing.
- CI/CD helper scripts.

### Python + MLOps
The same fundamentals become useful for:
- Data preprocessing.
- ML training scripts.
- Model evaluation.
- Pipeline orchestration.
- Experiment automation.
- Model deployment and monitoring.

The important takeaway is not to learn Python as a separate programming language only; build enough Python fluency to automate and work with AI/ML systems.

---

# 26. Interview Questions

### Q1. Why is Python widely used in AI/ML?
**Answer:** The instructor highlighted its ease of learning, versatility, large community, and availability of libraries/frameworks.

### Q2. What is the difference between syntax and semantics?
**Answer:** Syntax is the set of rules for correctly structuring code. Semantics is the meaning/behavior of that code.

### Q3. Why is indentation important in Python?
**Answer:** Python uses indentation to define code blocks, such as the body of an `if` statement or loop.

### Q4. What are three common errors discussed in the session?
**Answer:** `IndentationError`, `SyntaxError`, and `NameError`.

### Q5. What does zero-based indexing mean?
**Answer:** The first list element is at index `0`, not `1`.

### Q6. What is negative indexing?
**Answer:** It accesses elements from the end of a sequence; `-1` represents the last element.

### Q7. What does it mean that a list is mutable?
**Answer:** List contents can be changed after the list is created.

### Q8. Difference between `append()` and `remove()`?
**Answer:** `append()` adds an item to the end; `remove()` removes the first occurrence of a specified item.

### Q9. What is list slicing?
**Answer:** Extracting a portion of a list using `start:stop:step`.

### Q10. Is the stop index included in Python slicing?
**Answer:** No. The stop index is excluded.

---

# 27. Additional Clarification

These points are general clarifications to make the transcript easier to study; they are **not presented as additional instructor-covered material**.

- `print()` is a built-in Python function.
- `append()`, `remove()` and `sort()` are list methods.
- A Python list can contain mixed data types, although keeping related data together is usually clearer.
- In real projects, use consistent indentation and preferably spaces rather than mixing tabs/spaces.

---

# 28. Lesson Takeaway

The session establishes the basic Python foundation required for the upcoming AI/ML lessons:

**Jupyter → Syntax → Variables → Data Types → Conditions → Loops → Lists → Indexing → Methods → Slicing**

The instructor ended by emphasizing **regular practice**, even if only a small amount, because Python concepts are easy to forget without hands-on repetition.
