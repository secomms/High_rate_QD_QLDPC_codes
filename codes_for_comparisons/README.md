This folder contains the parity-check matrices and the meta-check matrices of the CSS codes used for comparison against the proposed QD codes.

The code instances are from the following code families:

  - Hypergraph Product (HP) codes.

  - Bicycle (Bic) codes.

  - Quasi-Cyclic (QC) codes.
  
  - Generalized Bicycle (GB) codes.

  - Bivariate Bicycle (BB) codes.

  - Dyadic CAMEL codes.

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
header row. 
For HP and Bic codes, both meta-check matrices have zero rows,
so their `Mx_meta.csv` and `Mz_meta.csv` files are intentionally empty.

| Paper label | Directory | H shape | M_X shape | M_Z shape |
|---|---|---:|---:|---:|
| HP1 [[65,9,4]] | `HP_65_9` | 56 x 121 | 0 x 28 | 0 x 28 |
| Bic1 [[64,12,6]] | `Bic_64_12` | ? x ? | 0 x 26 | 0 x 26 |
| Bic2 [[64,18,2]] | `Bic_64_18` | ? x ? | 0 x 23 | 0 x 23 |
| GB1 [[48,6,8]] | `GB_48_6` | 54 x 96 | 3 x 24 | 3 x 24 |
| BB1 [[72,12,6]] | `BB_72_12` | 84 x 144 | 6 x 36 | 6 x 36 |
| HP2 [[241,121,3]] | `HP_241_121` | 120 x 361 | 0 x 60 | 0 x 60 |
| Bic3 [[256,96,8]] | `Bic_256_96` | 160 x 416 | 0 x 80 | 0 x 80 |
| Bic4 [[256,130,2]] | `Bic_256_130` | 126 x 382 | 0 x 63 | 0 x 63 |
| QC [[272,142,8]] | `QC_272_142` | 142 x 408 | 3 x 68 | 3 x 68 |
| CPM [[276,98,14]] | `GB_276_98` | 190 x 460 | 3 x 92 | 3 x 92 |
| BB2 [[288,12,18]] | `BB_288_12` | 300 x 576 | 6 x 144 | 6 x 144 |
| D0 [[65,27,4]] | `D0_65_27` | 58 x 113| 5 x 24 | 5 x 24 |
| D1 [[257,121,10]] | `D1_257_121` | 312 x 481 | 44 x 112 | 44 x 112 |



