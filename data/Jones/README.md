# Jones Polynomial Data 
This dataset contains Jones polynomial information for all prime knots with up to 17 crossings, including both knots and their mirror images.
## Contents

Each row in the dataset represents a unique knot (or its mirror) and includes:

* `knot_id`: Knot identifier, e.g., `07_7`, or `10_123!` for mirrors.
* `number_of_crossings`: Number of crossings in the knot diagram.
* `table_number`: Knot index in the standard tables for its crossing number.
* `is_alternating`: 1 if the knot is alternating, 0 otherwise.
* `signature`: The signature of the knot (a classical knot invariant).
* `minimum_exponent`, `maximum_exponent`: The lowest and highest exponents of the Jones polynomial.
* `J{n}`: Coefficients of the Jones polynomial at $q^n$, for $n \in [-25, 25]$. Zero-padding is used where coefficients are not present.

## Format

The dataset is a CSV file with columns:

```
knot_id, number_of_crossings, table_number, is_alternating, signature, minimum_exponent, maximum_exponent, J-25, ..., J0, ..., J25
```

### Polynomial Representation

The Jones polynomial for a knot is given in the form:

$$
V_K(q) = \sum_{i = \text{min}}^{\text{max}} J_i \cdot q^i
$$

Where:

* `J{i}` is the coefficient of $q^i$
* `minimum_exponent` and `maximum_exponent` specify the support range
* Coefficients outside the range are set to zero

## Notes

* Mirror knots are denoted with an exclamation mark (`!`) suffix (e.g., `11_5!`).
* The dataset includes the Jones polynomial for the **mirror image** computed directly via inversion:

  $$
  V_{K^!}(q) = V_K(q^{-1})
  $$