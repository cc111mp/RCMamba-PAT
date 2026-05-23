# Data

Expected dataset layout:

```bash
data/
|-- train/
|   |-- input/
|   `-- target/
|-- val/
|   |-- input/
|   `-- target/
`-- test/
    |-- input/
    `-- target/
```

Sparse inputs correspond to 16, 32, or 64 projection reconstructions. Targets correspond to dense-view reconstructions.

Large datasets should not be committed to this repository.

