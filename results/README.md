# Equal sums of like powers

Two classical questions, then a mixed-exponent search.

## Same exponent: `a^k + b^k = c^k + d^k`

Primitive solutions (`gcd(a,b,c,d)=1`, `{a,b} ≠ {c,d}`):

| k | what is known |
|---|---|
| 2 | infinitely many (sums of two squares) |
| 3 | infinitely many (taxicab numbers; Hardy–Wright) |
| 4 | infinitely many; parametric families exist. Wroblewski listed the primitives with bases ≤ 10^14 |
| ≥ 5 | no primitive solution known. Guy (D1): searches for k=5 at least to N < 10^25. Fermat’s Last Theorem rules out a zero term |

These are *equal sums of like powers*. The tables below are not this equation.

## Two exponents: `a^j + b^j = c^k + d^k`

Wagstaff, [Equal Sums of Two Distinct Like Powers](https://cs.uwaterloo.ca/journals/JIS/VOL25/Wagstaff/wagstaff8.html), *J. Integer Sequences* **25** (2022), studies `2 < j < k`. The density heuristic (birthday / Erdős–Ulam) says:

- `2/j + 2/k > 1` — expect many primitives
- `= 1` — borderline
- `< 1` — expect finitely many, perhaps none

Wagstaff found primitives only for `(j,k) = (3,4), (3,5), (3,6)` among `2 < j < k < 11`. Ulas, [On the Diophantine equation `x^3 ± y^3 = a^k ± b^k`](https://arxiv.org/abs/2402.06567), pushed the `j=3` searches further (both signs).

Published counts we reproduce, then the files here:

| source | k | M | sum | diff |
|--------|--:|--:|----:|-----:|
| Wagstaff | 4 | 10^4 | 75 | — |
| Wagstaff | 5 | 5000 | 14 | — |
| Wagstaff | 6 | 1400 | 7 | — |
| Ulas | 4 | 10^5 | 355 | 648 |
| Ulas | 5 | 5·10^4 | 56 | 99 |
| Ulas | 6 | 5·10^4 | 28 | 83 |
| Ulas | 7 | 5·10^4 | 0 | 1 |

## Files (`j = 3`)

| file | equation | bound | n |
|------|----------|-------|--:|
| `k4_x3y3_eq_a4b4_M1e7.csv` | X^3 + Y^3 = A^4 + B^4 | A,B ≤ 10^7, sum, primitive | 7629 |
| `k5_x3y3_eq_c5d5_M1e6.csv` | X^3 + Y^3 = C^5 + D^5 | C,D ≤ 10^6, sum, primitive | 216 |
| `k6_x3y3_eq_c6d6_M5e5.csv` | X^3 + Y^3 = C^6 + D^6 | C,D ≤ 5·10^5, sum, primitive | 69 |
| `k7_x3minusy3_eq_c7d7.csv` | X^3 − Y^3 = C^7 + D^7 | one recorded instance | 1 |

k=4,5,6: gcd of the four bases is 1; parametric trivial families excluded (`a = c^{k/3}` when 3 divides k, and the like). k=6 sits on Wagstaff’s borderline `2/3 + 2/6 = 1`. k=7 is the Ulas instance `1250534^3 − 637445^3 = 402^7 + 51^7`.

## Mixed: variable exponents

`a^A + b^B = c^C + d^D` with each exponent in `2..8` and bases ≤ 1000. This is not a fixed k; A,B,C,D may all differ.

| file | n |
|------|--:|
| `mixed_grid_M1000.csv` | 45436 |

Raw collisions were 96,332. This file keeps one writing per identity: each term is reduced to the least exponent in `2..8` (`d^4 → (d^2)^2`, `8^2 → 2^6` the other way, and so on), then drops rows that become *same-k* on both sides (`a^2+b^2 = c^2+d^4` is just two squares). gcd=1 and no single term equal to a term on the other side.

Most of the 45,436 are still the dense families (`σ = 1/A+1/B+1/C+1/D > 1`), especially `a^2+b^2 = c^2+d^3`. The sparse `σ < 1` rows are the interesting residue; they have not been separated yet.
