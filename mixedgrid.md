# Mixed grid: \(a^A + b^B = c^C + d^D\)

Each exponent is in \(2..8\) and bases are \(\le 1000\). No side is fixed to cubes.

| file | n |
|------|--:|
| `mixed_grid_M1000.csv` | 45436 |
| `mixed_grid_sigma_lt1.csv` | 2 |

Raw collisions were 96,332. The big file keeps one writing per identity: each term is reduced to the least exponent in \(2..8\), then drops rows that become the same shape on both sides (\(a^2+b^2 = c^2+d^4\) is just two squares). gcd=1 and no single term equal to a term on the other side.

## What σ is

\(\sigma = 1/A + 1/B + 1/C + 1/D\) is the sum of the **reciprocals of the four exponents**, not of the bases. It is the same density count as Wagstaff’s \(2/j + 2/k\).

A random integer of size about \(B\) is a sum of two \(e\)-th powers with probability about \(B^{2/e - 1}\). Four exponents collide when \(\sigma > 1\). So:

- **σ > 1** — expect many solutions (almost all 45,436 rows; the bulk is \(a^2+b^2 = c^2+d^3\), where \(\sigma = 11/6\)).
- **σ = 1** — borderline.
- **σ < 1** — expect finitely many.

Only two reduced identities in the \(M=1000\) box have \(\sigma < 1\) (both \(\sigma = 1/2 + 1/5 + 2/7 = 0.9857\ldots\)):

```
42² + 7⁵ = 3⁷ + 4⁷ = 18571
72² + 2⁷ = 5⁵ + 3⁷ = 5312
```
