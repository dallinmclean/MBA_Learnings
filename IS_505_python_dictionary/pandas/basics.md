# Python Basics

This document covers foundational Python tools and behaviors used when working with:
- strings  
- lists  
- dictionaries  
- tuples  
- basic loops and indexing  

---

## Working with Strings

### Basic Operations
- `len(string)` → returns the number of characters  
- `string.upper()` / `string.lower()` / `string.capitalize()` → change letter casing  
- `string + string` → concatenates two strings  
- `string[x]` → retrieves the character at index `x`

### Searching Within Strings
- `string.find("abc")` → returns the index of `"abc"` or `-1` if not found  
- `string.index("abc")` → same as `.find()` but throws an error if not found  
- `string.startswith("abc")` / `string.endswith("xyz")` → return `True` or `False`

### Replacing & Splitting
- `string.replace("old", "new")` → replaces all instances of `"old"`  
- `string.split()` → splits at whitespace → returns a *list*  
- `string.split("x")` → splits at `"x"` and removes the separator  
- `string.splitlines()` → splits on newline characters  
- `"separator".join(list_of_strings)` → joins elements back into one string  

### Type Conversion & Cleanup
- `str(anything)` → converts to string  
- `string.strip()` → trims leading and trailing whitespace  

---

## Working with Dictionaries

### Accessing and Inspecting Data
- `dict.items()` → returns a list-like view of `(key, value)` pairs  
- `dict.get(key, default)` → returns the value or a fallback value  
  - Useful when counting or building dictionaries dynamically  

### Example Count Pattern
```python
counts = {}
for item in sequence:
    counts[item] = counts.get(item, 0) + 1
```