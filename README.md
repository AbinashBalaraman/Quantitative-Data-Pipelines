# Quantitative-Data-Pipelines

End-to-end data science and financial engineering pipelines covering automated data extraction, comprehensive data cleansing, and unsupervised machine learning clustering for market and consumer segmentation.

## Overview

High-quality data is the foundational layer of any machine learning model. This repository demonstrates professional data engineering techniques applied to financial and quantitative datasets. The projects within span the entire data lifecycle: utilizing automated scrapers to pull raw ticker data from major financial APIs, systematically cleansing the data using Pandas, and ultimately applying K-Means clustering algorithms to derive actionable statistical insights. 

## Core Implementations

The repository is modularized by the stages of the data pipeline.

*   `DataCleaning/`
    *   **Functionality:** The Transformation layer.
    *   **Capabilities:** Extensive scripts focusing on imputing missing variables (NaNs), normalizing floating-point data, resolving strict typing errors, and preparing diverse `.csv` and `.xlsx` structures for ingestion by neural networks or statistical modules.
*   `clustering/`
    *   **Functionality:** The Analysis / Loading layer.
    *   **Capabilities:** Applies unsupervised Machine Learning—specifically the K-Means Clustering and HDBSCAN algorithms via Scikit-Learn. The module takes scrubbed datasets (such as customer metrics) and programmatically determines optimal centroids to establish highly defined data segments.

## Technology Stack

*   **Language:** Python 3.10+
*   **Data Processing:** `pandas`, `numpy`
*   **Machine Learning:** `scikit-learn`
*   **Visualization:** `matplotlib`, `seaborn`

## Prerequisites

1.  Python 3.10 or higher.
2.  Adequate memory allocation for processing larger Pandas DataFrames if executing locally.

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
    pip install -r requirements.txt
    ```

## Usage

Each module is designed to be executed independently. For example, to execute the data cleaning pipeline:

```bash
cd DataCleaning
jupyter notebook clean.ipynb
```

To execute the K-Means and HDBSCAN clustering models:

```bash
cd clustering/models
jupyter notebook KMeans.ipynb
```

*(Note: Ensure that any necessary input datasets are placed in the requisite `/data` directories as defined locally. Standardized datasets have been omitted from the remote repository under `.gitignore` protocols.)*

## License

Standard MIT License applies.
