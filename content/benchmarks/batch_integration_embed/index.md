---
title: "Batch integration embed"
summary: "Removing batch effects while preserving biological variation (embedding output)"
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

<!--- TODO: add links --->

## The task

This is a sub-task of the overall batch integration task. Batch (or data) integration
integrates datasets across batches that arise from various biological and technical
sources. Methods that integrate batches typically have three different types of output:
a corrected feature matrix, a joint embedding across batches, and/or an integrated
cell-cell similarity graph (e.g., a kNN graph). This sub-task focuses on all methods
that can output joint embeddings, and includes methods that canonically output corrected
feature matrices with subsequent postprocessing to generate a joint embedding. Other
sub-tasks for batch integration can be found for:

-   [graphs](../batch_integration_graph/), and
-   [corrected features](../batch_integration_features)

This sub-task was taken from a
[benchmarking study of data integration
methods](https://openproblems.bio/bibliography#luecken2022benchmarking).

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="902" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **ARI**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Cell Cycle Score**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Graph connectivity**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Isolated label F1**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Isolated label Silhouette**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **kBET**<sup><a href="/bibliography#bttner2018test" target="_blank">2</a></sup>: Missing 'metric_description'.

<!-- -->

-   **NMI**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **PC Regression**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Silhouette**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Batch ASW**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-c9fb623f4b312d1bf7e4" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-c9fb623f4b312d1bf7e4">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">8<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">6<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">5<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">3<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">9<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>"],["Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>"],[0.712641370606311,0.71237662475037,0.702396403342601,0.692912904773849,0.690639027451313,0.68201745886261,0.681243360635646,0.680742077551287,0.668633990739888,0.668142596576756,0.666029622810062,0.659560391032513,0.65544703864264,0.655336115131479,0.652317783263478,0.651437238180128,0.643026101463514,0.642982433002048,0.640741127591843,0.639831240314927,0.637854084252294,0.637154817314615,0.636398445250228,0.634573678157009,0.63217054015795,0.629579943062838,0.629414722995915,0.62930408642947,0.628623302371467,0.628126677247396,0.627331440400608,0.625929247771975,0.625564029343056,0.624213738169177,0.623689451484735,0.620450611708523,0.620008405743323,0.614844501799567,0.614365687654311,0.614281702387723,0.614070874715389,0.61257016720687,0.612330183605833,0.612310687598206,0.611427108404053,0.609466599011854,0.60936746424926,0.606945889032317,0.606196927040954,0.60518260405076,0.60517150353903,0.603791497369687,0.596469788036964,0.596336587323825,0.595622644554904,0.594615367238281,0.594137321545062,0.593989689579093,0.593119633019643,0.592800560933127,0.592068846600761,0.591990939876335,0.591127469044097,0.589637860032153,0.589282095578904,0.58814026946168,0.586797356926096,0.585878940221216,0.583845213297255,0.583353411516457,0.581082522156266,0.579156394535143,0.57599235793272,0.574727463109753,0.572589670226782,0.57240300820247,0.572193753153784,0.57088946322834,0.570464507943614,0.568300563712471,0.567230798514702,0.56376691864194,0.561955669514348,0.560702065392149,0.558503303917926,0.551125136844359,0.550160463924096,0.549380429643076,0.54857417769945,0.547276212287346,0.547090644474471,0.546103476548524,0.544915588364977,0.540733021321132,0.537476111372354,0.533755657362766,0.532946630586417,0.529607616171146,0.523699351491718,0.521551760014941,0.520646923281633,0.520389268170517,0.518362799597133,0.5172057115172,0.516183658789206,0.515382873850847,0.514182495683055,0.510544628890526,0.510036662040873,0.507338668066202,0.50506240367461,0.503393086955751,0.499041934911395,0.48345097318752,0.481369400819927,0.480777764976286,0.475814360932105,0.474593290374694,0.474253557982661,0.470237654505132,0.46322019333154,0.454587289687222,0.423071002722475,0.386222195049251,0.381733720459861,0.375664709344254,0.228108764378182,0.210404788630882],[0.944771200033903,0.944783156042593,0.94438759927174,0.906346356654058,0.942350591085936,0.947582158839779,0.904175457268052,0.948316231587251,0.847457757557665,0.9485439116014,0.944772736128615,0.884761520173224,0.953621515332102,0.824617032748088,0.716748854465712,0.879071992379126,0.867728059543211,0.844066746541777,0.81533393484829,0.944967582345794,0.950268519532374,0.841982684870931,0.746894133268973,0.918549010714758,0.926820914436892,0.79338330097484,0.722781376379514,0.714319396876895,0.697151822279303,0.785782171177023,0.713079385975077,0.780374217020839,0.77577333567933,0.778280539695365,0.753387012202225,0.756030561841191,0.842662032622315,0.673809699757411,0.698570738247986,0.744550410910099,0.764801143124305,0.703142457127648,0.690837474382518,0.912620514798665,0.779865327913535,0.955629189435981,0.704584335644806,0.733231867942189,0.737066720957725,0.758061502464934,0.595250898290923,0.682816050747955,0.659009622841577,0.749093542285998,0.799725851812297,0.883889316263747,0.692131382902639,0.562751262733426,0.891386471579295,0.644424378720404,0.574540101892011,0.705855023918323,0.882887340781314,0.682814197810288,0.606597054604415,0.549278015713805,0.550426179933088,0.6044252371078,0.77029586966485,0.701399251386487,0.589163969934536,0.513790310939634,0.73186196573501,0.703664013433633,0.493774780878605,0.502882292700192,0.745548399896117,0.515525026743487,0.68336435052811,0.603545293031209,0.697803117698125,0.592509226495449,0.752231381944729,0.722219329145093,0.465920641466197,0.495111543666085,0.685399337935761,0.460394146046204,0.695094734686687,0.476819519435264,0.626184570453833,0.622408047195273,0.492146070496039,0.658856597509895,0.479124151119447,0.520880562943154,0.417294881736071,0.581223506336902,0.646300766119576,0.620646764270799,0.325175146762175,0.592893570654247,0.461588745988094,0.460902785634702,0.646631093968729,0.480299638349372,0.626005192092723,0.438598912661242,0.576198624775946,0.399923232774236,0.6010909901281,0.530665343175813,0.519263473720297,0.506766022897469,0.432949576492976,0.50133910458591,0.506399512385444,0.4905620199259,0.491782102397559,0.434576828145041,0.480864366157409,0.477575279913343,0.365090112194406,0.375801080900029,0.386144023626927,0.307801009242876,0.0519134031487777,0.0875362552940661],[0.866778910959157,0.899095348177301,0.86324912752735,0.681641403152299,0.723736648022746,0.673422996976239,0.716144974324424,0.578248614199418,0.844376390444308,0.605748805880914,0.611169668121434,0.682380530984776,0.436515848010508,0.465154901101698,0.868181330076587,0.738157752001577,0.594715715410352,0.624830242136964,0.677386228028257,0.38663964311763,0.0400943326271703,0.542761450884785,0.693490766504949,0.636655957379823,0.643063766538126,0.645197257009557,0.795163280449705,0.813287641063035,0.7479330924209,0.446461244408304,0.82533055740713,0.63394872226058,0.581763812645309,0.56799896471538,0.705960596514058,0.791987499583416,0.643064466924957,0.789841018328401,0.792755860300287,0.449931908577786,0.66525076723577,0.725004129699711,0.675074232355942,0.0317691222911664,0.243665752007187,0.0492341246612833,0.530584168528399,0.793702730469513,0.790793533239948,0.741139378624237,0.884799129434387,0.713387258438503,0.770972626502704,0.738129210898388,0.427515447967515,0.333508748106955,0.741118893228136,0.801503964444367,0.0477766294072944,0.85484328391013,0.639971023000254,0.241216075192649,0.33350571854521,0.722702529225616,0.617897661746563,0.774794203489614,0.757899260783911,0.771828762514716,0.73279224707367,0.676819636582603,0.488924512804937,0.657245237689966,0.427727189683088,0.73266359440065,0.907622324424872,0.90758414772476,0.686183025430868,0.547428229076967,0.703992834174817,0.244441678986087,0.457275761005104,0.858523120257987,0.257253710919234,0.381572220558888,0.580827073588883,0.62423224103994,0.247029324153734,0.241947194708996,0.589089054749381,0.777213572119995,0.640060797534396,0.640118744590812,0.784112683367688,0.0583645700078345,0.407076899516782,0.819418663329819,0.798956042702289,0.621974189853271,0.0139856617297612,0.251159446813352,0.453511973050295,0.233016209343523,0.626428889769237,0.747969779177605,0.0775946092865409,0.698207705497129,0.814173596058646,0.390776426881703,0.813807423048856,0.503738954703603,0.049106027622489,0.259070011538982,0.244633196677807,0.308838998448702,0.26558415337082,0.295011560128904,0.615807603722242,0.679228190802355,0.679089496771475,0.227787205295703,0.313541549873335,0.27771666289415,0.436952635055307,0.249463918154863,0.336197298382811,0.393780936850947,0.128582571775292,0.170038922244187],[0.992224214808968,0.993158988239297,0.993780766580945,0.981933577799365,0.992356307992578,0.994056912009167,0.988792400201138,0.992104894967444,0.994169373364254,0.995122134499819,0.995875902619918,0.978574061666863,0.994762334165101,0.984349858567528,0.960495131367395,0.984082988605912,0.986989751557148,0.987209917589916,0.983811393035803,0.994710064638003,0.994425202710708,0.985783544335781,0.98019854582558,0.987716749284766,0.94306657648511,0.978832172808801,0.936344583055069,0.990730615893475,0.978968662003452,0.973403737155852,0.974610159961925,0.972330036756183,0.985472970634172,0.986466343013904,0.969380464816063,0.971841782429996,0.939293396773472,0.987072718664944,0.975702835828711,0.98740915424268,0.987632858839478,0.939060764348882,0.968298752759253,0.992929941698455,0.972003667575999,0.994137253169264,0.982424629664018,0.962580823197552,0.952567029163173,0.955816526451988,0.890356779753995,0.987362030909015,0.929976511779822,0.934780971503086,0.89901871546312,0.948128313479644,0.955263101745613,0.981255527977659,0.988221846625954,0.947972360084417,0.980877571367907,0.976027065430008,0.946906746660912,0.952708959024676,0.92577961205328,0.970447262111609,0.982077353220412,0.955822646899359,0.957594259054408,0.970272337246214,0.981710836473796,0.977896087864427,0.913071162441264,0.955772551506354,0.946335521021309,0.94639696099341,0.93511741028746,0.975106612481261,0.954989315516878,0.948182062861436,0.940138645615905,0.960588216099858,0.932304493040452,0.895559674266797,0.980862834488771,0.955392784473356,0.915881906409654,0.947742100348889,0.867551337472715,0.988080120627126,0.954902110942813,0.955249713070257,0.985571932497788,0.984310112109173,0.919038390483765,0.930359462393093,0.972950567103004,0.967277615554516,0.979543850540091,0.910128248341665,0.931622940350498,0.929847110107143,0.958852577240857,0.914345161356014,0.982086794994094,0.898904132192212,0.973899674226125,0.770650602701489,0.972761155999978,0.902632197838316,0.987183605072056,0.89443770208049,0.90792283129226,0.930575708545888,0.846352710161743,0.903757510488973,0.874592856349001,0.97250687152855,0.970181058355384,0.869858834165433,0.850514958649024,0.817546498320958,0.70859981287398,0.690919792416482,0.632615020967284,0.67936537123498,0.45490344448196,0.339373933012656],[0.924998177678624,0.95262933177622,0.925559108542813,0.802476155247118,0.816270707822077,0.954596842325979,0.822687269309489,0.949440444154631,0.926173522376154,0.940868253228597,0.938635769849533,0.853705708696882,0.950838566600603,0.926422813334214,0.833935923048197,0.76393253748331,0.884856937385638,0.86641286789073,0.830686649370721,0.947723933526461,0.952278423754417,0.884689661691883,0.864594906385933,0.689032356836264,0.844603102984613,0.811206726785137,0.742914103551136,0.852996675314942,0.857156825384059,0.839196145753472,0.802600692054881,0.846302437754835,0.867575223629084,0.874219787018746,0.813846537260675,0.571114648391907,0.84469145194189,0.842833518044902,0.733124844086243,0.840609600813396,0.85002653685943,0.613000607460214,0.818164321122899,0.955705591119453,0.893559590695898,0.953141512405022,0.894437812960282,0.717436553809577,0.770858804071252,0.723233771017736,0.689905776640598,0.814397125587628,0.799105970459625,0.784271637675678,0.810259551724511,0.773168988695132,0.723744188365626,0.707827529951715,0.94784852520931,0.764260204257778,0.844248778159056,0.888292081175515,0.741813741178007,0.808291081468436,0.64926431169376,0.633360693000115,0.717982763364051,0.76234675901062,0.762472336320891,0.54250829722045,0.852883174252583,0.733782259238094,0.820790035201821,0.769985160109663,0.733416504704563,0.721721004913844,0.715385069574672,0.794852949626744,0.734341767716378,0.889204202579805,0.802933693304543,0.179636683544067,0.83195165602674,0.833333201073161,0.700790150583095,0.56089874190451,0.870503131021699,0.868561051593696,0.584543596120419,0.745170206374493,0.709407206091253,0.702422504114209,0.70550503975606,0.918515607161958,0.852629650271029,0.672193164960458,0.332363896714055,0.176145775814467,0.926813662324748,0.859245095542966,0.726922386571632,0.847223600206288,0.222648995055655,0.867844207379439,0.78914572168134,0.293611563582386,0.719580134960323,0.851827517629532,0.741519840021471,0.331464345106467,0.848898664204781,0.815990151411069,0.856106018115436,0.806997214922336,0.842870832653967,0.732453903950687,0.43491065416102,0.632037266460058,0.633331624664782,0.811923444989573,0.825886478393779,0.866789739870498,0.57534641799531,0.611625788318412,0.434121757764716,0.383406687032594,0.139962988941454,0.106195888855318],[0.388000266584759,0.47947044845944,0.352944740104622,0.375534544860821,0.301731215540694,0.314321077184883,0.294545564688847,0.346976688370107,0.409947066655687,0.375741240500805,0.356951184922772,0.343639930714828,0.427962145241505,0.34079035395056,0.179962452356889,0.304595313995925,0.360981311430432,0.328582825959055,0.323824479585231,0.365917136685673,0.462713988293165,0.324455521563712,0.354337816214398,0.190980538469657,0.283569306985038,0.298287375521013,0.20783550300866,0.239001064708084,0.311382301611726,0.252798832820793,0.280734787563412,0.262420304192102,0.301456292125679,0.31337751555973,0.258283703016565,0.242742199533707,0.283565816213468,0.332975180763652,0.186125950223409,0.223430903732847,0.311341858334963,0.250639596463388,0.313867028845657,0.358783097182466,0.312435151704441,0.38086805016631,0.305411923380435,0.20297321907634,0.211436978469692,0.228427830692514,0.151523986871425,0.235669049004538,0.263888307524291,0.186321726798315,0.275799171729369,0.224600265342561,0.22843376898519,0.241552693881273,0.594309215010141,0.219170337350691,0.250390930408287,0.273592324493226,0.224605131599049,0.283828293688421,0.251505032586437,0.17794768425881,0.270089285234922,0.18995024866503,0.179786174215218,0.185103090906272,0.249130315933252,0.18492314192722,0.256999173854089,0.179688267899096,0.211365624364916,0.211322270498754,0.159914692044818,0.321122695991652,0.196660876654631,0.221792633999366,0.214496872165232,0.223522163984088,0.313604443431863,0.330393491862334,0.363391701827798,0.115876508580841,0.401632702648397,0.238562972564365,-0.0442165784369722,0.277596174023541,0.143241433362074,0.143347534542156,0.143550560741818,0.469607168897431,0.293462828961684,0.0863959767794972,0.168957458492321,0.174378485584131,0.41942610838581,0.414837217901919,0.0608600223143185,0.326830853023767,0.100643553204796,0.360278439721786,0.37509078375519,0.168548741520683,0.0273613849681005,0.271977851928268,0.0270652184986284,0.262200756937326,0.292386416767155,0.347050253957889,0.271716940039432,0.394082126190209,0.353589719080961,0.284146108399909,-0.146343148618236,-0.00592815233749848,-0.00619823575509178,0.346569578520259,0.444510992945992,0.229301574389456,0.0669585067155461,-0.0147474565739425,0.0319572280665081,0.0284721475091292,0.164801084430077,0.154835719210439],[0.454646553710639,0.13850520626873,0.115413371912061,0.542012903260928,0.263126844282936,0.190819168763083,0.453416031375079,0.141617086358629,0.140051318329978,0.258496067984833,0.264312267025797,0.21186157327762,0.288579008829194,0.473473933826281,0.260912247363777,0.230846626771184,0.226384503721656,0.232729158435593,0.219685077229188,0.27874157735755,0.306352378846047,0.170698039357004,0.118150164784683,0.269258048461131,0.370840313711787,0.23111369616441,0.342418188942296,0.130330533920185,0.136868019934985,0.297546814507613,0.0609898897506225,0.13104082968938,0.235338067581912,0.244426373404446,0.0835108508010874,0.213518152116105,0.371220923507612,0.110451712604474,0.127531677130001,0.227023467323389,0.178712929058153,0.450688572932459,0.0984842684378951,0.233089342982829,0.262084094359719,0.216446832677866,0.208844780550761,0.0777891285968288,0.292912459247472,0.251006267233074,0.326255894683385,0.125358145674909,0.0405572034743424,0.0308147723988175,0.177771161204538,0.336074117733334,0.247481012372162,0.0781006936458155,0.256030405545036,0.0129484379256964,0.2348524656266,0.207667458653151,0.335756207952417,0.222841799926198,0.41363872139316,0.290638967511639,0.0546078594141099,0.0949395446674295,0.259548338553888,0.222829456008391,0.210588239555529,0.418619168525139,0.176676137866037,0.257970319119141,0.320924525731975,0.317862923632393,0.120392374883675,0.0849044583959401,0.106092072227792,0.182353089725497,0.182886657654743,0.299638483468551,0.164220906573049,0.119923700400715,0.0640764330762601,0.290472719466569,0.190878209000356,0.162889565653236,0.509335871365008,0.0544357995484602,0.268157144177063,0.269282242685642,0.0750458637475388,0.191922315682166,0.148189243320364,0.303698449148102,0.192385486646003,0.304290774896611,0.217353958724288,0.12556287984744,0.49044698897052,0.171820605573941,0.253439492299185,0.109017296175723,0.156725062038006,0.467634626594153,0.156798434716802,0.181430513989418,0.155209021477647,0.441186335669813,0.20127023343312,0.137291424750211,0.143871349984797,0.0737186982232094,0.139928083589994,0.0984447258367416,0.417911166392959,0.151165994372533,0.150534391165461,0.115221200342793,0.0648426234594406,0.0821545732009073,0.242209186367535,0.277334243979165,0.331871777238745,0.261362674583436,0.123967670989814,0.208945216372062],[0.91692984365783,0.914894775947522,0.908682569103518,0.875586478024477,0.907272739165741,0.918473188816174,0.862417734790781,0.918791474388954,0.879441125590448,0.920748908446912,0.912877234568363,0.851820626485238,0.924367792703928,0.805880582937519,0.777894527442712,0.839800219184444,0.871213576781529,0.85406590745695,0.802105150369166,0.912462179271121,0.92092040080567,0.867772095036217,0.814818742631615,0.863643737416729,0.875644394248496,0.793172861240116,0.753688536581859,0.79121191111724,0.786620084211387,0.817876850015472,0.789609618793781,0.80863101221201,0.818290115030638,0.817244339972454,0.801701606414614,0.81452116309812,0.84150665219741,0.801687843828155,0.746571611146617,0.794270900350482,0.837452311155419,0.751544612031677,0.793288172769175,0.863581634439485,0.822021379412668,0.930355532358132,0.801648594739494,0.770851789828787,0.783552008123222,0.799294896577699,0.717183834204203,0.79422759733329,0.752687669329412,0.766878252221626,0.835643002787831,0.832175918758445,0.75837650111103,0.719435092633263,0.884874618522763,0.752107044349199,0.737165690277074,0.791051551985606,0.831194629224091,0.751015194662888,0.692743971207687,0.648797133805653,0.708039242928627,0.73344118189115,0.801756792131357,0.779682324996775,0.748820249283435,0.540874217992475,0.795949343071507,0.773046082606952,0.665291374217449,0.669032461899621,0.764261326791524,0.720930439735315,0.715418156606184,0.727266887416861,0.745852920200932,0.765438960299832,0.832847114997077,0.78895511310554,0.70870366016194,0.615816983709425,0.787097231361536,0.71530212116685,0.742509853787619,0.739002321682631,0.732757627396125,0.732013905904477,0.723698785846414,0.833251516503162,0.702158244360368,0.669464853920312,0.627622655981773,0.741962055682445,0.743770978012667,0.782177171605456,0.470792030751217,0.718385430450969,0.630087309230441,0.675209692591697,0.803079774829811,0.625358821488695,0.730331085567877,0.704148089264568,0.719255094512416,0.555167496481339,0.775209536889486,0.743139944290335,0.731178263415979,0.722191968776626,0.680467732490337,0.732542809845267,0.659443574532257,0.699555714271891,0.69706450153031,0.665532393139307,0.724324885207666,0.716167008998081,0.359483943253678,0.376474579678536,0.438873339510539,0.403515390602881,0.191618654022707,0.197635585065461],[0.739346508049499,0.84089231622797,0.9999561615494,0.885061577229264,0.998815160852434,1,0.91704973312825,0.999975759278429,0.670473137810025,0.887331140021786,0.89839131409157,0.913969777433702,0.79072089375738,0.96782085760858,0.95859562830265,0.918614928900698,0.81194601282983,0.894223299305534,0.932181932187105,0.819317708922467,0.805491549939534,0.850978614892259,0.871567684057098,0.999944601387756,0.700181026889081,0.936025083201114,0.939235589277272,0.882350765805029,0.864684956537832,0.913593513670146,0.999967559328457,0.92464266771426,0.920179554794018,0.876067962701774,0.99996338177752,0.998310307191021,0.700161838194794,0.688809102846447,1,0.937511498378698,0.731147367298408,0.86440628650741,1.00000000003407,0.856130087257569,0.868978391957514,0.582132979439182,0.876723828994117,0.99920083462852,0.726715035468929,0.859879861400555,0.964329164516699,0.813175904540932,1,0.99999649859302,0.805498472195192,0.864227017099767,0.859897588932627,0.999917887461111,0.734883998089955,0.999991703447003,0.87670424699575,0.89400275624463,0.86421844329069,0.726599286955192,0.945307147235969,0.964583979025961,0.999954812988967,0.99984283198309,0.670659925976067,0.999759536286127,0.92612226708937,0.980085850010523,0.894525882978232,0.670824466713788,0.811107052529213,0.811126434995023,0.881848275011379,0.849168068229062,0.940244570173553,0.887850112262861,0.927425482862192,0.99691492609211,0.563381394886321,0.801984147340401,1.00000000010221,0.999999999520946,0.757166895563432,0.888366683097624,0.933240949814129,0.531269214191483,0.770897160576911,0.770884653783347,0.706198332925507,0.532587507828371,0.689161143248102,0.55895032334591,0.95507045876471,0.999491175487537,0.765021756991537,0.544916467984874,1,0.815285577295637,0.999999998562837,0.322503557563773,0.612943546090306,0.768921693015695,0.451918889638566,0.644430958315767,0.452413973013943,0.903771419582629,0.461149394786329,0.56259158129716,0.458136316077021,0.430400239485408,0.64209080562211,0.302512733024588,0.945027473084299,0.637328465530138,0.637338029635945,0.753409492033181,0.30017774878585,0.224098410196632,0.945233275685119,0.880277085881622,0.879221052364037,0.912731390768641,0.847933423536506,0.82414512139636],[0.362746828638276,0.315858644163512,0.304683663141521,0.372320284174014,0.353707467260739,0.315835190548345,0.250095401048759,0.285849498682037,0.330235900719459,0.250553576399808,0.231922141507156,0.315965141563257,0.274269915590044,0.259607352063516,0.199602513956555,0.289878841375679,0.3045536763518,0.268018366932937,0.231930369732499,0.231890865485538,0.313931701340648,0.271615643841563,0.278617440753231,0.259524059019879,0.558632915263047,0.229091819193367,0.221675354996622,0.256850966478182,0.271719980698938,0.230813184676866,0.259253889748161,0.257564206134633,0.223109858941816,0.226581749144561,0.244930894862664,0.295532154546012,0.558632890208447,0.296406782909939,0.180083506278488,0.215057855251502,0.323425971902099,0.270105924971317,0.27131364803713,0.22141895151324,0.260631350773724,0.318373975339018,0.263622683023323,0.253225118138954,0.276513122316014,0.274614259062133,0.226441078982507,0.253548431509986,0.238626613305482,0.203846587784535,0.26258756349335,0.497564667119367,0.274604757419164,0.24509659812142,0.386807653004417,0.222017671715131,0.215924012215645,0.215577077725469,0.497557472208109,0.1889186320229,0.215655957612233,0.143871672885211,0.251060334387831,0.226031773528509,0.373966848713895,0.236762849419912,0.208315616124924,0.0823344886948303,0.280972163734022,0.37397963596692,0.171777290042725,0.171770603131774,0.224731503074171,0.262429471961547,0.185636399939302,0.237149166303657,0.234135135045763,0.279663878238343,0.279528008703846,0.306400114088951,0.259479140257562,0.155342215307183,0.305810352957247,0.210254426411665,0.233250229972824,0.287264467311421,0.282943754848389,0.282949948084482,0.232178684210214,0.363230321377855,0.218104992750671,0.242061035235595,0.149678016004247,0.224732715711349,0.222037639882568,0.318941828135989,0.103904103201131,0.214182459711665,0.18203903644193,0.131024095080639,0.307195077341935,0.216322135743316,0.288653371816504,0.227286510865823,0.288701260273148,0.160919441790677,0.212362512058428,0.26856939829425,0.204599829039499,0.271226606674992,0.249651242133301,0.25762248727917,0.163929096430591,0.179515082002611,0.179495994294028,0.186374604206664,0.287195048941162,0.183331982309398,0.122949865697094,0.125694356605196,0.122787041741282,0.096952813186035,0.00397947743041937,0.00941653864582599],[0.53597120194145,0.64447803220112,0.615306925692045,0.506215767336147,0.607022592487255,0.511067053162451,0.603109040221643,0.64610008352597,0.644014314550903,0.498271927202683,0.505388009265462,0.558925039328736,0.512832366196032,0.505243465176807,0.766849224254312,0.565391181103423,0.520891469623544,0.529684997771023,0.590466061532174,0.515941711799034,0.632064344673202,0.630810916672019,0.641314252075824,0.530431722599325,0.175283084037311,0.579489137730029,0.632090713717015,0.621961293117633,0.633747278632089,0.723794278288415,0.567137863422636,0.642038043984925,0.546681062368598,0.557473806465411,0.605929467181877,0.548907648353759,0.175284588848864,0.624557440247345,0.703189853301369,0.723021324296345,0.490917003345864,0.558108720525997,0.493973937313794,0.697078592698732,0.699026377639849,0.714346540466487,0.525391885006963,0.558466824634913,0.519553579352108,0.460351746982725,0.605668492012177,0.617973379950116,0.509873355152384,0.569232673078786,0.66240750717132,0.252816319783863,0.46032202038843,0.602455644940876,0.199056967202264,0.510270187570818,0.566013646065024,0.726627983944771,0.25282925900117,0.556658625536917,0.574431485655534,0.727683082814378,0.575836477005045,0.520160415944455,0.329579341268305,0.518397335111338,0.555166040110302,0.702013182469122,0.461350524762129,0.32968053934133,0.464281704352189,0.464330981534931,0.488555454543155,0.637426680041425,0.48390473589849,0.741220509957929,0.469359699594481,0.48123352793911,0.692233584620172,0.426679662079613,0.460981403626547,0.698107630774735,0.34020554818915,0.759784034839235,0.375342727462692,0.595910727559043,0.342354639361853,0.342357471514588,0.601147930060697,0.396684496133473,0.665815569691327,0.534134081571719,0.7141868417197,0.504599866790234,0.302739132206138,0.387902479704944,0.643233640844541,0.354407265337994,0.747899398178297,0.582962100490616,0.411344123906113,0.53601968052483,0.35310319278488,0.624318904667452,0.353435008786696,0.612382499777618,0.621966655784159,0.475125058761308,0.652991130751426,0.389712147710359,0.360209152603056,0.69994670622271,0.286464820881475,0.309961451190403,0.309916616766764,0.291122964213363,0.340343280901744,0.671191166778792,0.407886271386772,0.289378561132147,0.223548664935762,0.28925867243102,0.173424925024814,0.00592470621244605],[499,1189,762,469,1907,509,980,771,1437,10819,19860,10769,15630,609,10170,25658,9976.33333333333,19299,16509,3599,708,7249,2088.33333333333,8540,649,22720,570,8279,3908,619,708.666666666667,1668,18176.6666666667,8019.66666666667,1068.66666666667,2461.66666666667,648,2571.33333333333,1214,4230,3530,506.333333333333,637.666666666667,1838,777.666666666667,708,21420,3479,619.666666666667,683,630,7552.66666666667,590,1211,817,801,1008,1224,599,704,3951,3622.66666666667,886,893,593,16925.6666666667,660,7570,660.666666666667,8419.33333333333,11950,8018,1708,785,1498,703,890,3408,1019,1006,3849,1999,779.333333333333,1518,814,1210,1108.33333333333,4800,4369,2369,841,1357,7130,549,1577,470,32589,9148,4501,999,949,3913.33333333333,1467,680,1660,480,650,1599,699,540,1477,1612.66666666667,1514,1579,1018,813,27500,1687,1019,3390,930,1488,27639,2659,3958.66666666667,28539.6666666667,30480,4848],[113.5,419.4,180.8,114.7,314,136.2,163.9,141.4,312.8,2555.1,2598.5,2194.2,2279.1,140.6,1692.7,2632,1987.73333333333,2519.93333333333,2334.9,986.9,273,1163.3,608.533333333333,2443.3,93.6,2636.6,136.8,1981.5,591,616.7,167.6,959.1,2623.83333333333,1208.56666666667,187.533333333333,853.8,94.2,549.233333333333,382.4,1543.5,1489.9,166.633333333333,163.766666666667,532.4,353.6,150.3,2372.7,2033.8,201.633333333333,101.5,204.3,2590.43333333333,170.5,240.6,362.9,86,83.5,180.6,638.8,136.4,303.9,1077.66666666667,93.7,181.333333333333,259.666666666667,1876.5,185.6,2429.5,97.8666666666667,2408.66666666667,2636.4,836.3,237,91.5,90.8,96.6,202.4,447.1,218.3,171.1,1198.6,213.6,253.266666666667,219.9,184.6,259.7,353.666666666667,1157.1,100.4,743.9,92.9666666666667,94.3333333333333,4626.5,691.1,504.5,289,3100.5,2353.2,1009.6,367.366666666667,173.3,1087.16666666667,223.4,161.8,580.6,248.4,98.5,1497.2,96.8,434.1,899,989.1,914.333333333333,889.5,185.2,246.6,101,98.5,96.3,1053.3,191.1,1339.5,99.7,96.6,99.2,100.433333333333,100.6,100.6],[2.05078125,13.37890625,3.125,2.34375,19.43359375,3.61328125,2.44140625,13.4765625,27.5390625,4.78515625,3.7109375,14.16015625,6.73828125,7.32421875,585.9375,5.6640625,8.69140625,5.859375,11.81640625,3.80859375,4.78515625,321.6796875,20.8984375,28.80859375,3.02734375,3.3203125,2.9296875,190.13671875,38.37890625,8.59375,4.23177083333333,19.3359375,3.67838541634115,6.08723958333333,17.0572916666667,19.7591145833333,3.41796875,44.7591145833333,23.046875,42.3828125,5.17578125,2.79947916666667,5.01302083333333,32.71484375,6.99869791666667,4.58984375,7.12890625,18.359375,2.21354166666667,3.3203125,8.69140625,319.010416666667,5.76171875,17.1875,7.6171875,6.34765625,4.1015625,20.5078125,4.78515625,4.6875,2.63671875,38.37890625,12.40234375,2.50651041666667,8.85416666666667,473.828125,4.8828125,24.90234375,3.28776041666667,27.9296875,4.00390624902344,132.32421875,7.71484375,3.93880208333333,13.4765625,6.93359375,2.1484375,29.98046875,2.34375,7.6171875,42.3828125,21.484375,5.76171875,7.6171875,5.6640625,22.9166666666667,6.70572916666667,40.0390625,4.78515625,68.359375,7.03125,13.9648437496745,445.21484375,3.61328125,19.04296875,2.44140625,703.22265625,30.078125,31.640625,5.43619791666667,18.1640625,38.0859375,27.5390625,2.734375,17.67578125,3.125,3.515625,17.7734375,4.296875,10.546875,25.78125,19.7265625,23.33984375,23.73046875,7.6171875,5.078125,15.13671875,16.0156249990234,7.8125,40.234375,5.078125,25.1953125,13.18359375,3.61328125,4.45963541666667,15.7552083333333,18.9453125,4.98046875]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>ARI<\/th>\n      <th>Cell Cycle Score<\/th>\n      <th>Graph connectivity<\/th>\n      <th>Isolated label F1<\/th>\n      <th>Isolated label Silhouette<\/th>\n      <th>kBET<\/th>\n      <th>NMI<\/th>\n      <th>PC Regression<\/th>\n      <th>Silhouette<\/th>\n      <th>Batch ASW<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":14,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":13,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":15,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":8,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":9,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":10,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":11,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":12,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render","options.columnDefs.6.render","options.columnDefs.7.render","options.columnDefs.8.render","options.columnDefs.9.render","options.columnDefs.10.render","options.columnDefs.11.render","options.columnDefs.12.render","options.columnDefs.13.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **Random Integration by Batch**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Embedding by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Embedding by Celltype (with jitter)**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Graph by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Combat (full/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (full/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **FastMNN embed (full/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (full/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (hvg/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (hvg/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **Harmony (full/scaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (full/unscaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (hvg/scaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (hvg/unscaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Liger (full/unscaled)**<sup><a href="/bibliography#welch2019single" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/welch-lab/liger).

<!-- -->

-   **Liger (hvg/unscaled)**<sup><a href="/bibliography#welch2019single" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/welch-lab/liger).

<!-- -->

-   **MNN (full/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (full/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **No Integration**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **No Integration by Batch**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **SCALEX (full)**<sup><a href="/bibliography#xiong2021online" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **SCALEX (hvg)**<sup><a href="/bibliography#xiong2021online" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **Scanorama (full/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (full/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (hvg/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (hvg/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (full/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (full/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **scANVI (full/unscaled)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scANVI (hvg/unscaled)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scVI (full/unscaled)**<sup><a href="/bibliography#lopez2018deep" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scVI (hvg/unscaled)**<sup><a href="/bibliography#lopez2018deep" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Integration by Batch**: Missing 'method_description'.

<!-- -->

-   **Random Embedding by Celltype**: Missing 'method_description'.

<!-- -->

-   **Random Embedding by Celltype (with jitter)**: Missing 'method_description'.

<!-- -->

-   **Random Graph by Celltype**: Missing 'method_description'.

<!-- -->

-   **Random Integration by Celltype**: Missing 'method_description'.

<!-- -->

-   **No Integration**: Missing 'method_description'.

<!-- -->

-   **No Integration by Batch**: Missing 'method_description'.

<!-- -->

-   **Random Integration**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **Immune (by batch)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Lung (Viera Braga et al.)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (by batch)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'dataset_description'.

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
  Task id: batch_integration_embed
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_embed
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_embed
  Field: dataset_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_embed
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_embed
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_embed
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_embed
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_embed
  Field: method_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_embed
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_embed
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_embed
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_embed
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_embed
  Field: metric_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_embed
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_embed
  Field: metric_description
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
