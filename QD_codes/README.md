This folder contains the parity-check matrices and the meta-check matrices of the designed quasi-dyadic (QD) codes.

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

| Paper label | Directory | H shape | M_X shape | M_Z shape |
|---|---|---:|---:|---:|
| QD,1 [[64,18,8]] | `QD_64_18` | 82 x 128 | 9 x 32 | 9 x 32 |
| QD,2 [[64,12,8]] | `QD_64_12` | 172 x 176 | 30 x 56 | 30 x 56 |
| QD,3 [[128,36,8]] | `QD_128_36` | 164 x 256 | 18 x 64 | 18 x 64 |
| QD,4 [[128,24,8]] | `QD_128_24` | 344 x 352 | 60 x 112 | 60 x 112 |
