# Colorectal Cancer Gene Expression Analysis

## Overview

This project investigates gene expression changes across healthy colon tissue, adjacent normal tissue, and colorectal tumor tissue using GEO dataset GSE44076.

The goal is to identify genes that show progressive expression changes during colorectal cancer development.

## Dataset

* GEO Accession: GSE44076
* Platform: Affymetrix Human Genome U219 Array
* Samples:

  * Healthy tissue (n = 50)
  * Adjacent normal tissue (n = 98)
  * Tumor tissue (n = 98)

Total samples: 246

## Preliminary Findings

The strongest progressively increasing genes included:

* IL8
* CXCL1
* CXCL2
* SPP1
* THBS2
* TIMP1
* COL1A1
* COL1A2
* COL8A1
* COL12A1

These genes are associated with inflammatory signaling and extracellular matrix remodeling.

Several genes demonstrated increased expression in adjacent normal tissue relative to healthy tissue and further increased expression in tumor tissue.

## Current Status

Completed:

* Data acquisition from GEO
* Expression matrix processing
* Sample grouping
* Differential expression analysis
* Progressive gene identification

Planned:

* Statistical testing
* Visualization
* Literature review
* Research report


## Key Results

| Gene   | Progression Strength |
| ------ | -------------------: |
| IL8    |                 6.09 |
| CXCL1  |                 4.47 |
| SPP1   |                 4.37 |
| THBS2  |                 4.23 |
| PHLDA1 |                 4.15 |
| COL1A1 |                 4.06 |

## Figure 1

![Progressive Gene Expression](figure1_progressive_genes.png)

## Results

The gene expression dataset GSE44076 was obtained from the Gene Expression Omnibus (GEO) and contained expression measurements from 246 human colon tissue samples analyzed using the Affymetrix Human Genome U219 Array platform. The dataset consisted of 50 healthy colon mucosa samples from individuals without colorectal lesions, 98 adjacent normal tissue samples collected from colorectal cancer patients, and 98 colorectal tumor samples.

Expression data were loaded into Python and grouped according to tissue type. Mean expression values were calculated for healthy, adjacent normal, and tumor samples for each of the 49,386 probes present in the dataset. To identify genes associated with colorectal cancer progression, expression differences between tissue groups were examined. In addition to comparing healthy and tumor tissues directly, the analysis focused on genes that demonstrated progressive expression increases across all three tissue states (Healthy → Adjacent Normal → Tumor).

The distribution of expression differences showed that most probes exhibited relatively small changes between healthy and tumor tissues, with expression differences centered near zero. However, a subset of probes displayed substantial positive or negative expression changes, suggesting the presence of genes strongly associated with colorectal tumor biology.

To identify candidate progression-associated genes, probes were filtered to retain only those showing increased expression from healthy tissue to adjacent normal tissue and from adjacent normal tissue to tumor tissue. This approach identified multiple genes with strong stepwise increases across tissue states.

The most strongly progressive genes included IL8, CXCL1, SPP1, THBS2, PHLDA1, COL1A1, COL12A1, APCDD1, COL8A1, TIMP1, CXCL2, and COL1A2. Among these genes, IL8 demonstrated the largest overall increase, with mean expression values rising from 3.77 in healthy tissue to 5.65 in adjacent normal tissue and 9.86 in tumor tissue. Similar patterns were observed for CXCL1, SPP1, THBS2, and several collagen-associated genes.

Several of the identified genes belong to biological pathways involved in inflammation and extracellular matrix remodeling. Chemokine-related genes such as IL8, CXCL1, and CXCL2 showed substantial increases across tissue states, while extracellular matrix-associated genes including COL1A1, COL1A2, COL8A1, COL12A1, THBS2, and TIMP1 also demonstrated strong progressive expression patterns.

A notable observation was that many of these genes exhibited elevated expression in adjacent normal tissue compared with healthy tissue before further increases were observed in tumor samples. This pattern suggests that molecular alterations associated with colorectal cancer may be detectable in tissue surrounding tumors even when that tissue is not classified as tumor tissue itself.

Overall, the analysis identified a set of candidate genes whose expression progressively increased across healthy, adjacent normal, and tumor colon tissues. These findings provide a foundation for further investigation into the biological significance of these genes and their potential roles in colorectal cancer development and progression.

### Results Subsection

Statistical testing confirmed that the identified genes were significantly differentially expressed between healthy and tumor tissues. IL8 exhibited the strongest statistical signal (p = 1.39 × 10⁻⁵⁴), followed by TIMP1, COL1A1, CXCL1, THBS2, and SPP1. All examined genes demonstrated progressively increasing expression across healthy, adjacent normal, and tumor tissues.

|index|Gene|T\_Statistic|P\_Value|
|---|---|---|---|
|0|IL8|-27\.96735832921123|1\.393956855073207e-54|
|1|CXCL1|-20\.558784292831508|3\.2553498294811003e-44|
|2|SPP1|-16\.097052522531815|5\.5377223682575366e-30|
|3|THBS2|-20\.279741902375587|4\.962829272156988e-38|
|4|COL1A1|-22\.23867101018993|9\.928920185143985e-46|
|5|TIMP1|-24\.772615102264776|9\.65868646072685e-51|

"Using GSE44076, I identified a set of inflammatory and extracellular-matrix genes that display a stepwise expression increase from healthy tissue to adjacent normal tissue to tumor tissue."

## Literature Review Notes

| Gene        | Biological Function                                             | Findings from Literature                                                             | Findings in This Project                                    |
| ----------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| IL8 (CXCL8) | Chemokine involved in inflammation and immune-cell recruitment  | Associated with inflammation, tumor progression, angiogenesis, and colorectal cancer | Strong progressive increase from healthy → adjacent → tumor |
| CXCL1       | Chemokine involved in inflammatory signaling                    | Reported to contribute to tumor progression and colorectal carcinoma                 | Progressive increase across tissue states                   |
| SPP1        | Secreted phosphoprotein involved in cell adhesion and signaling | Frequently associated with tumor invasion and metastasis                             | Strong progressive increase                                 |
| COL1A1      | Extracellular matrix collagen protein                           | Associated with remodeling of tumor microenvironment                                 | Progressive increase                                        |
| TIMP1       | Regulator of extracellular matrix degradation                   | Frequently elevated in cancer tissues                                                | Progressive increase                                        |


