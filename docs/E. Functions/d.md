# Type Hints

Python is dynamically typed, so I could easily pass a string to the function and generate a bug! From Python v3.5 onwards, we have _type hints_. I could tell the function that I am passing a float and expect it to return a float.

```python
def calculate_circumference(radius: float) -> float:
    return radius * 2 * 3.142

print(calculate_circumference(5))
```
