# LeetCode 159 – Longest Substring with At Most Two Distinct Characters

## Problem

Given a string `s`, find the length of the longest substring that contains **at most two distinct characters**.

A substring must contain characters that are next to each other in the original string.

### Example

**Input:**

```text
eceba
```

**Output:**

```text
3
```

**Explanation:**

The longest substring is:

```text
ece
```

It contains only two distinct characters: `e` and `c`.

---

## Approach

This problem can be solved efficiently using the **Sliding Window** technique.

We maintain a window using two pointers:

* `left` – beginning of the current window
* `right` – end of the current window

A dictionary is used to keep track of the frequency of each character inside the window.

### Steps

1. Start both `left` and `right` at the beginning.
2. Move `right` through the string.
3. Add each character to the dictionary.
4. If the window contains more than two distinct characters, move `left` forward.
5. Remove characters whose frequency becomes zero.
6. Keep updating the maximum window length.

---

## Example Walkthrough

For:

```text
eceba
```

The window can contain:

```text
ec
```

Then:

```text
ece
```

This contains only two distinct characters, so its length is `3`.

When `b` is added:

```text
eceb
```

there are three distinct characters: `e`, `c`, and `b`.

So the left side of the window is moved forward until only two distinct characters remain.

---

## Key Concepts

* Sliding Window
* Two Pointers
* Hash Map / Dictionary
* String Processing
* Frequency Counting

---

## Complexity

### Time Complexity

**O(n)**

Each character is added to and removed from the window at most once.

### Space Complexity

**O(1)**

At most three character entries are temporarily maintained, while the valid window contains at most two distinct characters.

---

## Important Points

* The substring must be contiguous.
* It can contain one or two distinct characters.
* If there are more than two distinct characters, shrink the window.
* The dictionary keeps track of character frequencies.
* Sliding Window avoids checking every possible substring.

---

## LeetCode Details

* **Problem Number:** 159
* **Problem Name:** Longest Substring with At Most Two Distinct Characters
* **Difficulty:** Medium
* **Language:** Python
* **Topic:** String, Sliding Window, Hash Map

---

## What I Learned

This problem helped me understand how the **Sliding Window technique** can be used to find the longest valid substring efficiently.

Instead of generating every possible substring, the window is expanded and contracted depending on the number of distinct characters. This reduces the solution to linear time.

---

# Author

T.Nandhini
