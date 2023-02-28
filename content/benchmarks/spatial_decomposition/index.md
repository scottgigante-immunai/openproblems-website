---
title: "Spatial Decomposition"
summary: "Calling cell-type compositions for spot-based spatial transcriptomics data"
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

Spatial decomposition (also often referred to as Spatial deconvolution) is
applicable to spatial transcriptomics data where the transcription profile of
each capture location (spot, voxel, bead, etc.) do not share a bijective
relationship with the cells in the tissue, i.e., multiple cells may contribute
to the same capture location. The task of spatial decomposition then refers to
estimating the composition of cell types/states that are present at each capture
location. The cell type/states estimates are presented as proportion values,
representing the proportion of the cells at each capture location that belong to
a given cell type.

We distinguish between *reference-based* decomposition and *de novo*
decomposition, where the former leverage external data (e.g., scRNA-seq or
scNuc-seq) to guide the inference process, while the latter only work with the
spatial data. We require that all datasets have an associated reference single
cell data set, but methods are free to ignore this information.

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="770" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **r2**<sup><a href="/bibliography#miles2005rsquared" target="_blank">1</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-cb75baae28b377419af6" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-cb75baae28b377419af6">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=1, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=200, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Cell2location (detection_alpha=20, reference NB without batch info) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","Cell2location, amortised (detection_alpha=20, reference hard-coded) <sup><a href=\"/bibliography#kleshchevnikov2022cell2location\" target=\"_blank\">2<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","Non-Negative Least Squares <sup><a href=\"/bibliography#aliee2021autogenes\" target=\"_blank\">4<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","Stereoscope <sup><a href=\"/bibliography#andersson2020single\" target=\"_blank\">6<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","Non-Negative Matrix Factorization (NMF) <sup><a href=\"/bibliography#cichocki2009fast\" target=\"_blank\">7<\/a><\/sup>","RCTD <sup><a href=\"/bibliography#cable2021robust\" target=\"_blank\">5<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","NMF-reg <sup><a href=\"/bibliography#rodriques2019slide\" target=\"_blank\">8<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>","Tangram <sup><a href=\"/bibliography#biancalani2021deep\" target=\"_blank\">10<\/a><\/sup>","SeuratV3 <sup><a href=\"/bibliography#stuart2019comprehensive\" target=\"_blank\">9<\/a><\/sup>"],["Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=0.5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Tabula muris senis (alpha=5) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=0.5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Pancreas (alpha=5) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Tabula muris senis (alpha=1) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">12<\/a><\/sup>","Pancreas (alpha=1) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">11<\/a><\/sup>","Overall mean","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>","DestVI <sup><a href=\"/bibliography#lopez2022destvi\" target=\"_blank\">3<\/a><\/sup>"],[0.929680772309262,0.925876660204544,0.925560259977039,0.924542681560651,0.924062466633372,0.913364072999505,0.912861307440742,0.912594277476491,0.912262869426645,0.912223473608386,0.91221391182389,0.910931682564593,0.90765012628091,0.900926504220092,0.900788191610969,0.900428857836666,0.891213927324339,0.870806750684175,0.869376084095192,0.869315354624464,0.866515620078981,0.858409794267454,0.853825946388012,0.853614648542271,0.852456414011013,0.848170213507334,0.844091846912841,0.841893069465698,0.841784713649959,0.840868854720932,0.830183370460417,0.828353969263217,0.813804766818375,0.806490483174224,0.765422928803302,0.764774624558863,0.764579053396944,0.762856913088324,0.760038532235312,0.757352701113686,0.748611363419125,0.746137471116146,0.74296034208539,0.738302492182609,0.733706796153313,0.732266215956394,0.720396756364459,0.719290320185536,0.714759866513875,0.711578220125039,0.709505809839684,0.683845522100175,0.68326385690036,0.670228765619469,0.670202765631377,0.669198257859164,0.65732179772213,0.648069804085473,0.645284503086297,0.642980795897815,0.632692754033841,0.632036488399979,0.596447915636559,0.580167326464707,0.57724683688478,0.574175319142238,0.565322653268171,0.560593080060308,0.559727949153353,0.529428618853124,0.522199047362362,0.516544783049756,0.509130032614993,0.5062843876079,0.494157022767787,0.465776095609513,0.430952099657254,0.421008139949226,0.398930665926777,0.338407960927012,0.334350215555255,0.224677075079343,0.180374630371125,0.16824737874224,0.113816003952863,0.0910168805310615,0.0714113681675428,0.0670943343106955,-0.142761748984467,-0.160067335308539,-0.163079392405294,-0.177596714035102,-0.194704478597087,-0.196472679951363,-0.207166160787635,-0.207777950736167,-0.267146128421899,-0.508513593131604,-0.531444766834243,-0.614982949875505,-0.677763754898386,-0.900439182406306,-2.63833219307876,-4.84769467992547],[0.929680772309262,0.925876660204544,0.925560259977039,0.924542681560651,0.924062466633372,0.913364072999505,0.912861307440742,0.912594277476491,0.912262869426645,0.912223473608386,0.91221391182389,0.910931682564593,0.90765012628091,0.900926504220092,0.900788191610969,0.900428857836666,0.891213927324339,0.870806750684175,0.869376084095192,0.869315354624464,0.866515620078981,0.858409794267454,0.853825946388012,0.853614648542271,0.852456414011013,0.848170213507334,0.844091846912841,0.841893069465698,0.841784713649959,0.840868854720932,0.830183370460417,0.828353969263217,0.813804766818375,0.806490483174224,0.765422928803302,0.764774624558863,0.764579053396944,0.762856913088324,0.760038532235312,0.757352701113686,0.748611363419125,0.746137471116146,0.74296034208539,0.738302492182609,0.733706796153313,0.732266215956394,0.720396756364459,0.719290320185536,0.714759866513875,0.711578220125039,0.709505809839684,0.683845522100175,0.68326385690036,0.670228765619469,0.670202765631377,0.669198257859164,0.65732179772213,0.648069804085473,0.645284503086297,0.642980795897815,0.632692754033841,0.632036488399979,0.596447915636559,0.580167326464707,0.57724683688478,0.574175319142238,0.565322653268171,0.560593080060308,0.559727949153353,0.529428618853124,0.522199047362362,0.516544783049756,0.509130032614993,0.5062843876079,0.494157022767787,0.465776095609513,0.430952099657254,0.421008139949226,0.398930665926777,0.338407960927012,0.334350215555255,0.224677075079343,0.180374630371125,0.16824737874224,0.113816003952863,0.0910168805310615,0.0714113681675428,0.0670943343106955,-0.142761748984467,-0.160067335308539,-0.163079392405294,-0.177596714035102,-0.194704478597087,-0.196472679951363,-0.207166160787635,-0.207777950736167,-0.267146128421899,-0.508513593131604,-0.531444766834243,-0.614982949875505,-0.677763754898386,-0.900439182406306,-2.63833219307876,-4.84769467992547],[6178,6904,11990,6733,21590,4669,26560,24710,28349,22909,23159,23700,4501,3959,3738,9880,429,6605,16090,17769,19219,25550,17183.4285714286,13350.5714285714,13026.4285714286,14441.2857142857,15024,9709,9040,8338,11129,11930,159,13145,18869,10238,19360,25460,10149,19539,15177,16269,20899,25819,8942,21339,12289,14780,460,987,420,1258,2619,7421,1460,412.285714285714,16729,450,1267,644,1138,3807,538,439,3048,1032,1231.42857142857,579,1990,319,1027,569,530,319,1340,540,330,426.857142857143,480,1990,540,180,588.428571428571,470,1039,699,669,923,591,798,529,469,529,439,699,759,679,649,943.571428571429,708,549,748,3349,939],[1892.2,1393,1369,1242.4,1345.2,1951.5,1909,1887.7,2009.5,2072,2039.5,2259.9,1461.6,1272.7,1326.8,1342.5,14.4,1312.7,1367.1,1502,1287,1904.8,1423.47142857143,1462.78571428571,1412.27142857143,1557.65714285714,1912.01428571429,1297.2,1241.7,1480.7,1549.1,1889.6,58.7,2316.3,1315,1263.7,1319.4,1393.3,1492.4,1299.9,1565.6,2243.21428571429,1544.6,2293.2,1920.5,1916.5,2164.3,2321,10.6,41.4,28.3,729.8,26,2176.3,588.1,38.1285714285714,2171.5,139.7,30.6,336.6,39.8,424.2,51.2,87.1,489.7,28.4,38.2,382.4,538.371428571429,65.6,693.1,17,72.3,369,657.4,581.8,1143.7,332.657142857143,372.3,186.3,185.5,278.1,379.128571428571,112.1,50,135.2,274.4,136.9,491.3,121.6,524.4,358.4,176.1,219.5,190.6,369.1,134.7,144.8,347.985714285714,350.7,114.4,129.314285714286,475.6,117.6],[15.52734375,3.125,1.171875,1.171875,3.3203125,17.67578125,40.33203125,5.078125,5.17578125,5.078125,5.078125,21.6796875,3.125,4.58984375,1.171875,4.78515625,0.2314453125,1.85546875,1.171875,3.125,3.41796875,17.48046875,2.74832589285714,1.79966517857143,2.58091517857143,4.58984375,20.1032366071429,1.26953125,1.26953125,1.26953125,6.0546875,17.1875,0.26123046875,16.0156249990234,1.46484375,1.26953125,1.5625,1.26953125,1.26953125,1.26953125,5.859375,17.1037946427176,5.76171875,15.72265625,16.40625,16.11328125,16.796875,15.72265625,0.22138671875,4.19921875,0.8244140625,1.3671875,2.34375,17.08984375,1.26953125,0.539536830357143,16.69921875,0.82578125,4.19921875,2.24609375,4.19921875,1.3671875,2.34375,0.64306640625,1.3671875,2.34375,3.40401785714286,0.82509765625,1.33928571428571,0.1427734375,1.171875,0.8259765625,1.26953125,1.3671875,1.26953125,1.3671875,0.82548828125,0.810797991071429,1.46484375,1.5625,1.26953125,0.643359375,2.46930803571429,0.64326171875,4.19921875,24.31640625,3.61328125,25.87890625,0.9765625,18.84765625,1.26953125,1.26953125,0.9765625,1.3671875,0.9765625,3.61328125,21.6796875,70.3125,1.42299107142857,3.61328125,13.18359375,34.4866071428571,3.125,67.1875]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>r2<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **Cell2location, amortised (detection_alpha=20, reference hard-coded)**<sup><a href="/bibliography#kleshchevnikov2022cell2location" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/BayraktarLab/cell2location).

<!-- -->

-   **Cell2location (detection_alpha=1, reference hard-coded)**<sup><a href="/bibliography#kleshchevnikov2022cell2location" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/BayraktarLab/cell2location).

<!-- -->

-   **Cell2location (detection_alpha=20, reference hard-coded)**<sup><a href="/bibliography#kleshchevnikov2022cell2location" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/BayraktarLab/cell2location).

<!-- -->

-   **Cell2location (detection_alpha=200, reference hard-coded)**<sup><a href="/bibliography#kleshchevnikov2022cell2location" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/BayraktarLab/cell2location).

<!-- -->

-   **Cell2location (detection_alpha=20, reference NB without batch info)**<sup><a href="/bibliography#kleshchevnikov2022cell2location" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/BayraktarLab/cell2location).

<!-- -->

-   **DestVI**<sup><a href="/bibliography#lopez2022destvi" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **Non-Negative Matrix Factorization (NMF)**<sup><a href="/bibliography#cichocki2009fast" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.NMF.html).

<!-- -->

-   **NMF-reg**<sup><a href="/bibliography#rodriques2019slide" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/tudaga/NMFreg_tutorial).

<!-- -->

-   **Non-Negative Least Squares**<sup><a href="/bibliography#aliee2021autogenes" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.nnls.html).

<!-- -->

-   **Random Proportions**<sup><a href="/bibliography#openproblems" target="_blank">13</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **RCTD**<sup><a href="/bibliography#cable2021robust" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/dmcable/spacexr).

<!-- -->

-   **SeuratV3**<sup><a href="/bibliography#stuart2019comprehensive" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://satijalab.org/seurat/archive/v3.2/spatial_vignette.html).

<!-- -->

-   **Stereoscope**<sup><a href="/bibliography#andersson2020single" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/scverse/scvi-tools).

<!-- -->

-   **Tangram**<sup><a href="/bibliography#biancalani2021deep" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/broadinstitute/Tangram).

<!-- -->

-   **True Proportions**<sup><a href="/bibliography#openproblems" target="_blank">13</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Proportions**: Missing 'method_description'.

<!-- -->

-   **True Proportions**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **DestVI**<sup><a href="/bibliography#lopez2022destvi" target="_blank">3</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (alpha=0.5)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">11</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (alpha=1)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">11</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (alpha=5)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">11</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Tabula muris senis (alpha=0.5)**<sup><a href="/bibliography#tabula2020single" target="_blank">12</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Tabula muris senis (alpha=1)**<sup><a href="/bibliography#tabula2020single" target="_blank">12</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Tabula muris senis (alpha=5)**<sup><a href="/bibliography#tabula2020single" target="_blank">12</a></sup>: Missing 'dataset_description'.

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
  Task id: spatial_decomposition
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: spatial_decomposition
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: spatial_decomposition
  Field: dataset_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: spatial_decomposition
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: spatial_decomposition
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: spatial_decomposition
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: spatial_decomposition
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: spatial_decomposition
  Field: method_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: spatial_decomposition
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: spatial_decomposition
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: spatial_decomposition
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: spatial_decomposition
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: spatial_decomposition
  Field: metric_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: spatial_decomposition
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: spatial_decomposition
  Field: metric_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method seuratv3 performs much worse than baselines.
  Task id: spatial_decomposition
  Method id: seuratv3
  Metric id: r2
  Worst score: -2.577283361629789%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method seuratv3 performs much worse than baselines.
  Task id: spatial_decomposition
  Method id: seuratv3
  Metric id: r2
  Worst score: -2.577283361629789%
"> Worst score seuratv3 r2 </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method seuratv3 performs much worse than baselines.
  Task id: spatial_decomposition
  Method id: seuratv3
  Metric id: r2
  Worst score: -2.577283361629789%
"> -2.577283 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method seuratv3 performs much worse than baselines.
  Task id: spatial_decomposition
  Method id: seuratv3
  Metric id: r2
  Worst score: -2.577283361629789%
"> worst_score &gt;= -1 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method seuratv3 performs much worse than baselines.
  Task id: spatial_decomposition
  Method id: seuratv3
  Metric id: r2
  Worst score: -2.577283361629789%
"> ✗✗ </td>
  </tr>
</tbody>
</table>

</details>
<details>
<summary>
Visualization of raw results
</summary>

<img src="index.markdown_strict_files/figure-markdown_strict/raw_results-1.png" width="960" />

</details>
