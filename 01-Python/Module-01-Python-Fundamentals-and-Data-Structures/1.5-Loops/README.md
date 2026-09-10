# 1.5 Loops — `for`, `while`

## Core idea
Loops repeat a block of code.

### `for`
Use when iterating over a known sequence or collection.

```python
services = ["api", "worker", "frontend"]

for service in services:
    print(service)
```

### `while`
Use when repetition depends on a condition.

```python
retries = 0

while retries < 3:
    print(f"Attempt {retries + 1}")
    retries += 1
```

## Important concepts

- loop variable
- iterable/sequence
- condition
- updating loop state
- avoiding unintended infinite loops

## DevOps connection
Loops are common when processing multiple services, files, environments, resources or retry attempts.

## Practice

1. Iterate through a list of service names.
2. Print retry attempts from 1 to 3.
3. Process a list of server CPU values and identify values above a threshold.
