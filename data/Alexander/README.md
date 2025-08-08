# 🧮 Alexander Polynomial Dataset

This dataset contains Alexander polynomials for all prime knots up to 17 crossings, stored in a structured `.csv` format.

## 📄 File: `alexander_upto17.csv`

Each row represents one knot, with associated metadata and polynomial coefficients.

### 🔢 Column Descriptions

| Column Name           | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `knot_id`              | Knot identifier |
| `number_of_crossings` | Minimal crossing number of the knot                                         |
| `table_number`         | Knot index within the set of knots with that crossing number               |
| `is_alternating`       | Boolean (1 or 0), indicating whether the knot is alternating                |
| `signature`            | The signature of the knot                                                   |
| `minimum_exponent`     | Lowest exponent of the variable `t` in the Alexander polynomial             |
| `maximum_exponent`     | Highest exponent of `t` in the polynomial                                   |
| `A0`–`A16`             | Coefficients of the polynomial, aligned to degrees from `minimum_exponent` to `maximum_exponent` (zero-padded) |

### 🧠 Notes on Polynomial Format

- The Alexander polynomial is expressed as a Laurent polynomial in `t`, but in this dataset it's encoded as a standard vector of coefficients for uniform CSV formatting.
- The nonzero coefficients always begin at the index corresponding to `minimum_exponent` and end at `maximum_exponent`.

### 📦 Example

```csv
knot_id,number_of_crossings,table_number,is_alternating,signature,minimum_exponent,maximum_exponent,A0,A1,A2,A3,A4,A5,A6,A7,A8,A9,A10,A11,A12,A13,A14,A15,A16
05_1,5,1,1,4,2,7,0,0,0,0,0,0,1,-1,1,-1,1,0,0,0,0,0,0
````

This represents the Alexander polynomial of knot **5₁**:

$$
\Delta(t) = t^2 - t^3 + t^4 - t^5 + t^6
$$
