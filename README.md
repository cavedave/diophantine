# Introduction

What solutions exist for the equation \(x^3 \pm y^3 = a^k \pm b^k\)?

This calculation is based on work by Wagstaff, [Equal Sums of Two Distinct Like Powers](https://cs.uwaterloo.ca/journals/JIS/VOL25/Wagstaff/wagstaff8.html), *J. Integer Sequences* **25** (2022), and Ulas, [On the Diophantine equation \(x^3 \pm y^3 = a^k \pm b^k\)](https://arxiv.org/abs/2402.06567).

Left side two cubes, right side two \(k\)-th powers. Primitive: gcd of the four bases is 1. The trivial family \(X = A^{k/3}\), \(Y = B^{k/3}\) is dropped when \(3 \mid k\). CSVs live in [results/](results/).

## Census files

| file | equation | bound | n |
|------|----------|-------|--:|
| `k4_x3y3_eq_a4b4_M3e7.csv` | \(X^3 + Y^3 = A^4 + B^4\) | \(A,B \le 3\cdot10^7\), sum | 15777 |
| `k4_x3minusy3_eq_a4b4_M1e6.csv` | \(X^3 - Y^3 = A^4 + B^4\) | \(A,B \le 10^6\), diff | 3207 |
| `k5_x3y3_eq_c5d5_M2e6.csv` | \(X^3 + Y^3 = C^5 + D^5\) | \(C,D \le 2\cdot10^6\), sum | 272 |
| `k5_x3minusy3_eq_c5d5_M1e6.csv` | \(X^3 - Y^3 = C^5 + D^5\) | \(C,D \le 10^6\), diff | 403 |
| `k6_x3y3_eq_c6d6_M1e6.csv` | \(X^3 + Y^3 = C^6 + D^6\) | \(C,D \le 10^6\), sum | 91 |
| `k6_x3minusy3_eq_c6d6_M1e6.csv` | \(X^3 - Y^3 = C^6 + D^6\) | \(A,B \le 10^6\), diff | 240 |
| `k7_x3minusy3_eq_c7d7.csv` | \(X^3 - Y^3 = C^7 + D^7\) | one recorded instance | 1 |
| `k8_x3y3_eq_a8b8_M3e4.csv` | \(X^3 \pm Y^3 = A^8 + B^8\) | \(A,B \le 3\cdot10^4\), both signs | 0 |
| `k9_x3y3_eq_a9b9_M4000.csv` | \(X^3 \pm Y^3 = A^9 + B^9\) | \(A,B \le 4000\), both signs | 11 |
| `k15_x3minusy3_eq_a15b15_M100.csv` | \(X^3 - Y^3 = A^{15} + B^{15}\) | \(A,B \le 100\) | 1 |

k=4 sums through \(3\cdot10^7\) include the published 7629 at \(10^7\). k=7 is \(1250534^3 - 637445^3 = 402^7 + 51^7\) (Ulas); not a complete \(M\)-census. k=8 is a finished empty search. k=9 is thin: 9 through \(M=1000\), then one more in \((1000,2000]\) and one in \((2000,4000]\).

CSV columns: `X,Y,A,B,sign` with \(X \ge Y\), \(A \ge B\), `sign` `+` or `−`. The k=7 file uses `X,Y,C,D`.

## Published checkpoints

The density heuristic says many primitives when \(2/3 + 2/k > 1\) (k=4,5), a few when equal to 1 (k=6), and finitely many when less (k ≥ 7).

| source | k | M | sum | diff |
|--------|--:|--:|----:|-----:|
| Wagstaff | 4 | \(10^4\) | 75 | — |
| Wagstaff | 5 | 5000 | 14 | — |
| Wagstaff | 6 | 1400 | 7 | — |
| Ulas | 4 | \(10^5\) | 355 | 648 |
| Ulas | 5 | \(5\cdot10^4\) | 56 | 99 |
| Ulas | 6 | \(5\cdot10^4\) | 28 | 83 |
| Ulas | 7 | \(5\cdot10^4\) | 0 | 1 |
| this repo | 4 | \(3\cdot10^7\) | 15777 | — |
| this repo | 4 | \(10^6\) | — | 3207 |
| this repo | 5 | \(2\cdot10^6\) | 272 | — |
| this repo | 5 | \(10^6\) | — | 403 |
| this repo | 6 | \(10^6\) | 91 | 240 |
| this repo | 9 | 4000 | 3 | 8 |

## Mixed: variable exponents

\(a^A + b^B = c^C + d^D\) with each exponent in 2..8 and bases ≤ 1000. No side is fixed to cubes.

| file | n |
|------|--:|
| `mixed_grid_M1000.csv` | 45436 |
| `mixed_grid_sigma_lt1.csv` | 2 |

Raw collisions were 96,332. What \(\sigma\) is, and the two \(\sigma<1\) identities, are in [mixedgrid.md](mixedgrid.md).

---

(6,1,5)-type searches (equal sums of sixth powers) live in a separate project: [cavedave/six-one-five](https://github.com/cavedave/six-one-five).

## References

[^1^]: S. S. Wagstaff, Jr., [Equal Sums of Two Distinct Like Powers](https://cs.uwaterloo.ca/journals/JIS/VOL25/Wagstaff/wagstaff8.html), *J. Integer Sequences* **25** (2022), Article 22.8.2.

[^2^]: M. Ulas, [On the Diophantine equation \(x^3 \pm y^3 = a^k \pm b^k\)](https://arxiv.org/abs/2402.06567), arXiv:2402.06567 (2024).
