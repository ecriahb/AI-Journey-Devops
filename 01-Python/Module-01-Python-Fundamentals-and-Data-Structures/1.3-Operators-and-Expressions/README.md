# 1.3 Basic Operators and Expressions

## Arithmetic operators

`+`, `-`, `*`, `/`, `//`, `%`, `**`

```python
print(10 + 3)
print(10 // 3)  # 3
print(10 % 3)   # 1
print(2 ** 3)   # 8
```

## Comparison operators

`>`, `<`, `>=`, `<=`, `==`, `!=`

They produce `True` or `False`.

```python
cpu_usage = 82
print(cpu_usage >= 80)  # True
```

## Logical operators

- `and` — all required conditions are true
- `or` — at least one condition is true
- `not` — reverses a Boolean result

```python
needs_attention = cpu_high or memory_high
```

## Assignment vs comparison

```python
threshold = 80   # assignment
threshold == 80  # comparison
```

## Curriculum hands-on

Even/odd check:

```python
number = int(input("Enter a number: "))
print("Even" if number % 2 == 0 else "Odd")
```

## DevOps connection
Operators are used for threshold checks, capacity calculations, retry counters, health checks and automation decisions.

## Practice

Write a program that accepts response time and error rate and sets `needs_attention` when either threshold is reached.
