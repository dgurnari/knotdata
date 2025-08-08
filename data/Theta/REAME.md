# 🧮 Theta Polynomial Dataset

This dataset contains Theta polynomials for all prime knots up to 15 crossings, stored in a structured `.csv` format.

## 📄 File: `theta_upto15.csv`

Each row represents one knot, with associated metadata and polynomial coefficients.

### 🔢 Column Descriptions

| Column Name           | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `knot_id`              | Knot identifier   |
| `number_of_crossings` | Minimal crossing number of the knot                                         |
| `table_number`         | Knot index within the set of knots with that crossing number               |
| `is_alternating`       | Boolean (1 or 0), indicating whether the knot is alternating                |
| `signature`            | The signature of the knot                                                   |
| `s_invariant`            | The Rasmussen invariant of the knot                                                |
| `T1[x]_T2[y]`             | Coefficients of the polynomial in degree `x` and `y` for the variables $T_1$ and $T_2$, respectively |
