# Xenium Basic Analysis

A notebook that walks through basic handling of a 10x Genomics Xenium dataset, using the public Xenium V1 human ovarian cancer FFPE sample (base panel plus add-on, 480 genes).

The notebook loads the Xenium output bundle with spatialdata, then goes through quality control and filtering, normalisation, clustering, marker genes and a first pass of cell type annotation, with spatial plots along the way.

This is meant as a demonstration only. It shows the basic steps of getting a Xenium dataset into shape and can serve as a starting point for a larger analysis pipeline. It is not a full analysis of the sample.

## Running it

The main packages used are scanpy, squidpy, spatialdata, spatialdata-io and anndata. If rapids-singlecell is installed the notebook uses the GPU, otherwise it runs on the CPU.

Download the dataset from the 10x Genomics website and unpack it next to the notebook as `Xenium_V1_Human_Ovarian_Cancer_Addon_FFPE_outs`. On the first run the notebook converts it to a zarr store and saves the processed data as `.h5ad` files, so later runs are much faster.
