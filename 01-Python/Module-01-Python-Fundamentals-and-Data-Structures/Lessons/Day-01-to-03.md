# Python Fundamentals — Day 01 to Day 03

> Detailed revision notes based on the Python revision material already prepared from the course. These notes are intentionally practical and DevOps-oriented.

## Day 01 — `print()`, Variables and Data Types

### 1. `print()`
`print()` displays output on the screen.

```python
print("Hello Brijesh")
print("I am learning Python")
print("My goal is Agentic AI")
```

### 2. Variables
A variable is a named place used to store a value.

```python
name = "Brijesh Chauhan"
experience = 10
is_learning = True
```

Think of it as:

```text
variable name → stored value
name          → "Brijesh Chauhan"
experience    → 10
is_learning   → True
```

`=` assigns a value; it is not an equality comparison.

### 3. Basic data types

| Type | Meaning | Example |
|---|---|---|
| `str` | Text | `"Brijesh"` |
| `int` | Whole number | `10` |
| `float` | Decimal number | `28.5` |
| `bool` | True/False | `True` |

Use `type()` to inspect a value's type.

```python
name = "Brijesh"
experience = 10
salary = 28.5
is_learning = True

print(type(name))
print(type(experience))
print(type(salary))
print(type(is_learning))
```

### 4. String vs number

```python
number_text = "10"
number_value = 10

print(number_text + number_text)  # 1010
print(number_value + number_value)  # 20
```

A string contains text. An integer is numeric data, so operators can behave differently.

### 5. Variable access

```python
name = "Brijesh"
print(name)       # Brijesh
print("name")     # name
```

Quotes mean literal text; without quotes Python looks for the variable.

### 6. Top-to-bottom execution
Python executes statements in order.

```python
name = "Brijesh"
role = "DevOps Engineer"
print(name)
print(role)
```

A variable must be defined before it is used:

```python
print(server_name)
server_name = "production-server-01"
```

This produces `NameError` because `server_name` has not been defined yet.

### 7. Comments
Comments start with `#` and are not executed.

```python
# Threshold for CPU usage
cpu_threshold = 80  # inline comment
```

### 8. Variable naming rules

- Start with a letter or underscore.
- Do not use spaces.
- Do not use hyphens.
- Avoid Python keywords.
- Names are case-sensitive.
- Prefer meaningful names.
- `snake_case` is the recommended variable style.

```python
cpu_threshold = 80
memory_usage = 92.5
```

Avoid unclear names such as `x` or `a` when a meaningful name is possible.

### 9. f-strings
An f-string inserts variable values into readable text.

```python
name = "Brijesh"
experience = 10
print(f"My name is {name}")
print(f"I have {experience} years of experience")
```

Pattern:

```python
f"Normal text {variable}"
```

### Day 01 checkpoint
You should be able to explain and use:

- `print()`
- variables
- `str`, `int`, `float`, `bool`
- `type()`
- comments
- variable naming
- f-strings

---

## Day 02 — `input()` and Type Conversion

### 1. `input()`
`input()` makes a program interactive by accepting user input.

Important rule: **`input()` returns a string.**

```python
age = input("Enter your age: ")
print(type(age))  # <class 'str'>
```

Even if the user enters `34`, the returned value is initially text.

### 2. Type conversion

| Function | Converts to | Example |
|---|---|---|
| `int()` | Whole number | `int("34")` → `34` |
| `float()` | Decimal number | `float("28.5")` → `28.5` |
| `str()` | String | `str(34)` → `"34"` |

Examples:

```python
age = int(input("Enter your age: "))
height = float(input("Enter your height: "))
```

### 3. Complete input flow

```python
monthly_salary = float(input("Enter your monthly salary: "))
```

Flow:

```text
Prompt
  ↓
User enters text
  ↓
input() returns str
  ↓
float() converts it
  ↓
monthly_salary stores numeric value
```

### 4. String addition vs numeric addition

```python
number1 = input("Enter first number: ")
number2 = input("Enter second number: ")
print(number1 + number2)
```

If inputs are `10` and `20`, result is `1020` because both are strings.

Correct numeric version:

```python
number1 = float(input("Enter first number: "))
number2 = float(input("Enter second number: "))
print(number1 + number2)  # 30.0
```

### 5. Invalid conversion
Conversion requires valid numeric text.

```text
int("25")       → 25
float("25.5")   → 25.5
float("25")     → 25.0
int("25.5")     → ValueError
float("twenty") → ValueError
```

Graceful invalid-input handling with `try/except` is intentionally covered later; at this stage focus on understanding the conversion itself.

### 6. Salary calculator

```python
name = input("Enter your name: ")
monthly_salary = float(input("Enter your monthly salary: "))
annual_bonus = float(input("Enter your annual bonus: "))

annual_salary = monthly_salary * 12
total_annual_income = annual_salary + annual_bonus

print("\n===== SALARY SUMMARY =====")
print(f"My name is: {name}")
print(f"My monthly salary is: Rs. {monthly_salary:,.2f}")
print(f"My annual bonus is: Rs. {annual_bonus:,.2f}")
print(f"My annual salary is: Rs. {annual_salary:,.2f}")
print(f"My total income is: Rs. {total_annual_income:,.2f}")
```

Formulas:

```text
Annual salary = monthly salary × 12
Total income  = annual salary + annual bonus
```

### 7. Number formatting: `:,.2f`

```python
monthly_salary = 125000.567
print(f"Rs. {monthly_salary:,.2f}")
```

Output:

```text
Rs. 125,000.57
```

Meaning:

```text
,   → thousands separator
.2f → two decimal places
```

### Day 02 checkpoint
You should be able to explain:

- why `input()` returns `str`
- when to use `int()` vs `float()`
- why `"10" + "20"` becomes `1020`
- salary calculation flow
- `:,.2f` formatting

---

## Day 03 — Arithmetic, Comparison and Logical Operators

### 1. Arithmetic operators

| Operator | Meaning | Example | Result |
|---|---|---|---:|
| `+` | Addition | `10 + 3` | `13` |
| `-` | Subtraction | `10 - 3` | `7` |
| `*` | Multiplication | `10 * 3` | `30` |
| `/` | Normal division | `10 / 3` | `3.333...` |
| `//` | Floor division | `10 // 3` | `3` |
| `%` | Remainder | `10 % 3` | `1` |
| `**` | Power | `10 ** 3` | `1000` |

### 2. `/` vs `//` vs `%`

```text
10 / 3  → 3.333...
10 // 3 → 3
10 % 3  → 1
```

The `%` operator gives the remainder.

### 3. Practical `%` usage
Even/odd check:

```python
number = int(input("Enter a number: "))
is_even = number % 2 == 0
print(f"Is the number even? {is_even}")
```

Batch grouping:

```python
total_servers = 17
servers_per_batch = 5

full_batches = total_servers // servers_per_batch
remaining_servers = total_servers % servers_per_batch
```

Result: 3 full batches and 2 remaining servers.

### 4. Operator precedence

```python
result = 10 + 5 * 2       # 20
result_with_brackets = (10 + 5) * 2  # 30
```

Order covered:

```text
() 
**
* / // %
+ -
```

When intent is not obvious, use parentheses for readability.

### 5. Comparison operators
Comparison expressions return a Boolean: `True` or `False`.

```text
>   greater than
<   less than
>=  greater than or equal
<=  less than or equal
==  equal to
!=  not equal
```

### 6. `=` vs `==`

```python
cpu_usage = 80     # assignment
cpu_usage == 80    # comparison
```

`=` stores a value. `==` checks equality.

### 7. Inclusive thresholds
For a requirement such as “CPU usage of 80 or more is high”:

```python
is_cpu_high = cpu_usage >= 80
```

Boundary testing:

```text
79.9 >= 80 → False
80.0 >= 80 → True
80.1 >= 80 → True
```

This is an important engineering habit: test just below, exactly at, and just above a threshold.

### 8. Logical operators

| Operator | Meaning |
|---|---|
| `and` | all required conditions must be True |
| `or` | at least one condition must be True |
| `not` | reverses a Boolean result |

Examples:

```python
needs_attention = is_cpu_high or is_memory_high or is_disk_high
```

```python
cpu_is_high_and_disk_is_high = is_cpu_high and is_disk_high
```

```python
is_healthy = True
is_unhealthy = not is_healthy
```

### 9. Mixed `and` / `or`
Use parentheses to make intent explicit.

```python
result1 = cpu_high or (memory_high and disk_high)
result2 = (cpu_high or memory_high) and disk_high
```

Even when Python can evaluate the expression without parentheses, explicit grouping improves readability.

---

## DevOps Practical — Server Resource Checker

```python
server_name = "production-server-01"

cpu_usage = float(input("Enter CPU usage percentage: "))
memory_usage = float(input("Enter memory usage percentage: "))
disk_usage = float(input("Enter disk usage percentage: "))

cpu_threshold = 80
memory_threshold = 75
disk_threshold = 90

is_cpu_high = cpu_usage >= cpu_threshold
is_memory_high = memory_usage >= memory_threshold
is_disk_high = disk_usage >= disk_threshold

needs_attention = (
    is_cpu_high
    or is_memory_high
    or is_disk_high
)

print("\n==== SERVER REPORT ====")
print(f"Server: {server_name}")
print(f"CPU usage: {cpu_usage:.2f}%")
print(f"Memory usage: {memory_usage:.2f}%")
print(f"Disk usage: {disk_usage:.2f}%")
print(f"Is CPU high? {is_cpu_high}")
print(f"Is memory high? {is_memory_high}")
print(f"Is disk high? {is_disk_high}")
print(f"Needs attention: {needs_attention}")
```

### Program architecture

```text
1. INPUT
   ↓
2. RULES / THRESHOLDS
   ↓
3. EVALUATION
   ↓
4. DECISION
   ↓
5. REPORT
```

Example:

```text
User input: 85.5
      ↓
float conversion: 85.5
      ↓
85.5 >= 80
      ↓
True
      ↓
is_cpu_high = True
      ↓
needs_attention = True
```

This pattern is useful later because an agent also follows an observe → evaluate → decide → act/report style, although an agent adds model reasoning and tools.

### Dry-run scenarios

| Scenario | CPU | Memory | Disk | Needs attention |
|---|---:|---:|---:|---|
| Healthy | 45 | 60 | 70 | False |
| Boundary | 80 | 75 | 90 | True |
| One issue | 40 | 82 | 50 | True |

### Common mistakes

- Using `int(input())` when decimal percentages such as `82.5` are possible.
- Using `>` when the requirement includes the threshold itself; use `>=`.
- Using `and` when any one high metric should trigger attention; use `or`.
- Printing `"cpu_usage"` instead of the variable `cpu_usage`.
- Giving a Boolean flag a misleading label.

---

## Quick Revision Sheet

| Topic | Remember |
|---|---|
| Variable | `name = "Brijesh"` |
| Text vs variable | `"name"` is text; `name` is the variable |
| f-string | `f"Hello {name}"` |
| Input | `input()` returns `str` |
| Integer input | `int(input(...))` |
| Decimal input | `float(input(...))` |
| Money formatting | `f"Rs. {amount:,.2f}"` |
| Assignment | `=` |
| Equality | `==` |
| Inclusive threshold | `>=` |
| Any condition | `or` |
| All conditions | `and` |
| Reverse Boolean | `not` |
| Remainder | `%` |
| Floor division | `//` |

## Practice Questions

1. What is the difference between `print("name")` and `print(name)`?
2. What type does `input()` return by default?
3. Calculate annual income for monthly salary `120000` and bonus `200000`.
4. What is `17 % 5`?
5. How do you check whether CPU usage has reached or exceeded a threshold of 80?
6. If CPU is False, memory is True and disk is False, what is `needs_attention` when using `or`?
7. Explain `and` vs `or` in your own words.
8. Why can `float()` be preferable for CPU/memory percentages?
9. Which is valid: `server-name`, `1server`, or `server_name`?
10. What does `salary * 2` do if `salary = "100"`?
11. Format `125000.5` with comma separators and two decimal places.
12. What is `(10 + 5) * 2` and why do parentheses matter?

## Mini Challenge
Create a program that accepts:

- `service_name`
- `response_time_ms`
- `error_rate`

Thresholds:

- `response_time_ms >= 500`
- `error_rate >= 5`

Print both Boolean results and `needs_attention`.

The intended pattern is:

```text
Input → Convert → Compare → Boolean flags → OR → Report
```

## Completion Status

- [x] Day 01 — Variables and data types
- [x] Day 02 — Input and type conversion
- [x] Day 03 — Operators and comparisons
- [ ] Day 04 — `if`, `elif`, `else`

**Next:** Continue with Day 04 after this checkpoint.
