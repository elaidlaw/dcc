# Definitely Not From Project Euler

A multiplicative conguential pseudo-random number generator is a sequence X
parameterized by s, a, and d, defined X<sub>i</sub> = s * a^i mod d. For
example, if s = 3, a = 15, and d = 99, X<sub>0..4</sub> = (3, 45, 81, 27, 9).

The matrix A ∈ Z<sup>m×n</sup> is defined A<sub>ij</sub> = X<sub>in + j</sub>.
If  s = 3, a = 15, d = 99, m = 4, and n = 4, then

```
A = 
|36  45  81  *27*|
| 9  36  45  *81*|
|27   9  36  *45*|
|81  27   9  *36*|
```

This matrix has an adjacent collection of four numbers that multiply to 3542940,
which is the largest such product.

Return the greatest product of four adjacent numbers in the same direction (up,
down, left, right, or diagonally) in A, given the tuple (s, a, d, m, n). Your
run function should literally take a Python tuple.
