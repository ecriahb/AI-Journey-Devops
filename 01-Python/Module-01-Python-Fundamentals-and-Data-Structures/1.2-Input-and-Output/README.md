# 1.2 Input and Output — `print()`, `input()`

## Core notes

`print()` displays output.

```python
print("Hello Python")
```

`input()` accepts user input and returns a **string**.

```python
name = input("Enter your name: ")
```

Convert input when numeric data is required:

```python
age = int(input("Enter age: "))
salary = float(input("Enter salary: "))
```

### Formatting

```python
amount = 125000.567
print(f"Rs. {amount:,.2f}")
```

Output: `Rs. 125,000.57`

## Curriculum hands-on

Calculate total product cost from user-entered price and quantity:

```python
price = float(input("Enter price: "))
quantity = int(input("Enter quantity: "))
total = price * quantity
print(f"Total cost: Rs. {total:,.2f}")
```

## Common mistake

```python
x = input("Number: ")
y = input("Number: ")
print(x + y)  # string concatenation
```

Use numeric conversion if arithmetic is intended.

## Practice

Build an interactive server-status report that accepts server name and CPU percentage.
