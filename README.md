# Medley Interlisp Gabriel Benchmarks

## About

This repository runs Gabriel benchmark suites in Medley Interlisp.

The benchmark set comes from the work documented by Richard P. Gabriel in [*Performance and Evaluation of Lisp Systems*](https://www.dreamsongs.com/Files/Timrep.pdf).

## Quick Start

### 0. Clone the repository

```bash
git clone https://github.com/interlisp/new-gabriel.git
cd gabriel
```

### 1. Make the runner executable

```bash
chmod +x do-bench.sh
```

### 2. Set MEDLEYDIR (required before first run)

Set only `MEDLEYDIR` to your Medley install path:

```bash
export MEDLEYDIR="/absolute/path/to/medley"
```

### 3. Run a benchmark suite

The `do-bench.sh` script expects three arguments:

- bench-name - a human-readable name, e.g., "First Benchmark"
- bench-file - the name of the benchmark file, normally one of `BENCH-1`, ..., `BENCH-5`
- bench-fn - the name of the benchmark function, normally identical to the name of the file

For example,

```bash
./do-bench.sh "TAK, ARITH, IO Benchmarks" BENCH-1 BENCH-1
```

## What Each Suite Runs

- `BENCH-1`: TAK, ARITH, IO
- `BENCH-2`: AREFY (and IO support load)
- `BENCH-3`: CONSY
- `BENCH-4`: POLY
- `BENCH-5`: MISC (with IO and MISC support loads)

## Results

Each run writes output under `Results/`:

- `Results/BENCH-1/`
- `Results/BENCH-2/`
- `Results/BENCH-3/`
- `Results/BENCH-4/`
- `Results/BENCH-5/`

