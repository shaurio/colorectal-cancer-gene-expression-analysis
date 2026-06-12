# Colorectal Cancer Gene Expression Analysis

## Overview

This project investigates gene expression changes across healthy colon tissue, adjacent normal tissue, and colorectal tumor tissue using the publicly available GEO dataset GSE44076.

The goal is to identify genes that show progressive expression changes during colorectal cancer development.

## Dataset

* GEO Accession: GSE44076
* Platform: Affymetrix Human Genome U219 Array
* Samples:

  * Healthy colon tissue (n=50)
  * Adjacent normal tissue (n=98)
  * Tumor tissue (n=98)

Total samples: 246

## Analysis Pipeline

1. Load expression matrix from GEO.
2. Separate samples into healthy, adjacent normal, and tumor groups.
3. Calculate mean expression for each group.
4. Compute expression changes across tissue states.
5. Identify genes showing progressive increases from healthy → adjacent → tumor.

## Preliminary Findings

Several genes demonstrated strong progressive increases across tissue states, including:

* IL8
* CXCL1
* CXCL2
* SPP1
* THBS2
* TIMP1
* COL1A1
* COL1A2

These genes are associated with inflammatory signaling and extracellular matrix remodeling, suggesting that molecular alterations may occur in adjacent tissue prior to overt tumor formation.

## Future Work

* Statistical significance testing
* Volcano plots
* Heatmaps
* Pathway enrichment analysis
* Literature validation
* Independent dataset validation
