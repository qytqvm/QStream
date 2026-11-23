# QStream Benchmarks

QStream is a multi-codec Smart Builder by [Qytte](https://qytte.com/qstream). It learns the shape of your data from a sample and builds a Smart Profile. The profile makes the compressor you already use smaller, with no rebuild.

This repository holds **benchmark data only**. It contains no QStream source code.

## Results: 100 cloud event files (~5 KB each)

The profile was trained on 80 separate files that are not part of the test set. The shared profile is counted once in the batch total, and every file was restored byte for byte.

| Compressor | Without profile | With QStream profile |
|---|---|---|
| QSwift Turbo | 69.5% | **85.6%** |
| QSwift Maximus | 71.1% | **88.2%** |

Profile results for Zstandard, Brotli, LZ4, zlib/gzip and Snappy will be added once they are measured on the same files.

## What's in this repo

- `results/` – CSV and Markdown tables
- `images/` – benchmark tables and graphs
- `METHODOLOGY.md` – how the tests were run

## Supported compressors

Zstandard · Brotli · LZ4 · zlib/gzip · Snappy · QSwift

## Learn more

- Product: https://qytte.com/qstream
- Book a profile trial: https://qytte.com/contact

© 2026 Qytte. QStream is proprietary. These benchmark files are shared for information only.

