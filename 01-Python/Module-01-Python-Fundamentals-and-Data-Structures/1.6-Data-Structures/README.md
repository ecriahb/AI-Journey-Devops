# 1.6 Data Structures — Lists, Tuples, Sets, Dictionaries

## List
Ordered, mutable collection.

```python
services = ["api", "worker", "frontend"]
services.append("scheduler")
```

## Tuple
Ordered collection that is immutable after creation.

```python
region = ("eastus", "westeurope")
```

## Set
Collection of unique values.

```python
environments = {"dev", "qa", "dev"}
print(environments)  # duplicate is removed
```

## Dictionary
Key-value mapping.

```python
prices = {"cpu": 80, "memory": 75}
print(prices["cpu"])
```

## Curriculum hands-on

Create a list of customer names and sort alphabetically.

```python
customers = ["Ravi", "Anita", "Brijesh"]
customers.sort()
print(customers)
```

Create a product-price dictionary and retrieve a price from user input.

```python
prices = {"laptop": 50000, "mouse": 800}
product = input("Enter product: ").lower()
print(prices.get(product, "Product not found"))
```

## DevOps connection
Lists can represent services/resources, sets can remove duplicate resource IDs, and dictionaries naturally represent configuration and JSON-like API data.
