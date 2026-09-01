This folder contains the parity-check matrices of the CSS codes used for comparison against the proposed QD codes.

The code instances are from the following code families:

  - Hypergraph Product (HP) codes.

  - Quasi-Cyclic (QC) codes.
  
  - Generalized Bicycle (GB) codes.

  - Bivariate Bicycle (BB) codes.

Each code has its own subdirectory with three files:

- `CODE_H_extended_quaternary.csv`: the full joint-decoding matrix

  ```text
  [ omega H_X       I_X       0  ]
  [     0           L_X       0  ]
  [ omega_bar H_Z    0       I_Z ]
  [     0            0       L_Z ]
  ```

  where `L_X=M_X` and `L_Z=M_Z`. The first column block has width `n`; the
  other blocks have widths `m_X` and `m_Z`. Entries use the GF(4) integer
  encoding `0,1,2,3`, with `omega H_X` encoded by `1`, `omega_bar H_Z` by
  `2`, and the binary identity/meta blocks embedded using `0,1`.
- `CODE_Mx_meta.csv`: the binary X-syndrome meta-check matrix `M_X`, satisfying
  `M_X H_X = 0` over GF(2).
- `CODE_Mz_meta.csv`: the binary Z-syndrome meta-check matrix `M_Z`, satisfying
  `M_Z H_Z = 0` over GF(2).

The CSV files contain only comma-separated integer matrix entries and no
header row. For HP_65_9 and HP_125_25, both meta-check matrices have zero rows,
so their `Mx_meta.csv` and `Mz_meta.csv` files are intentionally empty.

| Paper label | Directory | H shape | M_X shape | M_Z shape |
|---|---|---:|---:|---:|
| HP,1 [[65,9,4]] | `HP_65_9` | 56 x 121 | 0 x 28 | 0 x 28 |
| GB,1 [[48,6,8]] | `GB_48_6` | 54 x 96 | 3 x 24 | 3 x 24 |
| BB,1 [[72,12,6]] | `BB_72_12` | 84 x 144 | 6 x 36 | 6 x 36 |
| HP,2 [[125,25,4]] | `HP_125_25` | 100 x 225 | 0 x 50 | 0 x 50 |
| QC [[136,38,6]] | `QC_136_38` | 106 x 238 | 2 x 51 | 2 x 51 |
| GB,2 [[126,28,8]] | `GB_126_28` | 154 x 252 | 14 x 63 | 14 x 63 |
| BB,2 [[108,8,10]] | `BB_108_8` | 116 x 216 | 4 x 54 | 4 x 54 |
| BB,3 [[144,12,12]] | `BB_144_12` | 156 x 288 | 6 x 72 | 6 x 72 |
