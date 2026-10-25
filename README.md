
# Project 02 — Prime Numbers and Goldbach

## Project Overview

This project explores prime numbers and Goldbach's conjecture using Python. It covers primality testing, prime number generation, Goldbach representations, and the identification of even numbers with the highest number of prime pairs.

All four required tasks, the mathematical discussion, and the optional exercise on twin primes are included.

## Group Information

**Course:** Computing with Python  
**Project:** 02 — Prime Numbers and Goldbach  
**Group:** 02  
**Originally assigned group size:** 5  
**Active participants:** 4

### Group Members

1. Kambale Maruba Exaucé
2. Adja Marie Josephine DIOP
3. BOKATOLA KIWA MIREILLE SAMANTHA
4. MAMADOU SARR NIANG

**Note:** Mr. ESSOZIMNA KONDO was initially expected to be the fifth member. Unfortunately, we were unable to reach him or arrange his participation during the project period. The four available members therefore completed the work together.

## Repository Contents

| File | Description |
|---|---|
| `Project_02_Prime_Numbers_and_Goldbach.ipynb` | Python solutions for all tasks and the optional exercise |
| `README.md` | Project description and results |
| `REFLECTION.md` | Group collaboration and reflection |

## Task 1 — Prime Number Test

We implemented `is_prime(n)` to determine whether an integer is prime.

```python
is_prime(97)  # True
is_prime(91)  # False
is_prime(1)   # False
```

The algorithm tests possible divisors only up to the square root of `n`, reducing the time complexity to `O(sqrt(n))`.

## Task 2 — Prime Numbers Up to n

The function `primes_up_to(n)` generates all prime numbers between 2 and `n`, inclusive.

```python
primes_up_to(20)
# [2, 3, 5, 7, 11, 13, 17, 19]

len(primes_up_to(100))
# 25
```

## Task 3 — Goldbach Pairs

The function `goldbach_pairs(n)` finds all unique pairs of prime numbers whose sum equals the given even integer.

```python
goldbach_pairs(10)
# [(3, 7), (5, 5)]

goldbach_pairs(28)
# [(5, 23), (11, 17)]
```

We use `p <= n - p` to avoid counting reversed pairs twice.

For odd numbers or integers below 4, the function returns an empty list.

## Task 4 — Maximum Goldbach Representations

We searched for the even number with the highest number of Goldbach representations within a given limit.

| Limit | Best Even Number | Number of Pairs |
|---|---|---|
| 100 | 90 | 9 |
| 200 | 180 | 14 |
| 500 | 420 | 30 |

The algorithm keeps the smallest even number when multiple numbers have the same maximum count.

This is achieved using the strict comparison `count > best_count`.

## Think and Explain

The prime factorizations of the two interesting numbers are:

- `90 = 2 × 3² × 5`
- `180 = 2² × 3² × 5`

Both numbers share small prime factors, particularly 2, 3, and 5.

Divisibility by small primes influences which prime pairs can represent an even number. However, having more prime factors does not necessarily guarantee more Goldbach representations.

The observed counts are obtained by enumeration, not directly from prime factorization.

Checking finitely many even numbers provides numerical evidence but does not prove Goldbach's conjecture for all even integers.

## Optional Task — Twin Prime Pairs

Two prime numbers form a twin prime pair when their difference is exactly 2.

```python
twin_primes_below(100)
# [(3, 5), (5, 7), (11, 13), (17, 19),
#  (29, 31), (41, 43), (59, 61), (71, 73)]
```

There are **8 twin prime pairs below 100**.

## Running the Project

1. Clone or download this repository.
2. Open `Project_02_Prime_Numbers_and_Goldbach.ipynb` in Jupyter Notebook or VS Code.
3. Select a Python 3 kernel.
4. Run the cells in order.

The notebook uses only standard Python functionality and does not require additional third-party libraries.

## Group Collaboration

Each of the four active members independently worked on all project questions, including the optional exercise.

We then compared our proposed solutions, discussed the different approaches, and combined our work into a common final solution.

Further details are provided in `REFLECTION.md`.
