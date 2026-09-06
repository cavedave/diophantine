# x³ ± y³ = aᵏ + bᵏ

The tables here are this equation: **left side cubes**, right side two k-th powers. k is 4, 5, 6, or 7 in the named files. Mixed is the same idea with every exponent allowed to vary.

## Files (left side always cubes)

| file | equation | bound | n |
|------|----------|-------|--:|
| `k4_x3y3_eq_a4b4_M1e7.csv` | X^3 + Y^3 = A^4 + B^4 | A,B ≤ 10^7, sum, primitive | 7629 |
| `k5_x3y3_eq_c5d5_M1e6.csv` | X^3 + Y^3 = C^5 + D^5 | C,D ≤ 10^6, sum, primitive | 216 |
| `k6_x3y3_eq_c6d6_M5e5.csv` | X^3 + Y^3 = C^6 + D^6 | C,D ≤ 5·10^5, sum, primitive | 69 |
| `k7_x3minusy3_eq_c7d7.csv` | X^3 − Y^3 = C^7 + D^7 | one recorded instance | 1 |

k=4,5,6: gcd of the four bases is 1; parametric trivial families excluded (`X = C^{k/3}` when 3 divides k, and the like). k=6 sits on Wagstaff’s borderline `2/3 + 2/6 = 1`. k=7 is `1250534^3 − 637445^3 = 402^7 + 51^7`.

Wagstaff, [Equal Sums of Two Distinct Like Powers](https://cs.uwaterloo.ca/journals/JIS/VOL25/Wagstaff/wagstaff8.html), *J. Integer Sequences* **25** (2022), studied `a^j + b^j = c^k + d^k` for `2 < j < k`. The density heuristic says many primitives when `2/j + 2/k > 1`, a few when equal to 1, and finitely many (perhaps none) when less. For `j=3` that is k=4 and 5 many, k=6 borderline, k≥7 sparse. He found primitives only for `(j,k) = (3,4), (3,5), (3,6)` among `2 < j < k < 11`. Ulas, [On the Diophantine equation `x^3 ± y^3 = a^k ± b^k`](https://arxiv.org/abs/2402.06567), pushed the cube searches further (both signs).

| source | k | M | sum | diff |
|--------|--:|--:|----:|-----:|
| Wagstaff | 4 | 10^4 | 75 | — |
| Wagstaff | 5 | 5000 | 14 | — |
| Wagstaff | 6 | 1400 | 7 | — |
| Ulas | 4 | 10^5 | 355 | 648 |
| Ulas | 5 | 5·10^4 | 56 | 99 |
| Ulas | 6 | 5·10^4 | 28 | 83 |
| Ulas | 7 | 5·10^4 | 0 | 1 |

## Mixed: variable exponents

`a^A + b^B = c^C + d^D` with each exponent in `2..8` and bases ≤ 1000. No side is fixed to cubes.

| file | n |
|------|--:|
| `mixed_grid_M1000.csv` | 45436 |

Raw collisions were 96,332. This file keeps one writing per identity: each term is reduced to the least exponent in `2..8`, then drops rows that become the same shape on both sides (`a^2+b^2 = c^2+d^4` is just two squares). gcd=1 and no single term equal to a term on the other side.

Most of the 45,436 are still the dense families (`σ = 1/A+1/B+1/C+1/D > 1`), especially `a^2+b^2 = c^2+d^3`. The sparse `σ < 1` rows have not been separated yet.

## Aside: same exponent on all four terms

A different equation, not what these files solve:

`a^k + b^k = c^k + d^k` with `gcd=1` and `{a,b} ≠ {c,d}`.

Infinitely many primitives for k=2 (two squares), k=3 (taxicab / Hardy–Wright), and k=4 (parametric; Wroblewski listed bases ≤ 10^14). **No primitive solution is known for any k≥5.** Guy (D1): k=5 has been searched at least to N < 10^25. Fermat’s Last Theorem is the special case with a zero term.
