# Even Khovanov Homology Coefficients Dataset

This CSV file contains detailed data on the **even Khovanov homology** of a large collection of knots, with homology groups presented as graded Betti numbers indexed by quantum degree `q` and homological degree `t`.

The same data is also available as a sparse matrix for faster import and more efficient memory usage. You can find it in the file named `even_KH_upto17.pkl`. Using this format can significantly speed up loading times.

## 📁 File Structure

Each **row** in the CSV corresponds to an individual knot.
Each **column** contains either metadata about the knot or a coefficient of its even Khovanov homology.

---

## 🔢 Columns Overview

### 🔹 Knot Metadata

* `knot_id`: A unique identifier for the knot (e.g. `"11n34"`).
* `number_of_crossings`: Integer count of the knot's minimal crossing number.
* `is_alternating`: Boolean indicator (`True` or `False`) of whether the knot is alternating.
* `s_invariant`: The Rasmussen invariant of the knot, a slice genus bound from Khovanov homology.
* `signature`: The classical knot signature.

### 🔹 Khovanov Homology Coefficients

These columns are named using the format:

```
F_q{q}_t{t}
```

where:

* `q` is the **quantum grading**
* `t` is the **homological grading**
* `F_` indicates that these are coefficients (Betti numbers) in the **even Khovanov homology**
* `T2_` and `T4_` indicate $Z_2$ and $Z_4$ torsion coefficients, respectively.

For example:

* `F_q-3_t2` is the dimension of the homology group in grading (q = -3, t = 2)
