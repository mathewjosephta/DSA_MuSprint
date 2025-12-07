# DSA Fundamental Concepts: Strings and Linked Lists

This document summarizes two core data structures used in technical interviews and real-world systems. If you can't explain when to use each of these and why, you're not ready for serious problem solving.

---

## 1. STRINGS

A string is a sequential collection of characters. It may be immutable (Python, Java) or mutable (C). Performance depends on how often you copy characters.

### Core Operations

| Operation | Description | Time Complexity |
|----------|-------------|----------------|
| Length | Count characters | O(1) if cached, O(n) otherwise |
| Access | Get character at index | O(1) |
| Concatenate | Combine strings | O(n + m) for immutables, O(1) amortized for builders |
| Compare | Equality or lexical order | O(n) |
| Substring | Extract part of a string | O(k) |

### Common String Tasks

| Task | Idea | Time |
|------|------|------|
| Reverse | Swap ends inward | O(n) |
| Palindrome Check | Two-pointer | O(n) |
| Frequency Count | Hash or array | O(n) |
| Anagram | Compare frequencies | O(n) |
| Rotation Check | Check if s2 in s1+s1 | O(n) |

### Pattern Matching Algorithms

| Algorithm | Why It Matters | Time |
|----------|---------------|------|
| Naive | Bruteforce match | O(nm) |
| KMP | Skips redundant checks using LPS | O(n + m) |
| Rabin-Karp | Hash-based matching | O(n + m) average |
| Boyer-Moore | Skips based on mismatches | Excellent for large alphabets |

### String Data Structures

| Structure | Purpose | Benefit |
|----------|---------|---------|
| Trie | Prefix-based storage | O(m) insert/search |
| Suffix Array | Sorted suffixes | Fast substring lookup |
| Suffix Tree | Stores all suffixes | O(m) search |
| Rolling Hash | Converts string to number | Enables fast comparison |

### Why Strings Matter

- Used in databases, compilers, network protocols, NLP, and search engines.
- Interviewers love string problems because they expose lazy thinking about memory and time.

### Complexity Recap

| Operation | Complexity |
|----------|------------|
| Compare strings | O(n) |
| Concatenate immutable | O(n) |
| KMP search | O(n + m) |
| Reverse | O(n) |

If you manipulate strings without considering copying costs, you're writing slow code.

---

## 2. LINKED LISTS

Linked lists are collections of nodes connected via pointers. They solve the problem arrays can't handle efficiently: cheap insertions and deletions without shifting elements.

### Why Linked Lists Exist

| Feature | Array | Linked List |
|--------|-------|-------------|
| Memory | Contiguous | Dynamic |
| Random Access | O(1) | Impossible |
| Insert/Delete at Start | O(n) | O(1) |
| Cache Efficiency | High | Weak |

If you want fast random access, use arrays. If your workload inserts or deletes frequently, linked lists win.

### Types of Linked Lists

| Type | Description | Use Case |
|------|-------------|----------|
| Singly | One pointer to next | Basic queues, stacks |
| Doubly | Pointers to prev/next | LRU cache, editor history |
| Circular | Last points to first | Round-robin scheduling |

### Node Structure

