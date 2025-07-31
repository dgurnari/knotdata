# Knot Polynomial Dataset Repository

This repository contains a collection of datasets for various knot invariants, including polynomial and homological data. Each dataset is stored in `.csv` format with coefficients or values organized by columns for ease of analysis and computational use.

## 📊 Included Invariants

| Invariant Type     | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Alexander**      | Classical knot invariant based on Seifert matrices.                        |
| **Jones**          | Polynomial invariant arising from a braid representation of knots.         |
| **Theta**          | (fill in exact meaning here).         |
| **HOMFLYPT**       | Two-variable polynomial generalizing both Alexander and Jones polynomials. |
| **Khovanov Homology** | A categorification of the Jones polynomial providing richer data.     |

## 📁 Dataset Format

Each dataset is provided as a `.csv` file. Each row typically corresponds to a knot, and columns represent:

- Knot identifier (e.g., `3_1`, `4_1`, `5_2`)
- Polynomial coefficients or homology ranks
- Additional scalar invariants (crossing number, alternating, signature, s invariant, etc.)

All datasets use the same knot identifier, following KnotScape's ordering for knots up to 16 crossings and Regina's ordering for 17 crossings knots.

Please refer to each subdirectory’s `README.md` for format-specific notes.

## 📦 Repository Structure

```
/<root>
├── data/
│   ├── Alexander/
│   ├── Jones/
│   ├── Theta/
│   ├── HOMLFYPT/
│   └── Khovanov/
├── README.md
├── LICENSE
└── utils/ (optional: scripts used for generating and parsing the data)
```

## 📚 References and Credits

TODO


## 📄 License

This project is licensed under the [MIT License](LICENSE).