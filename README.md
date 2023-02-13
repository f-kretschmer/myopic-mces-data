# Structure visualization via UMAP embedding of MCES distances

This repository contains datasets from the Paper [Small molecule machine learning: All models are
wrong, some may not even be helpful](https://doi) alongside Jupyter Notebooks for visualization of
MCES distances.

| file                               | description                                                                                |
|------------------------------------|--------------------------------------------------------------------------------------------|
| `biostructures.csv`                | Biomolecular structures (SMILES and InChI-key first block)                                 |
| `biostructures_20k.csv`            | Subsample of biomolecular structures used throughout the paper                             |
| `mces_distances.npz`               | Compressed numpy-object containing all computed MCES distances alongside SMILES            |
| `umap_df.csv`                      | Computed UMAP embeddings for various datasets                                              |
| `umap_embedding_biostructures.pkl` | `umap-learn` object allowing projection of new structures onto the computed UMAP embedding |

## Visualization

Visualization of precomputed UMAP embeddings as well as for new structures can be performed with the notebook [display_umap.ipynb](display_umap.ipynb).
To project MCES distances of a new dataset onto the existing UMAP embedding, use [umap_embedding.ipynb](umap_embedding.ipynb).

Python packages required are:
```
umap-learn
numba=0.53.1
pandas
numpy
plotly
rdkit
dash
jupyter-dash
```

A conda (or [mamba](https://github.com/mamba-org/mamba)) environment with all necessary packages installed can be created with
```bash
conda env create -f conda_env.yml
# to activate:
conda activate umap_mces
```
