# 1.8 Iterating over Data Structures

## Core idea
Iteration means visiting elements of a collection one by one.

### List

```python
services = ["api", "worker", "frontend"]
for service in services:
    print(service)
```

### Dictionary

```python
prices = {"api": 100, "worker": 150}

for name, price in prices.items():
    print(f"{name}: {price}")
```

Useful dictionary views:

```python
prices.keys()
prices.values()
prices.items()
```

### Set

```python
regions = {"eastus", "westeurope", "eastus"}
for region in regions:
    print(region)
```

Set iteration order should not be relied upon.

## DevOps connection
Iteration is fundamental when processing multiple services, deployments, resource IDs, configuration entries or API response records.

## Practice

Given a dictionary of service names and replica counts, print each service and determine which services have more than 3 replicas.
