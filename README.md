# FlakyLens Reproduction Study and Research Directions

The repository is organized into two separate components:

1. **FlakyLens Reproduction** – reproduction experiments, artifact files, and experimental results.
2. **FlTools** – the separate FlakyLens tooling(IDoFT, iDFlakies, NonDex) and its associated documentation.

---

## 1. FlakyLens Reproduction

The `FlakyLens/` folder contain the code, documentation, and outputs for the reproduction experiments. The detailed results and discussion of the three runs are provided in the accompanying PDF. Run 2.1 and Run 2.2 are split into two notebooks because the experiment was executed separately for Fold 2 and Folds 1, 3, and 4 due to GPU/runtime constraints.

### Artifact Contents

| File | Description |
|---|---|
| [Run 1](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FlakyLens/1.%20FlakyLensRQ1WithoutSmote.ipynb) | Code |
| [Run 2.1](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FlakyLens/2.1%20FlakyLensRQ1WithSmoteFold2.ipynb) | Code |
| [Run 2.2](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FlakyLens/2.2%20FlakyLensRQ1WithSmoteFold134.ipynb) | Code |
| [Run 3](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FlakyLens/3.FlakyLensWithSavedProjectWeight.ipynb) | Code |
| [Analysis Report](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FlakyLens/FlakyLens_Reproduction_Study_and_Research_Directions.pdf) | PDF |
|[Src & Dataset](https://drive.google.com/drive/folders/1U8D2WOrPuQxmInqzVgH4YpPhXpoFzi8d?usp=sharing)|---|
### Experimental Results

The three experimental runs are summarized below.

| Experimental Run | Run Description | Async Wait | Concurrency | Time | Unordered Collections | Test Order Dependency | Non-flaky | Macro F1-score Avg. |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| **Run 1** | Paper methodology, without SMOTE, seed 42 | 58.25 | 20.00 | 74.29 | 54.55 | 34.11 | 99.95 | **56.86** |
| **Run 2** | Released implementation with SMOTE, seed 14 | 55.24 | 24.56 | 63.49 | 76.54 | 58.82 | 99.94 | **63.10** |
| **Run 3** | Provided checkpoints evaluated on corresponding project splits | 86.92 | 82.79 | 89.29 | 90.63 | 85.12 | 100.00 | **89.98** |

Detailed experimental settings, observations, and analysis are provided in the accompanying PDF.

### Configuration

- **Platform:** Kaggle GPU
- **Model:** Microsoft CodeBERT

---

## 2. FlTools

`FLTools` contains the FlakyLens tooling and a separate PDF documenting the work carried out to analyze IDoFT, explore the tools, and identify the limitations observed during the study.

### FlTools Structure

- 📁 **[FlTools](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/tree/main/FLTools)**
  - 💻 **[Code](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FLTools/FLTools.ipynb)** — FlakyLens tooling/code
  - 📄 **[PDF](https://github.com/ZaimaSartajTaheri/PhD_Research_Directions_and_FlakyLens_Reproduction_Study/blob/main/FLTools/Flaky_Test_Tools_Exploration.pdf)** — Documentation of the work carried out to analyze IDoFT, explore the tools, and identify the limitations observed during the study.
