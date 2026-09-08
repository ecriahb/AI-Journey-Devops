# Python Lesson 03 — Interview Questions

## Beginner

1. **Why is Python popular in AI/ML?**  
   Easy to learn, versatile, large community and strong library/framework ecosystem.

2. **What is syntax?**  
   The rules that define how code must be structured.

3. **What is semantics?**  
   The meaning/behavior of correctly structured code.

4. **Why is indentation important in Python?**  
   It defines code blocks such as `if` and `for` blocks.

5. **What are the three common errors covered?**  
   `IndentationError`, `SyntaxError`, `NameError`.

6. **What is a variable?**  
   A name used to hold/reference a value.

7. **Is Python case-sensitive?**  
   Yes. `name` and `Name` are different identifiers.

8. **What is dynamic typing/type inference?**  
   Python determines a variable/value's type from the assigned value without requiring an explicit type declaration in the examples shown.

9. **What are the basic types demonstrated?**  
   `int`, `float`, `str`.

10. **How do you check a value's type?**  
    Use `type()`.

11. **What is a list?**  
    A collection of items; the instructor explained that list contents can be changed after creation.

12. **What is zero-based indexing?**  
    The first list item is at index `0`.

13. **What is negative indexing?**  
    It accesses elements from the end; `-1` is the last element.

14. **How do you modify a list item?**  
    Assign a new value to its index.

15. **What does `append()` do?**  
    Adds an item to the end of the list.

16. **What does `remove()` do?**  
    Removes the first occurrence of the specified item.

17. **What does `sort()` do?**  
    Sorts the list; `reverse=True` can be used for reverse sorting as demonstrated.

18. **What is list slicing?**  
    Extracting a portion of a list using `start:stop:step`.

19. **Is the stop index included in slicing?**  
    No.

20. **Why is a negative step useful in slicing?**  
    It allows traversal from right to left.

## Scenario Questions

### Q21. You get `NameError`. What would you check?
Check whether the variable/name has actually been defined and whether its spelling/case matches the definition.

### Q22. Your `if` block is not behaving as expected. What would you check first?
Check the condition, colon, and indentation of the statements belonging to the block.

### Q23. You need the last item of a list without knowing its length. What can you use?
Negative indexing, e.g. `my_list[-1]`.

### Q24. You need only the first two list items. What slicing can you use?
```python
my_list[:2]
```

### Q25. You need to traverse a list backward. What concept from this lesson helps?
Negative indexing/negative slicing step, for example `my_list[::-1]`.

## Interview Focus

For this lesson, be able to explain the concepts in simple language and write small examples without looking at notes. The instructor's emphasis was on practical understanding and regular practice.
