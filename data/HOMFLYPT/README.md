# HOMFLY-PT Polynomial Data

This dataset contains HOMFLY-PT polynomial information for prime knots with up to 15 crossings, including both knots and their mirror images. It includes detailed graded dimensions of the homological invariants extracted from the HOMFLY-PT homology.

## Contents

* `knot_id`: Unique identifier for each knot, including mirrors (e.g., `09_42!` for the mirror of `09_42`).
* `number_of_crossings`: The number of crossings in the knot diagram.
* `table_number`: Table index within its crossing number.
* `is_alternating`: 1 if the knot is alternating, 0 otherwise.
* `signature`: Knot signature invariant.
* `s_invariant`: Rasmussen’s s-invariant.
* `a{A}_z{B}`: The dimension of the homology in \$(a = A, q = B)\$ bigrading, following the structure of the HOMFLY-PT homology. Nonzero entries indicate the presence of a generator in that bidegree.

## Format

CSV file with one row per knot or mirror knot, and columns in the format:

```
knot_id, number_of_crossings, table_number, is_alternating, signature, s_invariant,
a18_z0, a18_z2, ..., a-18_z14
```

### Grading Notation

* `a{A}_z{B}` corresponds to the homological dimension in bigrading `(a = A, q = B)`.
* The `a`-grading ranges from `+18` to `-18`.
* The `z`-grading ranges from `0` to `14`, corresponding to the quantum grading used in triply-graded HOMFLY-PT homology.

## Notes

* Mirror images are denoted by an exclamation mark (`!`) following the knot ID (e.g., `12_341!`).
* Many entries may contain mostly zeros, indicating the sparse nature of homological dimensions at high gradings.