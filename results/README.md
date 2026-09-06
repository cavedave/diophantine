# results

Solution tables only. No search code.

| file | equation | bound | n |
|------|----------|-------|--:|
| `k4_x3y3_eq_a4b4_M1e7.csv` | X^3 + Y^3 = A^4 + B^4 | A,B <= 10^7, sum, primitive | 7629 |
| `k5_x3y3_eq_c5d5_M1e6.csv` | X^3 + Y^3 = C^5 + D^5 | C,D <= 10^6, sum, primitive | 216 |
| `k6_x3y3_eq_c6d6_M5e5.csv` | X^3 + Y^3 = C^6 + D^6 | C,D <= 5e5, sum, primitive | 69 |
| `k7_x3minusy3_eq_c7d7.csv` | X^3 - Y^3 = C^7 + D^7 | one recorded instance | 1 |
| `mixed_grid_M1000.csv` | a^A + b^B = c^C + d^D | bases <= 1000, exponents 2..8 | 96332 |

k=4,5,6: gcd of the four bases is 1; parametric trivial families excluded.
Mixed grid: gcd 1 and no term equal to a term on the other side.
