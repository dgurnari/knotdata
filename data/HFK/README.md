# 🧬 Knot Floer Homology (HFK) Dataset

This dataset contains bigraded **knot Floer homology** (HFK) data for all prime knots up to 15 crossings, stored in `.csv` format. The information includes algebraic, geometric, and topological invariants derived from Heegaard Floer theory.

## 📄 File: `HFK_upto17.csv`

Each row corresponds to a knot and contains metadata along with its full bigraded homology.

### 🔢 Column Descriptions

| Column Name     | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `knot_id`        | Knot identifier                                                             |
| `L_space_knot`   | Boolean, `True` if the knot is an L-space knot                              |
| `epsilon`        | Ozsváth–Szabó–Rasmussen invariant (takes values in {-1, 0, 1})              |
| `fibered`        | Boolean, `True` if the knot is fibered                                      |
| `modulus`        | Mod 2 grading shift (usually 2)                                             |
| `nu`             | Concordance invariant `ν` from HFK                                          |
| `ranks`          | Bigraded homology ranks as a Python-style dictionary: `{(a, m): rank}` where `a` = Alexander grading, `m` = Maslov grading |
| `seifert_genus`  | The Seifert genus of the knot                                               |
| `tau`            | Concordance invariant `τ` (tau) from HFK                                    |
| `total_rank`     | Sum of all HFK ranks (dimension of the chain complex)                       |
| `signature`      | Knot signature (a classical knot invariant)                                 |


### 📦 Example Entry

```csv
knot_id,L_space_knot,epsilon,fibered,modulus,nu,ranks,seifert_genus,tau,total_rank,signature
05_1,True,1,True,2,2,"{(-2, -4): 1, (-1, -3): 1, (0, -2): 1, (1, -1): 1, (2, 0): 1}",2,2,5,-4
````

This represents the knot **5₁**, with:

* Total HFK rank: 5
* Fibered: Yes
* L-space knot: Yes
* τ = 2
* Full HFK support:

  $$
  \widehat{HFK}(K) = \bigoplus_{(a, m)} \mathbb{F}_2^{r_{a,m}} \text{ for } (a, m) \in \{(-2, -4), (-1, -3), \dots\}
  $$
