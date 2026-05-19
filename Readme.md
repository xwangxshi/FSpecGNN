# Full-Spectrum Graph Neural Networks

This repository contains the official code for the paper: 

Full-Spectrum Graph Neural Networks: Expressive and Scalable (https://arxiv.org/abs/2605.05759)

## Environment

Create the conda environment from the provided file:

```bash
conda env create -f FSpecGNN.yml
conda activate FSpecGNN
```

If your local conda environment name differs, activate the environment you created before running the experiments.

## Repository Structure

```text
FSpecGNN/
├── FSpecGNN.yml
├── Heterophily/
│   ├── data/
│   ├── small/
│   └── large/
└── Hom-Cycle-count/
```

- `Heterophily/`: node classification experiments on heterophilic benchmarks.
- `Heterophily/small/`: Texas, Wisconsin, Chameleon, and Squirrel.
- `Heterophily/large/`: Roman-empire, Minesweeper, Tolokers, and Questions.
- `Heterophily/data/`: datasets used by the heterophily experiments.
- `Hom-Cycle-count/`: expressivity experiments based on homomorphism/cycle counting.

## Reproducing Heterophily Results

Small heterophilic datasets:

```bash
cd Heterophily/small
```

The best hyperparameters and reproduction commands are listed in:

```text
Heterophily/small/reproduce.md
```

Large heterophilic datasets:

```bash
cd Heterophily/large
```

The best hyperparameters and reproduction commands are listed in:

```text
Heterophily/large/reproduce.md
```

Each command calls `train.py` with the model, dataset, and hyperparameters used to reproduce the reported results.

## Reproducing Expressivity Results

Go to the expressivity experiment directory:

```bash
cd Hom-Cycle-count
```

Follow the instructions in:

```text
Hom-Cycle-count/README.md
```

Outputs are written to `Hom-Cycle-count/result.count/`.

## Data

The heterophily datasets used by the provided scripts are stored under:

```text
Heterophily/data/
```

Please see `Heterophily/data/Readme` for dataset notes.
