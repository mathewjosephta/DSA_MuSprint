# String Operations in DSA

Strings are contiguous sequences of characters. They are immutable in languages like Java and Python and mutable in C. Their performance impact is significant because most operations involve character traversal.

---

## What Strings Allow You To Do

### Basic Operations
| Operation | Description | Time Complexity |
|----------|-------------|----------------|
| Length | Count characters | O(1) or O(n) |
| Access | Get char at index | O(1) |
| Concatenate | Combine strings | O(n + m) if immutable, O(1) amortized with builders |
| Compare | Lexicographical equality/order | O(n) |
| Substring | Extract part of a string | O(k) |

---

## Core DSA-Level String Techniques

### Searching and Pattern Matching
| Algorithm | Why It's Used | Time |
|----------|---------------|------|
| Naive | Straight comparison | O(nm) |
| KMP | Skips repeated checks using LPS array | O(n + m) |
| Rabin-Karp | Hash-based matching | O(n + m) average |
| Boyer-Moore | Skips characters using heuristics | Best for large patterns |

### Other Common Operations
| Task | Idea | Time |
|------|------|------|
| Reverse string | Swap ends inward | O(n) |
| Palindrome check | Two-pointer | O(n) |
| Frequency count | Hash map / char array | O(n) |
| Anagram check | Compare frequency | O(n) |
| Sorting characters | Useful for grouping anagrams | O(n log n) |

---

## Important Data Structures for Strings

### Trie
- Stores characters level-wise
- Search and insert in **O(m)** where `m` is string length
- Used for autocomplete, prefix queries

### Suffix Array
- Stores sorted suffixes
- Provides fast substring search
- Construction O(n log n), search O(m log n)

### Suffix Tree
- Compressed representation of all suffixes
- Pattern search in **O(m)**
- Heavy to implement but powerful

### Hashing (Rolling Hash)
- Converts string into a number
- Enables fast comparisons
- Basis for Rabin-Karp

---

## Must-Know Interview Problems
| Problem | Key Idea |
|--------|----------|
| Longest Palindromic Substring | Expand from center, DP for optimization |
| Longest Common Prefix | Compare characters until mismatch |
| String rotation check | `s in (s+s)` trick |
| Remove duplicates | Character set tracking |
| Pattern searching | KMP or RK when naive fails |

If you can't handle string pattern problems efficiently, you're not ready for real coding interviews. They expose whether you understand memory, iteration, and algorithmic optimization.

---

## When Strings Become Slow

- Repeated concatenation in immutable languages creates fresh copies
- Unnecessary substring creation that copies memory
- Blind use of built-in methods without knowing complexity

**Rule:** If characters are being copied, you are paying a linear cost.

---

## Why Strings Matter

- Text searching, compilers, NLP
- Database engines and file systems
- Security (hashing, encryption)
- Network protocols, compression, URL routing

Strings are not beginner fluff. They sit at the center of real software systems.

---

## Quick Complexity Recap

| Operation | Complexity |
|----------|------------|
| Access character | O(1) |
| Compare strings | O(n) |
| Concatenate (immutable) | O(n) |
| Reverse | O(n) |
| Pattern search (KMP) | O(n + m) |

---

### Final Takeaway

Mastering strings is not optional. They force you to reason about memory, iteration, and optimization. If you understand why naive concatenation is slow or how KMP avoids redoing work, you're already ahead of most candidates.

---
