---
title: "Dimensionality reduction for visualisation"
summary: "Reduction of high-dimensional datasets to 2D for visualization & interpretation"
---

<script src="index_files/libs/htmlwidgets-1.6.1/htmlwidgets.js"></script>
<link href="index_files/libs/datatables-css-0.0.0/datatables-crosstalk.css" rel="stylesheet" />
<script src="index_files/libs/datatables-binding-0.27/datatables.js"></script>
<script src="index_files/libs/jquery-3.6.0/jquery-3.6.0.min.js"></script>
<link href="index_files/libs/dt-core-1.12.1/css/jquery.dataTables.min.css" rel="stylesheet" />
<link href="index_files/libs/dt-core-1.12.1/css/jquery.dataTables.extra.css" rel="stylesheet" />
<script src="index_files/libs/dt-core-1.12.1/js/jquery.dataTables.min.js"></script>
<link href="index_files/libs/dt-ext-select-1.12.1/css/select.dataTables.min.css" rel="stylesheet" />
<script src="index_files/libs/dt-ext-select-1.12.1/js/dataTables.select.min.js"></script>
<link href="index_files/libs/dt-ext-searchpanes-1.12.1/css/searchPanes.dataTables.min.css" rel="stylesheet" />
<script src="index_files/libs/dt-ext-searchpanes-1.12.1/js/dataTables.searchPanes.min.js"></script>
<script src="index_files/libs/jszip-1.12.1/jszip.min.js"></script>
<link href="index_files/libs/dt-ext-buttons-1.12.1/css/buttons.dataTables.min.css" rel="stylesheet" />
<script src="index_files/libs/dt-ext-buttons-1.12.1/js/dataTables.buttons.min.js"></script>
<script src="index_files/libs/dt-ext-buttons-1.12.1/js/buttons.html5.min.js"></script>
<script src="index_files/libs/dt-ext-buttons-1.12.1/js/buttons.colVis.min.js"></script>
<script src="index_files/libs/dt-ext-buttons-1.12.1/js/buttons.print.min.js"></script>
<link href="index_files/libs/crosstalk-1.2.0/css/crosstalk.min.css" rel="stylesheet" />
<script src="index_files/libs/crosstalk-1.2.0/js/crosstalk.min.js"></script>
<script src="index_files/libs/kePrint-0.0.1/kePrint.js"></script>
<link href="index_files/libs/lightable-0.0.1/lightable.css" rel="stylesheet" />


## Description

## The task

Dimensionality reduction is one of the key challenges in single-cell data
representation. Routine single-cell RNA sequencing (scRNA-seq) experiments measure cells
in roughly 20,000-30,000 dimensions (i.e., features - mostly gene transcripts but also
other functional elements encoded in mRNA such as lncRNAs). Since its inception,
scRNA-seq experiments have been growing in terms of the number of cells measured.
Originally, cutting-edge SmartSeq experiments would yield a few hundred cells, at best.
Now, it is not uncommon to see experiments that yield over [100,000
cells](https://openproblems.bio/bibliography#tabula2018single) or even [\> 1 million
cells.](https://openproblems.bio/bibliography#cao2020human)

Each *feature* in a dataset functions as a single dimension. While each of the \~30,000
dimensions measured in each cell contribute to an underlying data structure, the overall
structure of the data is challenging to display in few dimensions due to data sparsity
and the [*"curse of
dimensionality"*](https://en.wikipedia.org/wiki/Curse_of_dimensionality) (distances in
high dimensional data don't distinguish data points well). Thus, we need to find a way
to [dimensionally reduce](https://en.wikipedia.org/wiki/Dimensionality_reduction) the
data for visualization and interpretation.

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="928" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **continuity**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Density preservation**<sup><a href="/bibliography#narayan2021assessing" target="_blank">2</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Distance correlation**<sup><a href="/bibliography#schober2018correlation" target="_blank">3</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Distance correlation (spectral)**<sup><a href="/bibliography#coifman2006diffusion" target="_blank">4</a></sup>: Missing 'metric_description'.

<!-- -->

-   **local continuity meta criterion**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **global property**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **local property**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **co-KNN size**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **co-KNN AUC**<sup><a href="/bibliography#zhang2021pydrmetrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **trustworthiness**<sup><a href="/bibliography#venna2001neighborhood" target="_blank">5</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-08c849b43e52d8f22110" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-08c849b43e52d8f22110">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["densMAP (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","NeuralEE (CPU) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","densMAP (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PyMDE Preserve Distances (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","densMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP PCA (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","densMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PyMDE Preserve Distances (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","densMAP PCA (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PHATE (logCP10k, 1kHVG) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","UMAP (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","UMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","NeuralEE (CPU) (Default) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","UMAP PCA (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","densMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PHATE (logCP10k, 1kHVG) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","densMAP PCA (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PHATE (gamma=0) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PHATE (logCP10k) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PHATE (default) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","PHATE (gamma=0) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","UMAP PCA (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","densMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP PCA (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","UMAP (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","UMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PHATE (logCP10k) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","densMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PHATE (gamma=0) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","NeuralEE (CPU) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","UMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","PHATE (default) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","NeuralEE (CPU) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","PyMDE Preserve Distances (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","PHATE (logCP10k, 1kHVG) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PyMDE Preserve Distances (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","UMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PHATE (default) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PyMDE Preserve Distances (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","densMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","NeuralEE (CPU) (Default) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","PyMDE Preserve Distances (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","UMAP PCA (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","Diffusion maps <sup><a href=\"/bibliography#coifman2006diffusion\" target=\"_blank\">4<\/a><\/sup>","Diffusion maps <sup><a href=\"/bibliography#coifman2006diffusion\" target=\"_blank\">4<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","densMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","UMAP (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","UMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","UMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","NeuralEE (CPU) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","Diffusion maps <sup><a href=\"/bibliography#coifman2006diffusion\" target=\"_blank\">4<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","UMAP (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","UMAP PCA (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PHATE (logCP10k, 1kHVG) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","UMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PHATE (logCP10k) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","PHATE (gamma=0) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PyMDE Preserve Distances (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","UMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","PyMDE Preserve Distances (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","NeuralEE (CPU) (Default) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","PHATE (default) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","NeuralEE (CPU) (Default) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","PHATE (logCP10k) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","Diffusion maps <sup><a href=\"/bibliography#coifman2006diffusion\" target=\"_blank\">4<\/a><\/sup>","densMAP (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","densMAP PCA (logCP10k) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PyMDE Preserve Distances (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","UMAP (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#vandermaaten2008visualizing\" target=\"_blank\">9<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","PyMDE Preserve Neighbors (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","NeuralEE (CPU) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","UMAP PCA (logCP10k) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","densMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","UMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","UMAP (logCP10k, 1kHVG) <sup><a href=\"/bibliography#mcinnes2018umap\" target=\"_blank\">11<\/a><\/sup>","densMAP PCA (logCP10k, 1kHVG) <sup><a href=\"/bibliography#narayan2021assessing\" target=\"_blank\">2<\/a><\/sup>","PyMDE Preserve Distances (logCP10k, 1kHVG) <sup><a href=\"/bibliography#agrawal2021mde\" target=\"_blank\">8<\/a><\/sup>","NeuralEE (CPU) (Default) <sup><a href=\"/bibliography#xiong2020neuralee\" target=\"_blank\">7<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","PHATE (logCP10k, 1kHVG) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","Principle Component Analysis (PCA) (logCP10k, 1kHVG) <sup><a href=\"/bibliography#pearson1901pca\" target=\"_blank\">6<\/a><\/sup>","PHATE (gamma=0) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PHATE (logCP10k) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","PHATE (default) <sup><a href=\"/bibliography#moon2019visualizing\" target=\"_blank\">10<\/a><\/sup>","Diffusion maps <sup><a href=\"/bibliography#coifman2006diffusion\" target=\"_blank\">4<\/a><\/sup>"],["Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Overall mean","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Overall mean","Overall mean","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Overall mean","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","5k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2019pbmc\" target=\"_blank\">14<\/a><\/sup>","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Mouse myeloid lineage differentiation <sup><a href=\"/bibliography#olsson2016single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Zebrafish <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Overall mean","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>","Mouse hematopoietic stem cell differentiation <sup><a href=\"/bibliography#nestorowa2016single\" target=\"_blank\">15<\/a><\/sup>"],[0.545047295621359,0.506490527537706,0.481582494288093,0.473426291002834,0.465242304465696,0.457950039745393,0.456141641462576,0.447590229299205,0.445028388754523,0.443646131985656,0.441688684280695,0.439462273888756,0.43211805491082,0.431792633699819,0.42907946962985,0.427394747796049,0.42604574529851,0.42428121254362,0.423902897363383,0.41865037568175,0.418412331551172,0.417878641835099,0.414726798161101,0.410098970191979,0.403777103995067,0.402771972957809,0.401591214239062,0.400741322700206,0.397406751251203,0.39252062988052,0.386521868229543,0.382967710760787,0.380610349803942,0.377515384462661,0.37714840164718,0.374486024729612,0.373753937769071,0.372466944553195,0.370931751032348,0.37086004020614,0.370837968342482,0.368584915902452,0.364662682561599,0.360038533081525,0.357475444164895,0.357140569155466,0.355825188594743,0.354920979412259,0.353425914670037,0.351015717661627,0.35061485017506,0.350596422803734,0.349424581156481,0.348394838827954,0.346575515149468,0.345772521192122,0.343005075994585,0.342401152019028,0.34067658674673,0.340355323325465,0.340317856630798,0.338051812290152,0.336122157194542,0.335741623687659,0.33226191035454,0.330583620162941,0.329525390400259,0.328583866808462,0.328369906931026,0.32807737811202,0.321877550741657,0.318671813285351,0.318253701431948,0.317692697841741,0.317350606177526,0.311803788748587,0.308707265507851,0.306054082238189,0.301193357675007,0.298802759515613,0.298102991640922,0.29226971183752,0.289791285018683,0.284728049338314,0.284344991999951,0.283664820724221,0.282190986312087,0.279763444179052,0.279126786720509,0.278691494048684,0.274881615328941,0.228256548680625,0.210390407174513,0.208119622772679,0.19118164890488,0.167370754330714,0.140077351242265,0.132459160518222,0.12769764334769,0.117969676722864,0.114473116948052,0.111522683703842,0.109257415342824,0.104515141909347,0.100576689159299,0.0950841288829295,0.0939432648186151,0.0897926573455349,0.0569969153444722,0.0513760656027528,0.0465179759164838,0.0334609157526023,0.0266600299082014,0.0153843113259017,-0.0807151369013563],[null,0.96656458521664,0.935172081685106,0.925581839332488,0.839805850698596,null,null,null,0.949244219718033,0.94872433805558,0.792618831673494,0.840648285969583,null,null,0.942253100732949,0.958943738375145,0.95964000082634,0.947708225143381,0.788661531086708,0.945563588622442,0.963003061018777,0.966194869427639,0.950890915320837,0.814885139951178,null,0.958922794937387,0.946586967625292,0.946082757923066,0.943830982183118,0.815224028188735,null,null,0.832351629608203,null,0.799848313540207,null,0.848856718451779,null,0.834764861029562,0.927197333487204,0.820686593001792,0.809155066497394,0.83933103866766,null,null,null,null,0.808658504108793,null,null,0.533626826406683,0.771612534056944,0.747793267065869,0.789647501623004,0.797382120655965,null,null,0.707297963812813,null,null,null,0.793869206563925,null,0.169201645232276,0.76934393824024,null,null,0.792810699107171,0.921059766445051,null,0.62002563077859,null,null,null,null,null,null,null,null,null,null,0.736786008643798,null,0.930632627169053,null,null,null,null,null,null,null,null,0.475269924171352,0.256791024006199,0.347310403042783,0.28203879085346,0.466496128714359,0.287772483391473,0.235864761360775,0.279240920555236,0.319094404901645,0.122208101988806,0.205646065583526,0.256570787221121,0.268232459564693,0.173099467916094,0.171041938466826,0.344628525974223,0.188571264484351,0.264918828684069,0.190554026654201,0.17224012681184,0.266254820475558,0.184213601727325,-0.292860723445077],[0.786899130085512,0.295535077895018,0.358457763190205,0.0762410697073398,0.861316734886938,0.0992096258435234,0.267333269980721,0.422535951858076,-0.161031488008116,0.255236869526638,0.550121352381872,0.715088513744556,0.322031493105552,0.658714128201135,0.109222092848067,-0.122721079006181,-0.0600016532171973,-0.228513575573001,0.50526789959117,-0.140792238952583,-0.0248152475101115,-0.198875486579967,0.105176337510045,0.659609003016246,0.0512296018007089,0.105707106568165,0.0529742552255796,0.176770161844501,0.225966558218938,0.187435343427335,0.103637422345763,0.0218184609829134,0.172353516003528,-0.0332858694019941,0.552778860062162,0.480497967569215,0.0423308287140755,-0.0416834646427985,0.19414568527902,0.239915358243169,0.293802090773458,0.346870688159684,0.149789506540913,-0.000113246002858716,0.0313622196106029,0.081076454940781,0.082221326563081,0.176340256869872,-0.0160674050571678,-0.0492428296404758,0.375706871089966,0.173240642379364,0.342900934479771,0.113707976652226,0.316349134438298,0.313607024250231,0.345944831055626,0.0420804029302081,0.0996392026915216,-0.060353176088196,0.148448135728062,0.28922278467347,-0.0107282957802547,0.204722405209282,0.260358865490829,0.397167684990109,0.104065196945514,0.148921962639585,-0.212010964625805,0.178384258691513,0.206897107798471,0.0405870798772639,0.0953302336097512,0.0460863981561252,0.123433366915171,0.0826067478081217,0.0162818512692867,0.0309630709924326,-0.0174166387966451,0.0854182497800575,0.0597529930847659,0.268711998637049,0.192554140937465,-0.137655501237149,0.0164817011729319,0.251420610335601,-0.0271713311898404,0.0546318444045025,0.0644971361472979,-0.0988090594886735,-0.0316163673260156,-0.0237951972808861,0.691105569937072,0.678660298106062,0.336385120138478,0.40935398601211,0.407339095218291,0.221767418163049,0.206519994730244,0.247807507614178,0.208203950335949,0.11325031380711,0.367114885595471,0.157406024925527,0.164343038668165,0.308430324652983,0.187435433081144,0.146918818379071,-0.133017615678844,-0.268564931950992,0.0659816852887672,-0.211401796005737,-0.479964677630938,-0.365403603008825,-0.496072006351042],[0.770719967375606,0.531644147944968,0.35283284021195,0.550307830194078,0.790670493299562,0.96041275416021,0.663635244801901,0.549263624811916,0.445541703541543,0.32230240980364,0.821119653975706,0.503631208695805,0.60501618075261,0.60278741935949,0.396579219531495,0.433613815712972,0.385834061520868,0.441178653202959,0.805204449534709,0.445787748055924,0.26158040229204,0.415980665664708,0.293002791825264,0.428189586957423,0.688024525036355,0.221989313122272,0.36407503995373,0.322221930094562,0.326733824056883,0.595500395579993,0.56774883097228,0.548212010367664,0.519385371429626,0.617644033264524,0.3375195337879,0.382941661617348,0.777634271375715,0.603888971629041,0.465621901725346,0.188142554280346,0.411414910300553,0.390774907778482,0.39502408087516,0.568459676161634,0.495059372746521,0.559992194252418,0.583425374706197,0.402884406940421,0.846262532113163,0.644310101430344,0.314796251971805,0.408336599036554,0.44420344109356,0.475059684252612,0.373845078245469,0.636452093585008,0.332908740176078,0.529807679414076,0.569981443800085,0.615363883552946,0.399991919896761,0.285930523158756,0.560167771306001,0.738786127500385,0.405079472233034,0.312668237314954,0.573876252538264,0.345363339992355,0.193897152527583,0.400094631885136,0.318123083851345,0.383104814690466,0.329073078969129,0.402598169634414,0.4522395438159,0.395292527356249,0.371163621364564,0.358523980435905,0.534248922983002,0.508083338428201,0.33315791089608,0.270793064666249,0.30653514623754,0.0796491625360229,0.311486007254679,0.36214104040422,0.387883781649548,0.468919138358439,0.309146614804566,0.599719636733537,0.329629250950261,0.387105268937884,0.318115068817826,0.256882499839397,0.493482901537866,0.194674871347345,0.071613589828755,0.0897607164296973,0.137444680519181,0.0707121653539615,0.0758704148617893,0.15341806261716,0.0293246272694388,0.0390558620663016,0.0085275160768885,0.00817777231087052,0.119583024751431,0.00602714478587172,0.144560409249863,-0.00828585814614641,-0.039855065923024,-0.0106071376422412,-0.00357575100186459,-0.0239846373365054,-0.0686559069061946],[-0.00648301411731233,0.0729899142473271,0.386395499862698,0.322836245101326,0.168599311732171,0.132795661619706,0.185946602619548,0.0546160110706873,0.288044763809986,0.152441942806229,0.234602952432416,0.339329381559989,0.140322207782094,0.00635958919422247,0.174539130680524,0.0267460368838828,0.00503065435315451,0.26657097485243,0.195238848860175,0.17959521245356,0.0151362769969831,0.0302213638415461,-0.0385024479423169,0.362625471385835,0.190003261280078,-0.0982753173671716,-0.0576745274309835,-0.0784768525866586,-0.161388655407624,0.28862647346201,0.105871642946748,0.120968984187202,0.258309292706639,0.164457947704901,0.319853112135805,0.0273376593198695,0.135586591360555,0.153274471943714,0.289987411977062,-0.123434299495116,0.327083474732928,0.312788728633151,0.351493078704738,0.139915878559221,0.10802859648218,0.0259774641202572,0.185630496976562,0.315676725311736,0.000483601671315323,0.00536915712104469,0.433472831276778,0.328405712347343,0.28992831885983,0.296363409326313,0.29025256374886,0.075794119842483,0.103485262638334,0.331845097735667,0.249293358531537,-0.00502131183717357,0.043551409233156,0.326244641514094,0.264884244196601,0.364386032410902,0.281754293441609,0.0368726480385223,-0.02893300175706,0.306993717453119,-0.0820350390463093,0.153986429739204,0.113990350911668,0.141328572599527,0.15459071465692,0.0308237984723302,-0.0257479402372419,-0.0188840939013631,0.124598533850643,0.120851617039538,-0.0432850547359221,0.192430769228559,0.00295590672244786,0.0991326370813403,0.135821372961068,-0.317591632395524,0.0474153408249166,0.172544816404821,0.0443559852104735,-0.10615718757255,-0.0518153691235106,-0.0133049104262293,-0.0347740660482509,0.0929554722597577,-0.209667855085296,-0.186319437984026,-0.163354771763531,-0.250526097713571,-0.214676004905617,-0.10395514317858,-0.260313078820345,-0.181391357470958,-0.205309751754223,-0.290321908532601,-0.232022787518724,-0.15645693369224,-0.164582885539558,-0.244300607008245,-0.282515243048863,-0.17133761030909,-0.302759568426168,-0.194553968905373,-0.317295070688595,-0.363456963358901,-0.307321768847484,-0.362102848955536,-0.371438738480141],[null,0.531447024450254,0.440565892664924,0.432262032907889,0.0264401890874129,null,null,null,0.461428058844636,0.454405658926649,0.0308961929825643,0.048331926066082,null,null,0.407965554359526,0.482649033779281,0.480906248398175,0.439540724793685,0.0268038187275428,0.41780716592342,0.516992157465785,0.497770259880055,0.472704905428264,0.0419529993282096,null,0.499718078835409,0.397150033317956,0.407811779178841,0.392024193961761,0.0507109267625252,null,null,0.0464952882227139,null,0.042020794684844,null,0.028566498000037,null,0.0430438882485994,0.424522015480035,0.0392781643482709,0.0355062772337029,0.0462980653670502,null,null,null,null,0.0425138518240033,null,null,0.243272335844995,0.0361534147288494,0.0263847201592575,0.0399684443430938,0.0395924882744849,null,null,0.0243755123171837,null,null,null,0.0456386014434248,null,0.00861617350680727,0.0266743912285135,null,null,0.0409052529074963,0.418934850581783,null,0.221487518581168,null,null,null,null,null,null,null,null,null,null,0.251473678814906,null,0.38541186119227,null,null,null,null,null,null,null,null,0.0732319352691145,0.0879295334664823,0.0454925658489954,0.0964135129137434,0.0731465833632065,0.05856847783411,0.0896707123470067,0.0573223400078524,0.0527304074699988,0.0921117768559772,0.0506478209658422,0.0577661699185743,0.0558542872262338,0.0473361670166095,0.0449633840323654,0.0348577183728513,0.0557006537955993,0.0459022549973541,0.0421638415185811,0.0694593810279783,0.0734709206056571,0.0682985951076288,0.0262201054949557],[null,0.312960952425862,0.236221494156784,0.30345053197784,0.600548495073447,null,null,null,0.271634398805421,0.184390407225408,0.62810711099848,0.526488946956517,null,null,0.204600120929729,0.262311516974224,0.250889416597627,0.244899974451899,0.604189617472296,0.238616890501062,0.195412391238045,0.258920496516063,0.192994208047868,0.491576681822757,null,0.160395811925847,0.245928519312805,0.187274050713496,0.213621421799581,0.570845307542591,null,null,0.54910200030494,null,0.46306622822961,null,0.629411338176386,null,0.514073084185976,0.111409579694293,0.501654414177298,0.520592538441165,0.493381715629506,null,null,null,null,0.524978569918263,null,null,0.183407048268405,0.520801521309334,0.519584416675602,0.527662709901433,0.424209585285757,null,null,0.50492658131296,null,null,null,0.425085691701328,null,0.609712295394915,0.496106235204367,null,null,0.445438497535442,0.115880668889993,null,0.175079856394476,null,null,null,null,null,null,null,null,null,null,0.0856894257482844,null,0.0890150746394926,null,null,null,null,null,null,null,null,0.181557176760942,0.206284949612625,0.272279923981571,0.167825977546457,0.118293025191573,0.173397776596526,0.1537524101823,0.149650380271624,0.16460981788036,0.171957377184993,0.144650084797377,0.13823926952857,0.132890411995272,0.137099180714,0.188154390251198,0.126668604141973,0.130427873223981,0.16375609281168,0.123659830594985,0.102825880058261,0.117411838102185,0.0944379592849912,0.081306095714312],[null,0.468821709834422,0.417488887157911,0.395073186615199,0.390716749681496,null,null,null,0.438429068331974,0.431083402661903,0.349014195258542,0.402920077635407,null,null,0.412788379952132,0.444800006738812,0.461555364602681,0.422472641484288,0.355443415430762,0.422085752772977,0.468310071747416,0.416695665634336,0.444099683176693,0.379017104217076,null,0.447443284623481,0.404627156182362,0.410237571133712,0.400499317701131,0.349624819918754,null,null,0.408791776571605,null,0.362097242627491,null,0.352463857822314,null,0.399466328608313,0.361600608076319,0.370009075096176,0.36945983049864,0.391058002871156,null,null,null,null,0.364660600373906,null,null,0.222814650150552,0.380201512065237,0.327065756031293,0.355461912644647,0.344117618357792,null,null,0.359063907005861,null,null,null,0.335361923906442,null,0.355378694279709,0.337679776033065,null,null,0.342254806937333,0.355506793263666,null,0.26743152168555,null,null,null,null,null,null,null,null,null,null,0.203301938888179,null,0.388959433854777,null,null,null,null,null,null,null,null,0.170975694625958,0.189998232484438,0.147053565687321,0.172374264738607,0.172248748555231,0.164606343227082,0.169391536947679,0.163621580438968,0.1561342861769,0.178008188790629,0.157967479753708,0.166360037893111,0.16059793490989,0.161606556261074,0.165116337580155,0.147018745345174,0.144656100889605,0.167884314144729,0.151758554852072,0.14671344217805,0.160541154640484,0.142814529080082,0.126244024929093],[null,0.532292843207722,0.441267070541123,0.432949994866003,0.0264452417058106,null,null,null,0.462162439675531,0.455128863332991,0.0309020971261605,0.048341162111181,null,null,0.408614847520279,0.483417188623062,0.481671629530753,0.440240271075059,0.0268089408341655,0.418472122394496,0.517814970736215,0.49856248074751,0.473457233802238,0.041961016384954,null,0.500513399733032,0.397782113153301,0.40846082760037,0.39264811582298,0.0507206174255033,null,null,0.0465041732933881,null,0.0420288246970201,null,0.0285719569478862,null,0.0430521137700189,0.425197658897217,0.0392856702543428,0.0355130623466607,0.0463069127491955,null,null,null,null,0.0425219760575014,null,null,0.243659513297053,0.0361603235072925,0.0263897621777564,0.0399760821590167,0.0396000542466497,null,null,0.024380170383795,null,null,null,0.0456473228045518,null,0.00861782002441099,0.0266794886020392,null,null,0.0409130697439312,0.419601601807167,null,0.221840024643187,null,null,null,null,null,null,null,null,null,null,0.251873909025567,null,0.386025259266865,null,null,null,null,null,null,null,null,0.0732707087959009,0.0879760888129804,0.0455166524338173,0.096464560204953,0.0731853116994022,0.058599487617421,0.0897181895815542,0.0573526900085397,0.0527583262169086,0.0921605465414176,0.0506746370623399,0.057796754910333,0.0558838599487617,0.0473612297181896,0.0449871904355252,0.0348761742100769,0.055730145175064,0.0459265584970111,0.0421861656703672,0.0694961571306576,0.0735098206660973,0.068334756618275,0.0262339880444065],[null,0.424031804183361,0.354235960158163,0.398382401902053,0.404237687112612,null,null,null,0.382414152970881,0.320794915462517,0.408288457073309,0.335300156648711,null,null,0.329486001514256,0.380446748500963,0.373018844652501,0.360615186082685,0.378382916698935,0.354223412049564,0.339075373449318,0.380053216703197,0.329475037001752,0.293711954060887,null,0.311204042946917,0.357446336661892,0.3183068417673,0.334351720118891,0.358124910848495,null,null,0.335147125447079,null,0.268392205817625,null,0.36214837000928,null,0.308591287243829,0.26459942868606,0.295752802647671,0.310300108397201,0.301346117582688,null,null,null,null,0.311402341346097,null,null,0.277410729390695,0.302806224317349,0.287261022288946,0.306487361370344,0.23659107159178,null,null,0.3113537818298,null,null,null,0.24286610484505,null,0.365833091692965,0.265586752490697,null,null,0.252605645706334,0.266696535725709,null,0.269770998573477,null,null,null,null,null,null,null,null,null,null,0.211403734524716,null,0.244992809181689,null,null,null,null,null,null,null,null,0.103865919661769,0.128571931759959,0.1607135281334,0.100581394090056,0.0313571190965127,0.0777998903607318,0.0854520576159126,0.0543506999505092,0.0671981949870206,0.0981236679828561,0.0477481395379595,0.0444478125007703,0.0400527268225424,0.0423307661751979,0.0648420725148049,0.0288518097000123,0.0486091931711159,0.0494182387123812,0.00822897736271178,0.039087900340619,0.043607956841518,0.0299017279093299,0],[0.629053099141632,0.928617215971482,0.893187453252065,0.897177777424129,0.54364229137892,0.639382117358133,0.707651448448134,0.763945329456139,0.91241656985534,0.911952512054999,0.571215998904402,0.634543079499734,0.661102338003022,0.581873133820631,0.904746248229546,0.923740471378328,0.921912885720197,0.908099049922816,0.55302753539737,0.905144102996642,0.931613858077247,0.913262886515906,0.923969317440362,0.587460744795228,0.685851027863128,0.920101214252749,0.907016248388688,0.908724159332877,0.905780034056368,0.658393475649255,0.768829576653384,0.840871387505368,0.637663324451696,0.761245426283214,0.583878900889134,0.673252682707824,0.531968946832677,0.774387799282825,0.616570948255755,0.889450164711873,0.609412488092328,0.554887951038435,0.632598306627918,0.731891823608103,0.795451587820275,0.761516163308406,0.572023556133134,0.559572561372001,0.583024929952839,0.803626441735597,0.677981444053663,0.54824574428907,0.482734172732924,0.539613306006849,0.603815436649624,0.495266359653936,0.618295823116197,0.588880423447914,0.443792341963775,0.811431897674283,0.708846251136463,0.590651322290474,0.53016490905582,0.532161951624933,0.453355890581003,0.602209111972855,0.669093113874316,0.569631676061854,0.886167703741426,0.569382600749966,0.804129414198641,0.627486719519189,0.648698408676701,0.682360097188609,0.581186215522032,0.689343812342104,0.59655053689114,0.633282303040681,0.731226201249592,0.409278680625636,0.651377620029974,0.543530722345115,0.488404709573369,0.797841399175645,0.61041009381912,0.460083019717982,0.582180065548777,0.542846140521502,0.647111166711662,0.627160309376102,0.644796823517257,0.50708201671638,0.22617992879049,0.374421107622674,0.226936600008095,0.404506283313982,0.201769915660937,0.296274154740713,0.369475169012595,0.281029840498727,0.253441118404166,0.384310709802075,0.270823200381297,0.283965633821402,0.283967541920103,0.269700431072521,0.235824120121565,0.199416642855185,0.237490697560155,0.247359127182815,0.197796813834772,0.320252166985497,0.322665985230802,0.317333032832251,0.161871791986125],[1928,439,409,368,549,1690,579,972,819,469,1366,419,982,858.75,329,759,388,589,359,540,649,409,569,549,498,519,358,348,329,1082,1053,1199,699,1098,529,599.75,659,609,398,459,388,358,810,510,1092,648,1869,669,280,1228,619,509,996,460,409,1075.75,509.25,498,1640,360,862.25,669,1136,459,309,609.75,1437,599,400,751,509,691.25,750,851.5,748.25,546.75,461.25,541.75,1073,348,559.5,419,371.25,359,454.75,921.25,736.25,349.25,471.25,1159,564.75,655.75,519,489,828,519,509,420,609,409,409,559,449,419,449,460,430,879,399,509,419,439,440,499,519],[239.8,32.6,22,142.5,206,461.8,112.7,110,157,36.8,623.4,150.8,123.5,143.775,190.9,208,61.7,65.7,100,28.1,379,152,233.4,75.6,248.3,194,158,144.7,153.9,213.9,297.6,192.3,238.9,268.3,69.5,161.725,181.7,128.6,239.5,35,247.9,281,214.1,174.4,181.4,178.2,413.3,262.4,118.9,308.4,156.6,315.8,315.2,92.9,198.9,399.175,78.275,164.1,470.5,165.4,292.6,284.5,343.1,223.4,78.9,79.45,270.2,74.4,61.9,245.675,314.5,167.9,192.325,229.825,144.85,196.05,255.675,79.475,304.2,37.8,263.5,263.3,41.65,36.5,94.775,333.925,199.15,90.075,173.475,321.7,202.275,242.175,96.7,192.1,248.2,385.2,65.8,146.4,188.8,75.2,145.9,146.5,83.7,86.8,49.9,94.1,393.4,158.8,104.9,267.7,27.9,350.5,120.7,162.9,87.7],[5.56640625,0.45712890625,0.3548828125,0.56494140625,1.26953125,56.4453125,1.3671875,1.7578125,0.39404296875,0.423046875,15.8203125,0.57568359375,1.5625,2.0659423828125,0.39482421875,0.8150390625,0.45849609375,0.58447265625,0.53291015625,0.41630859375,0.520800780273437,2.05078125,0.56025390625,0.615625,1.46484375,0.55537109375,0.53662109375,0.484375,0.5365234375,0.7548828125,1.85546875,2.5390625,0.57958984375,1.5625,0.57451171875,0.9702392578125,1.26953125,1.3671875,0.710546875,0.4185546875,0.75751953125,0.74111328125,0.9556640625,1.46484375,2.5390625,1.85546875,1.66015625,0.94931640625,1.66015625,1.85546875,0.774609375,0.7427734375,15.8203125,0.58857421875,0.75908203125,19.00029296875,0.785498046875,2.63671875,56.54296875,1.7578125,1.19057617163086,0.765625,5.37109375,1.26953125,0.461328125,0.84365234375,5.37109375,0.55302734375,0.41572265625,0.9651611328125,0.440625,0.9998046875,1.1191162109375,1.17509765625,2.018505859375,0.9727783203125,0.857568359375,0.779052734375,1.46484375,1.3671875,1.03154296875,0.903515625,0.7405029296875,0.41064453125,0.8121337890625,18.99248046875,5.17578125,0.8883544921875,1.0319091796875,13.671875,0.87685546875,2.0146728515625,0.970703125,0.99208984375,2.83203125,0.94755859375,0.97490234375,0.777734375,1.07421875,0.9029296875,0.89443359375,0.99345703125,0.7779296875,0.7796875,0.77939453125,0.77724609375,2.83203125,2.34375,0.94970703125,0.82783203125,0.77861328125,0.9765625,0.84765625,0.9765625,0.97744140625]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>continuity<\/th>\n      <th>Density preservation<\/th>\n      <th>Distance correlation<\/th>\n      <th>Distance correlation (spectral)<\/th>\n      <th>local continuity meta criterion<\/th>\n      <th>global property<\/th>\n      <th>local property<\/th>\n      <th>co-KNN size<\/th>\n      <th>co-KNN AUC<\/th>\n      <th>trustworthiness<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":14,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":13,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":15,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":8,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":9,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":10,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":11,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":12,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render","options.columnDefs.6.render","options.columnDefs.7.render","options.columnDefs.8.render","options.columnDefs.9.render","options.columnDefs.10.render","options.columnDefs.11.render","options.columnDefs.12.render","options.columnDefs.13.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **densMAP (logCP10k)**<sup><a href="/bibliography#narayan2021assessing" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **densMAP (logCP10k, 1kHVG)**<sup><a href="/bibliography#narayan2021assessing" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **densMAP PCA (logCP10k)**<sup><a href="/bibliography#narayan2021assessing" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **densMAP PCA (logCP10k, 1kHVG)**<sup><a href="/bibliography#narayan2021assessing" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **Diffusion maps**<sup><a href="/bibliography#coifman2006diffusion" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **NeuralEE (CPU) (Default)**<sup><a href="/bibliography#xiong2020neuralee" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/HiBearME/NeuralEE).

<!-- -->

-   **NeuralEE (CPU) (logCP10k, 1kHVG)**<sup><a href="/bibliography#xiong2020neuralee" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/HiBearME/NeuralEE).

<!-- -->

-   **Principle Component Analysis (PCA) (logCP10k)**<sup><a href="/bibliography#pearson1901pca" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html).

<!-- -->

-   **Principle Component Analysis (PCA) (logCP10k, 1kHVG)**<sup><a href="/bibliography#pearson1901pca" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html).

<!-- -->

-   **PHATE (default)**<sup><a href="/bibliography#moon2019visualizing" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/PHATE/).

<!-- -->

-   **PHATE (logCP10k, 1kHVG)**<sup><a href="/bibliography#moon2019visualizing" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/PHATE/).

<!-- -->

-   **PHATE (logCP10k)**<sup><a href="/bibliography#moon2019visualizing" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/PHATE/).

<!-- -->

-   **PHATE (gamma=0)**<sup><a href="/bibliography#moon2019visualizing" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/PHATE/).

<!-- -->

-   **PyMDE Preserve Distances (logCP10k)**<sup><a href="/bibliography#agrawal2021mde" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://pymde.org/).

<!-- -->

-   **PyMDE Preserve Distances (logCP10k, 1kHVG)**<sup><a href="/bibliography#agrawal2021mde" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://pymde.org/).

<!-- -->

-   **PyMDE Preserve Neighbors (logCP10k)**<sup><a href="/bibliography#agrawal2021mde" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://pymde.org/).

<!-- -->

-   **PyMDE Preserve Neighbors (logCP10k, 1kHVG)**<sup><a href="/bibliography#agrawal2021mde" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://pymde.org/).

<!-- -->

-   **Random Features**<sup><a href="/bibliography#openproblems" target="_blank">16</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Spectral Features**<sup><a href="/bibliography#openproblems" target="_blank">16</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **True Features**<sup><a href="/bibliography#openproblems" target="_blank">16</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k)**<sup><a href="/bibliography#vandermaaten2008visualizing" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html#sklearn.manifold.TSNE).

<!-- -->

-   **t-Distributed Stochastic Neighbor Embedding (t-SNE) (logCP10k, 1kHVG)**<sup><a href="/bibliography#vandermaaten2008visualizing" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html#sklearn.manifold.TSNE).

<!-- -->

-   **UMAP (logCP10k)**<sup><a href="/bibliography#mcinnes2018umap" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **UMAP (logCP10k, 1kHVG)**<sup><a href="/bibliography#mcinnes2018umap" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **UMAP PCA (logCP10k)**<sup><a href="/bibliography#mcinnes2018umap" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

<!-- -->

-   **UMAP PCA (logCP10k, 1kHVG)**<sup><a href="/bibliography#mcinnes2018umap" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lmcinnes/umap).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Features**: Missing 'method_description'.

<!-- -->

-   **Spectral Features**: Missing 'method_description'.

<!-- -->

-   **True Features**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **Mouse hematopoietic stem cell differentiation**<sup><a href="/bibliography#nestorowa2016single" target="_blank">15</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Mouse myeloid lineage differentiation**<sup><a href="/bibliography#olsson2016single" target="_blank">13</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **5k Peripheral blood mononuclear cells**<sup><a href="/bibliography#10x2019pbmc" target="_blank">14</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Zebrafish**<sup><a href="/bibliography#wagner2018single" target="_blank">12</a></sup>: Missing 'dataset_description'.

</details>
<details>
<summary>
Download raw data
</summary>

<a href="data/task_info.json" class="btn btn-secondary">Task info</a>
<a href="data/method_info.json" class="btn btn-secondary">Method info</a>
<a href="data/metric_info.json" class="btn btn-secondary">Metric info</a>
<a href="data/dataset_info.json" class="btn btn-secondary">Dataset info</a>
<a href="data/results.json" class="btn btn-secondary">Results</a>
<a href="data/quality_control.json" class="btn btn-secondary">Quality control</a>

</details>
<details>
<summary>
Quality control results
</summary>
<table class="table lightable-paper" style='margin-left: auto; margin-right: auto; font-family: "Arial Narrow", arial, helvetica, sans-serif; margin-left: auto; margin-right: auto;'>
 <thead>
  <tr>
   <th style="text-align:left;"> Category </th>
   <th style="text-align:left;"> Name </th>
   <th style="text-align:right;"> Value </th>
   <th style="text-align:left;"> Condition </th>
   <th style="text-align:left;"> Severity </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: dimensionality_reduction
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: dimensionality_reduction
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: dimensionality_reduction
  Field: dataset_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: dimensionality_reduction
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: dimensionality_reduction
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: dimensionality_reduction
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: dimensionality_reduction
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: dimensionality_reduction
  Field: method_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: dimensionality_reduction
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: dimensionality_reduction
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: dimensionality_reduction
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: dimensionality_reduction
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: dimensionality_reduction
  Field: metric_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: dimensionality_reduction
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: dimensionality_reduction
  Field: metric_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method umap_logCP10k performs a lot better than baselines.
  Task id: dimensionality_reduction
  Method id: umap_logCP10k
  Metric id: distance_correlation_spectral
  Best score: 2.0573274891573483%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method umap_logCP10k performs a lot better than baselines.
  Task id: dimensionality_reduction
  Method id: umap_logCP10k
  Metric id: distance_correlation_spectral
  Best score: 2.0573274891573483%
"> Best score umap_logCP10k distance_correlation_spectral </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method umap_logCP10k performs a lot better than baselines.
  Task id: dimensionality_reduction
  Method id: umap_logCP10k
  Metric id: distance_correlation_spectral
  Best score: 2.0573274891573483%
"> 2.057327 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method umap_logCP10k performs a lot better than baselines.
  Task id: dimensionality_reduction
  Method id: umap_logCP10k
  Metric id: distance_correlation_spectral
  Best score: 2.0573274891573483%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method umap_logCP10k performs a lot better than baselines.
  Task id: dimensionality_reduction
  Method id: umap_logCP10k
  Metric id: distance_correlation_spectral
  Best score: 2.0573274891573483%
"> ✗ </td>
  </tr>
</tbody>
</table>

</details>
<details>
<summary>
Visualization of raw results
</summary>

    Warning: Removed 1 row containing missing values (`geom_path()`).

    Warning: Removed 138 rows containing missing values (`geom_point()`).

<img src="index.markdown_strict_files/figure-markdown_strict/raw_results-1.png" width="960" />

</details>
