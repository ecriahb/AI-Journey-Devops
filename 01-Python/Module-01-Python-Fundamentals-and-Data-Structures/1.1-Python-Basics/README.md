# 1.1 Python Basics — Syntax, Variables, Data Types

## What this topic covers
- Python syntax
- Variables and assignment
- `str`, `int`, `float`, `bool`
- `type()`
- Comments
- Naming conventions
- f-strings

## Core notes

A **variable** is a name bound to a value.

```python
name = "Brijesh"
experience = 10
salary = 28.5
is_learning = True
```

Basic types:

| Type | Example |
|---|---|
| `str` | `"AKS"` |
| `int` | `10` |
| `float` | `82.5` |
| `bool` | `True` |

Check a type:

```python
print(type(name))
```

`=` assigns a value. `==` compares values.

### f-string

```python
name = "Brijesh"
role = "DevOps Engineer"
print(f"{name} is a {role}")
```

Use meaningful `snake_case` names such as `cpu_threshold` and `memory_usage`.

## Practice

1. Create variables for server name, CPU usage and environment.
2. Print their values and types.
3. Create a formatted status message using an f-string.

## DevOps connection
Python variables become the basic building blocks for later scripts that process logs, metrics, configuration and API responses.

## Related class notes
See [Day 01–03](../Lessons/Day-01-to-03.md) for the detailed revision material already prepared.
