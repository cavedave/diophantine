# x³ ± y³ = aᵏ + bᵏ

Left side two cubes, right side two *k*-th powers. Primitive: gcd of the four bases is 1. The trivial family X = A<sup>k/3</sup>, Y = B<sup>k/3</sup> is dropped when 3 divides *k*.

## Census files

| k | equation | bound | n |
|--:|----------|-------|--:|
| 4 | X³ + Y³ = A⁴ + B⁴ | A, B ≤ 5×10⁷, sum | [22209](k4_x3y3_eq_a4b4_M5e7.csv) |
| 4 | X³ − Y³ = A⁴ + B⁴ | A, B ≤ 10⁶, diff | [3207](k4_x3minusy3_eq_a4b4_M1e6.csv) |
| 5 | X³ + Y³ = C⁵ + D⁵ | C, D ≤ 2×10⁶, sum | [272](k5_x3y3_eq_c5d5_M2e6.csv) |
| 5 | X³ − Y³ = C⁵ + D⁵ | C, D ≤ 10⁶, diff | [403](k5_x3minusy3_eq_c5d5_M1e6.csv) |
| 6 | X³ + Y³ = C⁶ + D⁶ | C, D ≤ 10⁶, sum | [91](k6_x3y3_eq_c6d6_M1e6.csv) |
| 6 | X³ − Y³ = C⁶ + D⁶ | C, D ≤ 10⁶, diff | [240](k6_x3minusy3_eq_c6d6_M1e6.csv) |
| 7 | X³ − Y³ = C⁷ + D⁷ | one recorded instance | [1](k7_x3minusy3_eq_c7d7.csv) |
| 8 | X³ ± Y³ = A⁸ + B⁸ | A, B ≤ 3×10⁴, both signs | [0](k8_x3y3_eq_a8b8_M3e4.csv) |
| 9 | X³ ± Y³ = A⁹ + B⁹ | A, B ≤ 4000, both signs | [11](k9_x3y3_eq_a9b9_M4000.csv) |
| 15 | X³ − Y³ = A¹⁵ + B¹⁵ | A, B ≤ 100 | [1](k15_x3minusy3_eq_a15b15_M100.csv) |

k=4 sums through 5×10⁷ include the published 7629 at 10⁷. k=7 is 1250534³ − 637445³ = 402⁷ + 51⁷ (Ulas); not a complete *M*-census. k=8 is a finished empty search. k=9 is thin: 9 through *M* = 1000, then one more in (1000, 2000] and one in (2000, 4000].

CSV columns: `X,Y,A,B,sign` with X ≥ Y, A ≥ B, and `sign` `+` or `−`. The k=7 file uses `X,Y,C,D`.

## Published checkpoints

Wagstaff, [Equal Sums of Two Distinct Like Powers](https://cs.uwaterloo.ca/journals/JIS/VOL25/Wagstaff/wagstaff8.html), *J. Integer Sequences* **25** (2022). Ulas, [On the Diophantine equation x³ ± y³ = aᵏ ± bᵏ](https://arxiv.org/abs/2402.06567).

The density heuristic says many primitives when 2/3 + 2/*k* > 1 (k=4, 5), a few when equal to 1 (k=6), and finitely many when less (k ≥ 7).

| source | k | M | sum | diff |
|--------|--:|--:|----:|-----:|
| Wagstaff | 4 | 10⁴ | 75 | — |
| Wagstaff | 5 | 5000 | 14 | — |
| Wagstaff | 6 | 1400 | 7 | — |
| Ulas | 4 | 10⁵ | 355 | 648 |
| Ulas | 5 | 5×10⁴ | 56 | 99 |
| Ulas | 6 | 5×10⁴ | 28 | 83 |
| Ulas | 7 | 5×10⁴ | 0 | 1 |
| this repo | 4 | 5×10⁷ | 22209 | — |
| this repo | 4 | 10⁶ | — | 3207 |
| this repo | 5 | 2×10⁶ | 272 | — |
| this repo | 5 | 10⁶ | — | 403 |
| this repo | 6 | 10⁶ | 91 | 240 |
| this repo | 9 | 4000 | 3 | 8 |

## Mixed: variable exponents

a<sup>A</sup> + b<sup>B</sup> = c<sup>C</sup> + d<sup>D</sup> with each exponent in 2..8 and bases ≤ 1000. No side is fixed to cubes.

| file | n |
|------|--:|
| [mixed_grid_M1000.csv](mixed_grid_M1000.csv) | 45436 |
| [mixed_grid_sigma_lt1.csv](mixed_grid_sigma_lt1.csv) | 2 |

Raw collisions were 96,332. The big file keeps one writing per identity: each term is reduced to the least exponent in 2..8, then drops rows that become the same shape on both sides (a² + b² = c² + d⁴ is just two squares). gcd = 1 and no single term equal to a term on the other side.

What σ is, and the two σ < 1 identities, are in [mixedgrid.md](../mixedgrid.md).
