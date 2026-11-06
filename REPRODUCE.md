# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py tg <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 3,605 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
ee3a200d7e8105f56b3a8d54e5e1a8ff351cd27008edd5242ae3ba88b47d0cd8 *tg_anwaltskommission.parquet
ed8007db125674be251e43e549bf611f516400ec2eb8bc74ee70acf924c4c044 *tg_gerichte.parquet
1557cf992e0071b35789168608ca2cca7bea027463174d8ec461f323422699b1 *tg_obergericht.parquet
```
