
# REFLECTION — Project 02: Prime Numbers and Goldbach

## 1. Group Members and Responsibilities

| Team Member | Contribution |
|---|---|
| Kambale Maruba Exaucé | Individual solutions, group discussion, coding and verification |
| Adja Marie Josephine DIOP | Individual solutions, group discussion and testing |
| BOKATOLA KIWA MIREILLE SAMANTHA | Individual solutions, group discussion and code review |
| MAMADOU SARR NIANG | Individual solutions, group discussion and verification |

**Collaboration:** Each of the four members independently proposed solutions to all project questions, including the optional task. We then met to compare our approaches, discuss differences, and combine our ideas into a common solution. Everyone participated in reviewing the final work.

## 2. Bug and Fix

During our review, we considered the risk of counting the same Goldbach pair twice, such as `(3, 7)` and `(7, 3)` for `n = 10`.

The incorrect approach would be:

```python
if n - p in primes:
    pairs.append((p, n - p))
```

To avoid duplicate pairs, we used:

```python
if n - p in primes and p <= n - p:
    pairs.append((p, n - p))
```

This ensures that each unordered pair is counted only once.

**Verification:**

```python
assert goldbach_pairs(10) == [(3, 7), (5, 5)]
```

## 3. What We Learned

This project helped us strengthen our understanding of Python functions, loops, conditions, lists, tuples, and mathematical reasoning.

We also learned how to improve primality testing by checking divisors only up to the square root of a number.

The most interesting challenge was finding Goldbach pairs efficiently and ensuring that each pair was counted only once.

Working individually before discussing our solutions helped us compare different approaches and understand the algorithms better.

## 4. Project Results

- **Task 1:** Implemented a function to check whether a number is prime.
- **Task 2:** Generated prime numbers up to a given limit.
- **Task 3:** Found unique Goldbach pairs for even integers.
- **Task 4:** Identified `420` as the even number with the most Goldbach pairs up to `500`, with `30` pairs.
- **Think and Explain:** Observed that numbers with several small prime factors can have many Goldbach representations, although this does not establish a general rule.
- **Optional Task:** Identified the eight twin prime pairs below `100`.

## 5. Final Reflection

We completed the project through individual effort followed by collective discussion. Comparing our solutions helped us identify possible mistakes, improve our code, and reach a shared understanding of the mathematical concepts and Python algorithms involved.
