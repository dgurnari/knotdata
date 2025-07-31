# 🧬 Khovanov Homology Diagonals — Non-Alternating Knots up to 17 Crossings

This dataset catalogs the diagonals in the **(unreduced, integral) Khovanov homology** for all **non-alternating knots** with up to **17 crossings**. Alternating knots are excluded, as they are always *Khovanov-thin* — i.e., they lie on exactly two diagonals.

> 📊 **Focus**: Understanding the *width* and *diagonal spread* in Khovanov homology for complex (non-alternating) knots.

---

## 📁 File Contents

The dataset is stored in CSV format with the following columns:

| Column Name                          | Description                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| `knot_id`                            | Identifier of the knot (e.g. `08_19` for the 19th 8-crossing knot)         |
| `signature`                          | The classical knot signature (σ)                                           |
| `s_mod3`                             | Signature modulo 3                                                         |
| `Integral unreduced Khovanov homology` | Set of diagonals (i.e., δ-gradings) where the homology has nonzero rank     |
| `Torsion of order 2`                 | Set of diagonals that contain **Z/2Z** torsion                             |
| `Torsion of order 4`                 | Set of diagonals that contain **Z/4Z** torsion                             |
| `all diagonals`                      | Full set of diagonals with any nontrivial homology                         |
| `width`                              | Number of distinct diagonals (i.e., Khovanov **thickness**)                |

---

## 📐 Diagonal Convention

- A *diagonal* in Khovanov homology refers to lines of constant `δ = q - 2h`, where `q` is the quantum grading and `h` is the homological grading.
- The set in `Integral unreduced Khovanov homology` lists the `δ`-values with nontrivial homology groups.

---

## 📌 Notes

- Alternating knots are always **thin** (i.e., those supported on two diagonals) therefore they are omitted by design.
- **Torsion structure** is included for detecting richer behavior beyond rank.
- All homology is computed with **integral coefficients**.
- Data is consistent with Bar-Natan’s and KnotAtlas conventions.

---

## 📎 Example

```csv
knot_id,signature,s_mod3,Integral unreduced Khovanov homology,Torsion of order 2,Torsion of order 4,all diagonals,width
08_19,6,0,"{3, 5, 7}",{5},set(),"{3, 5, 7}",3
````

This tells us that `8₁₉` has homology supported on diagonals `{3, 5, 7}`, with `Z/2Z` torsion on the 5-diagonal, and a total width of 3.