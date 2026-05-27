# Single Cell RNA-seq Analysis Pipeline

This repository contains beginner-friendly notebooks for single-cell RNA sequencing (scRNA-seq) analysis using Python-based tools such as Scanpy, scVelo, CellTypist, and related packages. The notebooks cover core stages of a single-cell workflow, including preprocessing, quality control, clustering, visualization, cell type annotation, and trajectory inference.

The project is designed as a practical learning resource for students, researchers, and anyone interested in computational biology and transcriptomics.

---

# Repository Structure

## Files

### `Single_cell_tutorial.ipynb`

A foundational notebook introducing single-cell RNA-seq analysis with Scanpy.

Topics covered include:

* Installation of required Python packages
* Loading 10x Genomics datasets
* Understanding AnnData objects
* Exploring metadata and gene expression matrices
* Quality control concepts
* Data preprocessing
* Normalization and scaling
* Dimensionality reduction
* Clustering cells
* Visualizing cell populations

This notebook serves as an introduction to the typical scRNA-seq workflow.

---

### `Trajectory_analysis.ipynb`

A more advanced notebook focused on trajectory and pseudotime analysis.

Topics covered include:

* Loading single-cell datasets
* RNA velocity analysis using scVelo
* Trajectory inference
* Pseudotime ordering
* Cell fate transitions
* Cell type annotation using CellTypist
* Downstream biological interpretation

This notebook is useful for studying dynamic cellular processes such as differentiation, development, immune activation, and disease progression.

---

# What is Single-Cell RNA Sequencing?

Single-cell RNA sequencing (scRNA-seq) is a technology used to measure gene expression at the level of individual cells rather than bulk tissue.

Instead of averaging signals across thousands or millions of cells, scRNA-seq allows researchers to:

* Identify different cell types
* Detect rare populations of cells
* Study cellular heterogeneity
* Understand developmental pathways
* Track cell state transitions
* Explore disease mechanisms

It is widely used in cancer biology, immunology, developmental biology, neuroscience, regenerative medicine, and many other fields.

---

# Tools and Libraries Used

## Core Libraries

### Scanpy

entity["software","Scanpy","single-cell analysis toolkit"] is one of the most widely used Python frameworks for analyzing single-cell transcriptomics data.

Main uses:

* Data preprocessing
* Quality control
* Clustering
* Visualization
* Differential expression analysis
* Integration with other single-cell tools

Official documentation:

urlScanpy Documentation[https://scanpy.readthedocs.io/en/stable/](https://scanpy.readthedocs.io/en/stable/)

---

### scVelo

entity["software","scVelo","RNA velocity analysis toolkit"] is used for RNA velocity analysis.

RNA velocity estimates the future transcriptional state of individual cells by comparing spliced and unspliced RNA counts.

Main uses:

* Trajectory analysis
* Developmental dynamics
* Cell fate prediction
* Temporal ordering of cells

Official documentation:

urlscVelo Documentation[https://scvelo.readthedocs.io/](https://scvelo.readthedocs.io/)

---

### CellTypist

entity["software","CellTypist","automatic cell type annotation tool"] is used for automated cell type annotation.

It predicts likely cell identities using pretrained immune and tissue reference models.

Official documentation:

urlCellTypist Documentation[https://celltypist.readthedocs.io/en/latest/](https://celltypist.readthedocs.io/en/latest/)

---

### AnnData

entity["software","AnnData","annotated data structure for single-cell omics"] is the data structure used internally by Scanpy.

It stores:

* Gene expression matrices
* Cell metadata
* Gene metadata
* Embeddings and clustering results
* Additional annotations

Official documentation:

urlAnnData Documentation[https://anndata.readthedocs.io/en/latest/](https://anndata.readthedocs.io/en/latest/)

---

# Typical Workflow in This Repository

## 1. Data Loading

The notebooks demonstrate how to load 10x Genomics datasets into Python using Scanpy.

Common formats include:

* `.h5`
* `.mtx`
* compressed matrix files

---

## 2. Quality Control

Quality control removes low-quality cells and technical noise.

Typical metrics include:

* Number of detected genes per cell
* Total counts per cell
* Percentage of mitochondrial genes

Cells with poor-quality signals are filtered before downstream analysis.

---

## 3. Normalization

Normalization adjusts for differences in sequencing depth between cells.

This makes gene expression values comparable across the dataset.

---

## 4. Feature Selection

Highly variable genes are selected because they contain the strongest biological signal.

These genes drive clustering and downstream analyses.

---

## 5. Dimensionality Reduction

High-dimensional gene expression data is reduced into lower dimensions using methods such as:

* PCA
* UMAP
* t-SNE

This allows visualization of cellular relationships.

---

## 6. Clustering

Cells with similar gene expression patterns are grouped together.

Clusters often represent:

* Distinct cell types
* Cellular states
* Developmental stages

---

## 7. Cell Type Annotation

Cell identities can be assigned using:

* Known marker genes
* Reference datasets
* Automated tools like CellTypist

---

## 8. Trajectory Analysis

Trajectory analysis attempts to reconstruct biological progression paths.

Examples include:

* Stem cell differentiation
* Immune activation
* Tumor evolution
* Developmental transitions

RNA velocity provides directional information about where cells may transition next.

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Single_Cell_PIPELINE.git
cd Single_Cell_PIPELINE
```

---

## Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## Install Required Packages

```bash
pip install scanpy
pip install anndata
pip install scvelo
pip install celltypist
pip install igraph
pip install leidenalg
pip install decoupler
```

Or install all dependencies together:

```bash
pip install scanpy anndata scvelo celltypist igraph leidenalg decoupler
```

---

# Running the Notebooks

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Or use JupyterLab:

```bash
jupyter lab
```

Then open:

* `Single_cell_tutorial.ipynb`
* `Trajectory_analysis.ipynb`

---

# Dataset Sources

The notebooks use publicly available single-cell datasets, including datasets downloaded from:

* 10x Genomics
* NCBI GEO

Useful resources:

* url10x Genomics[https://www.10xgenomics.com/](https://www.10xgenomics.com/)
* urlNCBI GEO Database[https://www.ncbi.nlm.nih.gov/geo/](https://www.ncbi.nlm.nih.gov/geo/)

---

# Applications of This Pipeline

This pipeline can be adapted for:

* Cancer transcriptomics
* Immune profiling
* Developmental biology
* Stem cell analysis
* Precision medicine
* Infectious disease studies
* Drug response analysis
* Biomarker discovery

---

# Learning Goals

By working through these notebooks, you will learn:

* How scRNA-seq datasets are structured
* How to preprocess single-cell data
* How clustering works
* How to visualize cell populations
* How trajectory inference is performed
* How RNA velocity analysis works
* How biological interpretation is performed

---

# Recommended Background Knowledge

Helpful topics include:

* Basic Python programming
* Molecular biology
* Gene expression concepts
* RNA sequencing basics
* Statistics fundamentals

No advanced bioinformatics background is required to begin.





---



