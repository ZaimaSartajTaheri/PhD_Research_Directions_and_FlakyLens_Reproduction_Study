# FlakyLens Reproduction Study and Research Directions

This repository contains my reproduction study of **FlakyLens** and the research directions developed from the reproduction and the limitations identified during the study.

The repository is organized into two separate components:

1. **FlakyLens Reproduction** – reproduction experiments, artifact files, and experimental results.
2. **FlTools** – the separate FlakyLens tooling and its associated documentation.

---

## 1. FlakyLens Reproduction

The `artifact/` folder contains the files used for the FlakyLens reproduction experiments.

### Artifact Contents

| File | Description |
|---|---|
| [Code File 1](./artifact/FILE_1) | Reproduction code |
| [Code File 2](./artifact/FILE_2) | Reproduction code |
| [Code File 3](./artifact/FILE_3) | Reproduction code |
| [Code File 4](./artifact/FILE_4) | Reproduction code |
| [Artifact PDF](./artifact/ARTIFACT_PDF) | Artifact documentation |
| [Result Table 1](./artifact/RESULT_1) | Experimental result |
| [Result Table 2](./artifact/RESULT_2) | Experimental result |
| [Result Table 3](./artifact/RESULT_3) | Experimental result |

### Experimental Results

The three experimental runs are summarized below.

| Experimental Run | Run Description | Async Wait | Concurrency | Time | Unordered Collections | Test Order Dependency | Non-flaky | Macro Avg. |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| **Run 1** | Paper methodology, without SMOTE, seed 42 | 58.25 | 20.00 | 74.29 | 54.55 | 34.11 | 99.95 | **56.86** |
| **Run 2** | Released implementation with SMOTE, seed 14 | 55.24 | 24.56 | 63.49 | 76.54 | 58.82 | 99.94 | **63.10** |
| **Run 3** | Provided checkpoints evaluated on corresponding project splits | 86.92 | 82.79 | 89.29 | 90.63 | 85.12 | 100.00 | **89.98** |

Detailed experimental settings, observations, and analysis are provided in the accompanying PDF.

### Configuration

- **Platform:** Kaggle GPU
- **Model:** Microsoft CodeBERT
- **Cross-validation:** Project-wise 4-fold
- **Maximum sequence length:** 512
- **Batch size:** 8
- **Learning rate:** 1e-5
- **Weight decay:** 0.01
- **Dropout:** 0.30
- **Focal loss gamma:** 2
- **Maximum epochs:** 30
- **Early stopping patience:** 10
- **Gradient clipping:** 1.0

### Reproduction Files

The files in `artifact/` contain the code, documentation, and outputs for the reproduction experiments. The detailed results and discussion of the three runs are provided in the accompanying PDF.

---

## 2. FlTools

`FlTools/` is a **separate component from the FlakyLens reproduction**.

It contains the FlakyLens tooling and a separate PDF documenting the work carried out using the tooling and the limitations identified during the study.

### FlTools Structure

```text
FlTools/
├── [FlTools Code File]
└── [FlTools PDF]
