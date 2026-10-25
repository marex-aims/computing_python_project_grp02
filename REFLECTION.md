
# REFLECTION — Project 02: Prime Numbers and Goldbach

## 1. Group Members and Responsibilities

Our group was initially expected to have five members. However, only four members were available to work on the project.

| Team Member | Contribution |
|---|---|
| Kambale Maruba Exaucé | Individual solutions, group discussions, coding and review |
| Adja Marie Josephine DIOP | Individual solutions, group discussions and code review |
| BOKATOLA KIWA MIREILLE SAMANTHA | Individual solutions, group discussions and code review |
| MAMADOU SARR NIANG | Individual solutions, group discussions and final review |

**Absent member:** Mr. ESSOZIMNA KONDO was initially expected to join our group, but we were unable to reach him or arrange his participation. Consequently, the project was completed by the four available members.

### How We Worked Together

Each of us independently proposed solutions to all four tasks and the optional exercise.

Afterward, we met to compare our solutions, discuss differences, and agree on a common approach.

This helped us understand the different algorithms and improve the final implementation.

## 2. Bug and Fix

One important issue discussed during our review was the possibility of counting the same Goldbach pair twice.

For example, `(3, 7)` and `(7, 3)` represent the same unordered pair for `n = 10`.

### Incorrect Approach

```python
if n - p in primes:
    pairs.append((p, n - p))
```

Without an ordering condition, this code would include both reversed pairs.

### Correction

```python
if n - p in primes and p <= n - p:
    pairs.append((p, n - p))
```

The additional condition ensures that each pair is counted only once.

For example, the expected result for 10 is:

```python
goldbach_pairs(10)
# [(3, 7), (5, 5)]
```

This illustrates the importance of carefully handling duplicate results in mathematical algorithms.

## 3. What We Learned

Through this project, we improved our understanding of Python functions, loops, conditions, lists, tuples, and prime numbers.

We also learned that checking divisors only up to the square root of a number makes primality testing more efficient.

The most interesting part was finding Goldbach representations and identifying the even number with the largest number of pairs.

Working individually before sharing our solutions allowed us to compare ideas and better understand each task.

## 4. Project Results

- **Task 1:** Implemented a function to determine whether an integer is prime.
- **Task 2:** Generated prime numbers up to a given limit.
- **Task 3:** Found unique Goldbach representations of even integers.
- **Task 4:** Found that `420` has the highest number of Goldbach representations up to `500`, with `30` pairs.
- **Think and Explain:** Compared the prime factorizations of `90` and `180` and discussed their Goldbach representations.
- **Optional Task:** Found the eight twin prime pairs below `100`.

## 5. Final Reflection

We completed the project through individual work followed by group discussions.

Although one expected member was unavailable, the four participating members contributed to solving all the questions.

Comparing our approaches helped us improve our understanding of Python programming, prime numbers, and algorithmic problem-solving.
