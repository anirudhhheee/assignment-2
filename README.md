# Highest Student Score Using Max Heap and Linear Search

## Problem Statement

A university wants to identify the highest student score from the following data:

**78, 92, 65, 88, 95, 72, 84, 90**

The objective is to implement a **Max Heap**, insert all the scores, record the heap arrangement after every insertion, and find the highest score using both **Max Heap** and **Linear Search**.

---

## Input Data

```text
78, 92, 65, 88, 95, 72, 84, 90
```

---

## Max Heap Insertion Trace

| Insertion | Heap Arrangement        |
| --------- | ----------------------- |
| 78        | 78                      |
| 92        | 92 78                   |
| 65        | 92 78 65                |
| 88        | 92 88 65 78             |
| 95        | 95 92 65 78 88          |
| 72        | 95 92 72 78 88 65       |
| 84        | 95 92 84 78 88 65 72    |
| 90        | 95 92 84 90 88 65 72 78 |

### Final Max Heap

```text
95 92 84 90 88 65 72 78
```

The root element of the Max Heap is **95**, which is the highest student score.

---

## Finding the Maximum Using Max Heap

In a Max Heap, the largest element is always stored at the root.

Therefore:

```text
Maximum Score = 95
```

The maximum can be obtained directly from the root.

### Operations

* Parent comparisons during insertion: **12**
* Swaps during insertion: **7**
* Maximum retrieval: **O(1)**

---

## Finding the Maximum Using Linear Search

Linear Search checks each score one by one and keeps track of the largest value found.

The comparisons are:

```text
78 → 92
92 → 65
92 → 88
92 → 95
95 → 72
95 → 84
95 → 90
```

Therefore:

```text
Maximum Score = 95
Number of Comparisons = 7
```

---

## Complexity Analysis

| Operation          | Max Heap | Linear Search |
| ------------------ | -------- | ------------- |
| Find Maximum       | O(1)     | O(n)          |
| Insert New Score   | O(log n) | O(1)          |
| Search for Maximum | O(1)     | O(n)          |
| Space Complexity   | O(n)     | O(n)          |

### Max Heap

Insertion into a Max
