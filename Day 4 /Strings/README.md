# String Operations in Data Structures and Algorithms

Strings are sequences of characters stored in contiguous memory. They are immutable in some languages (Java, Python) and mutable in others (C). Efficient string handling is critical because many algorithms depend on pattern matching, searching, and text manipulation.

---

## 1. Basic Operations

### 1.1 Length
Returns the number of characters in the string.

Time Complexity:  
- **O(1)** if cached (Java, C++)  
- **O(n)** if traversal needed (C)

### 1.2 Accessing Characters
Index-based access to any character.

Time Complexity: **O(1)**

Example:
```c
char c = s[i];
