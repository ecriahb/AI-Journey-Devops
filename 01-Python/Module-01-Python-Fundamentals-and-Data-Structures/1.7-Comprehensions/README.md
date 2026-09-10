# 1.7 List and Dictionary Comprehensions

## List comprehension
A compact way to create a list from an iterable, optionally applying a condition.

```python
numbers = [1, 2, 3, 4, 5]
squares = [n * n for n in numbers]
print(squares)
```

With a condition:

```python
even_numbers = [n for n in numbers if n % 2 == 0]
```

## Dictionary comprehension

```python
numbers = [1, 2, 3]
squares = {n: n * n for n in numbers}
```

## Readability rule
Comprehensions should stay readable. Use a normal loop when the logic becomes difficult to understand.

## DevOps connection
Useful for transforming lists of resources, filtering service names and building simple lookup/configuration dictionaries.

## Practice

Create a list of services whose names start with `api`, then create a dictionary mapping each service to its environment.
