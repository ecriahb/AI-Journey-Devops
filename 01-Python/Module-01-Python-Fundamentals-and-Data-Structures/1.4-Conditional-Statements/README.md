# 1.4 Conditional Statements — `if`, `elif`, `else`

## Core idea
Conditional statements allow a program to choose a path based on a Boolean condition.

```python
cpu = 85

if cpu >= 80:
    print("High CPU")
elif cpu >= 60:
    print("Moderate CPU")
else:
    print("Normal CPU")
```

### Structure

```text
if      → first condition
elif    → additional condition(s)
else    → fallback path
```

Python uses indentation to define the code block.

## DevOps example

```python
deployment_status = "failed"

if deployment_status == "failed":
    print("Investigate deployment")
elif deployment_status == "running":
    print("Deployment in progress")
else:
    print("Deployment completed")
```

## Practice

Create a program that classifies CPU usage as Normal, Warning or Critical using clearly defined thresholds.
