# Quantitative-Data-Pipelines

Data engineering and unsupervised machine learning pipelines applied to real-world datasets. The repository covers the full preparation and modeling lifecycle: raw data cleaning and normalization, followed by multi-algorithm clustering experiments including K-Means, HDBSCAN, DBSCAN, Gaussian Mixture Models, and hierarchical methods.

## Overview

High-quality, well-shaped data is a prerequisite for any reliable ML model. This repository demonstrates professional data preprocessing and exploratory clustering analysis using a real car sales dataset. The `DataCleaning` module prepares the raw dataset for modeling through systematic imputation and normalization. The `clustering` module then applies and compares multiple unsupervised learning algorithms to identify natural groupings — work performed during a Data Science internship at Kestone Integrated Marketing Services.

## Modules

### `DataCleaning/`

A Jupyter notebook (`clean.ipynb`) performing systematic data preparation on the `Car Sell Dataset.csv` (approximately 11MB of car sales records). Operations include:

*   Missing value imputation using median and mode strategies.
*   Outlier detection and handling via IQR-based filtering.
*   Categorical encoding and feature type normalization.
*   DataFrame reshaping and preparation for clustering input.

### `clustering/`

A structured directory containing the full suite of clustering experiments run on the cleaned dataset.

**`clustering/models/`** — The primary model notebooks:

| Notebook | Algorithm | Description |
|---|---|---|
| `KMeans.ipynb` | K-Means | Segment data using elbow method and silhouette analysis to find optimal cluster count |
| `optimal_kmeans.ipynb` | K-Means (optimized) | Refines the K-Means run with scaled features and centroid visualization |
| `HDBSC.ipynb` | HDBSCAN | Hierarchical density-based clustering for arbitrarily shaped clusters |
| `HDBScan_PRedict.ipynb` | HDBSCAN Prediction | Applies a trained HDBSCAN model to new data points |
| `DB_scan.ipynb` | DBSCAN | Density-based spatial clustering with noise identification |
| `hirarch.ipynb` | Hierarchical (agglomerative) | Ward linkage dendrogram visualization and flat cluster extraction |
| `gauss.ipynb` | Gaussian Mixture Model | Probabilistic soft-assignment clustering with BIC model selection |
| `embed_cluster.ipynb` | Embedding + Clustering | Applies dimensionality reduction before clustering for high-dimensional features |
| `rew_data_embeddding.ipynb` | Raw Embedding | Explores embedding representations of raw features |
| `ldx.ipynb` | LDA | Latent Dirichlet Allocation exploration for topic-based grouping |
| `models_for_cluster.ipynb` | Model comparison | Side-by-side comparison of algorithm outputs |
| `alldata.ipynb` | Full dataset run | Clustering experiment across the complete unpruned dataset |

**`clustering/input_data/`** — Holds preprocessed dataset versions ready for model input.

**`clustering/output/`** — Stores cluster label outputs and evaluation metric logs.

## Technology Stack

*   **Language:** Python 3.10+
*   **Environment:** Jupyter Notebook
*   **Data Processing:** `pandas`, `numpy`
*   **Machine Learning:** `scikit-learn` (K-Means, DBSCAN, Agglomerative, GMM), `hdbscan`
*   **Visualization:** `matplotlib`, `seaborn`

## Prerequisites

1.  Python 3.10 or higher.
2.  Jupyter Notebook or JupyterLab installed.
3.  Sufficient RAM for processing the full car sales dataset (recommend 8GB+).

## Setup and Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/AbinashBalaraman/Quantitative-Data-Pipelines.git
    cd Quantitative-Data-Pipelines
    ```

2.  Initialize and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  Install dependencies:
    ```bash
    pip install pandas numpy scikit-learn hdbscan matplotlib seaborn jupyterlab
    ```

## Usage

Start by running the data cleaning notebook to prepare the dataset:

```bash
cd DataCleaning
jupyter notebook clean.ipynb
```

Then run any clustering model from the models directory:

```bash
cd clustering/models
jupyter notebook KMeans.ipynb
# or any other model notebook
```

Input datasets must be placed in `clustering/input_data/` after the cleaning step. Cluster label outputs are written to `clustering/output/`.

## License

Standard MIT License applies.
