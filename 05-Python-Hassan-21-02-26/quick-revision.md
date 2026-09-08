# Python Lesson 03 — Quick Revision

## Core Flow
**Jupyter → Syntax → Semantics → Comments → Variables → Data Types → Conditions → Loops → Lists → Indexing → Methods → Slicing**

## Must Remember

### Jupyter
- Markdown = documentation/headings.
- Code = executable Python.
- Restart kernel if a cell gets stuck.

### Syntax vs Semantics
- **Syntax:** rules for writing valid code.
- **Semantics:** meaning/behavior of the code.

### Comments
```python
# single-line comment
```

### Variables
```python
x = 5
name = "Alex"
```
Python is case-sensitive and dynamically typed/type-inferred.

### Basic Types
```python
5       # int
3.14    # float
"Alex"  # str
```

Check type:
```python
print(type(x))
```

### If
```python
if age >= 18:
    print("Adult")
```
Remember `:` + indentation.

### For Loop
```python
for fruit in fruits:
    print(fruit)
```

### List
```python
fruits = ["apple", "banana", "cherry"]
```
Lists are mutable.

### Indexing
```text
apple  -> 0
banana -> 1
cherry -> 2
```
Negative:
```text
cherry -> -1
banana -> -2
apple  -> -3
```

### Modify
```python
fruits[0] = "blueberry"
```

### List Methods
```python
fruits.append("orange")
fruits.remove("blueberry")
fruits.sort()
fruits.sort(reverse=True)
```

### Slicing
```python
list[start:stop:step]
```
**Stop is excluded.**

Examples:
```python
fruits[:2]
fruits[1:]
fruits[::-1]
```

## Common Errors
- `IndentationError`
- `SyntaxError`
- `NameError`

## One-Line Interview Answers
- Python list = mutable collection of items.
- Python indexing starts at 0.
- `-1` = last element.
- `append()` = add at end.
- `remove()` = remove first occurrence of specified item.
- `sort()` = sort list; reverse sorting can use `reverse=True`.
- Slicing stop index is excluded.
