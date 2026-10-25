# Project 02 — Prime Numbers and Goldbach 


## Repository contents
| `Project_02_Prime_Numbers_and_Goldbach.ipynb` | Every requirement fully solved, commented and tested |


## Task 1 — Prime number test

```python
is_prime(97)  # True
is_prime(91)  # False (91 = 7 * 13)
is_prime(1)   # False
```

A composite integer must have a divisor at most its square root; this cuts the search from `O(n)` to `O(sqrt(n))`. 


## Task 2 — Primes up to n

```python
primes_up_to(20)  # [2, 3, 5, 7, 11, 13, 17, 19]
len(primes_up_to(100))  # 25
```

## Task 3 — Goldbach pairs

```python
goldbach_pairs(10)  # [(3, 7), (5, 5)]
goldbach_pairs(28)  # [(5, 23), (11, 17)]
```

A pair `(p, q)` is kept iff `p` and `q` are prime, `p + q == n`, and `p <= q` (so no reversed duplicate). Odd inputs and even inputs below 4 return `[]` by design.

## Task 4 — Maximum, including tie breaking

We test `n = 4, 6, 8, ..., limit` and update the champion only when `count > best_count`. Updating with `>=` is incorrect because it discards the required **smaller** winner on ties.

| Inclusive limit | Smallest maximizing even number | Number of pairs |
|---:|---:|---:|
| 100 | **90** | **9** |
| 200 | **180** | **14** |
| 500 | **420** | **30** |



## Think and explain — 90 and 180

- **90 = 2 × 3 × 3 × 5 = 2 × 3² × 5**.
- **180 = 2 × 2 × 3 × 3 × 5 = 2² × 3² × 5**.
- **Observation:** both share prime factors 2, 3, 5; 180 is twice 90. Small-prime divisibility influences which prime pairs can sum to a given even number, through modular restrictions. It can help explain why some numbers have many representations, but **it is not a universal rule that more factors implies more pairs**. The specific counts 9 and 14 are found by enumerating the pairs, not deduced from the factors alone. This numerical test does not prove Goldbach's conjecture in general.



## Extra : twin primes under 100

Two primes are twins if their difference is **exactly 2**. Both primes must be **strictly less than 100**.

```python
twin_primes_below(100)
# [(3, 5), (5, 7), (11, 13), (17, 19),
#  (29, 31), (41, 43), (59, 61), (71, 73)]
```

**Answer: eight pairs.** Algorithm: generate primes less than 100, use a `set` for membership, and include `(p, p+2)` exactly when `p+2` is also in the set.  

