---
title: "Batch integration graph"
summary: "Removing batch effects while preserving biological variation (graph output)"
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
methods integrate datasets across batches that arise from various biological and
technical sources. Methods that integrate batches typically have three different types
of output: a corrected feature matrix, a joint embedding across batches, and/or an
integrated cell-cell similarity graph (e.g., a kNN graph). This sub-task focuses on all
methods that can output integrated graphs, and includes methods that canonically output
the other two data formats with subsequent postprocessing to generate a graph. Other
sub-tasks for batch integration can be found for:

-   [embeddings](../batch_integration_embed/), and
-   [corrected features](../batch_integration_feature/)

This sub-task was taken from a [benchmarking study of data integration
methods](https://openproblems.bio/bibliography#luecken2022benchmarking).

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="745" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **ARI**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Graph connectivity**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Isolated label F1**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **NMI**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-93b5da203becf6e8e654" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-93b5da203becf6e8e654">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","BBKNN (hvg/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","BBKNN (hvg/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","BBKNN (full/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","BBKNN (full/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","scANVI (hvg/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","BBKNN (hvg/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","scANVI (full/unscaled) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">3<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","BBKNN (hvg/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","BBKNN (hvg/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","BBKNN (full/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","BBKNN (hvg/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","scVI (full/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","scVI (hvg/unscaled) <sup><a href=\"/bibliography#lopez2018deep\" target=\"_blank\">6<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","BBKNN (full/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","BBKNN (full/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","BBKNN (hvg/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","BBKNN (full/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","BBKNN (full/unscaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","BBKNN (hvg/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Harmony (full/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Scanorama (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Scanorama (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","FastMNN embed (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","Harmony (hvg/unscaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","FastMNN embed (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">2<\/a><\/sup>","BBKNN (full/scaled) <sup><a href=\"/bibliography#polanski2020bbknn\" target=\"_blank\">8<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">10<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">9<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">5<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">4<\/a><\/sup>","Harmony (hvg/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Harmony (full/scaled) <sup><a href=\"/bibliography#korsunsky2019fast\" target=\"_blank\">7<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (full/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>","Liger (hvg/unscaled) <sup><a href=\"/bibliography#welch2019single\" target=\"_blank\">11<\/a><\/sup>"],["Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>"],[0.958724309710583,0.955883362783007,0.955585664838564,0.953661264704337,0.95228455270925,0.951307417181265,0.951160077900022,0.948488013713018,0.948029403852519,0.944845488861956,0.943121626666146,0.943048824739164,0.93634985667793,0.929844013198328,0.922271887027446,0.916060008568093,0.902366764136145,0.900575371735384,0.897742944515614,0.896121475264988,0.895114292343077,0.892132294897176,0.891467476026479,0.890990198831547,0.888246959701411,0.887880741658339,0.885546251161666,0.866896519957631,0.86684547128024,0.866616824386966,0.864695742255672,0.862933225531571,0.861718729814646,0.861386910866471,0.859596333561197,0.859338874009922,0.859084634728252,0.857910308768152,0.847747669575734,0.846392869416391,0.845971312060815,0.845717983406786,0.844874008993167,0.844059229846603,0.842921354640298,0.842539446288796,0.842104908075584,0.841652189922151,0.841327222956201,0.840364757636901,0.839732287109716,0.839575746145719,0.837441875785824,0.836922411838227,0.835576736579518,0.824773708782178,0.824437316690631,0.82421025455594,0.824122386407004,0.822364804101701,0.8221564234689,0.821278718163328,0.820393558722944,0.81806016809724,0.814669272401874,0.812693680622642,0.811099670032291,0.810628901128447,0.80703940636734,0.806825465542245,0.805736593816475,0.804842170416795,0.804575057544665,0.803406420003211,0.800641564443371,0.798352983170622,0.796760867143816,0.796519893130578,0.793266492959855,0.793067555744816,0.792075845744514,0.791732110394964,0.789846373441651,0.789612746951229,0.789460495247764,0.788066816982323,0.786788094540042,0.785508545352975,0.781806680206164,0.777762410118243,0.776655678209403,0.776243358470319,0.775685747944154,0.774742541072163,0.773297542090606,0.772377423509352,0.771872876104914,0.767861280767801,0.764754557971423,0.763869932092415,0.762001779932269,0.761373494654138,0.760466888050142,0.75741920610599,0.756101097564654,0.755354551093822,0.751032489078469,0.750205808033165,0.750200128727487,0.749643644690836,0.74892563865845,0.748340701271297,0.748111562891429,0.746536555234509,0.745979622268521,0.745371802246349,0.738275711574611,0.736508709533217,0.734181409419211,0.733754672959471,0.732363776721374,0.729476445489815,0.727023238931363,0.726616954071323,0.724115250355846,0.723962882949866,0.722032823204688,0.72056432647364,0.718376538919359,0.717889658525946,0.714252918504641,0.710297294552886,0.709090333949756,0.708273612918253,0.706714708976567,0.698655358185824,0.698247573295778,0.698101537686214,0.696170025167383,0.69579549769295,0.692413577098134,0.688610155403566,0.678720176174967,0.677859973965767,0.676803347987141,0.655644471461026,0.624517861633603,0.618418997098314,0.616456429465804,0.604336016263993,0.587370095644183,0.572984651167856,0.566208624845996,0.550682335347378,0.512814956746149,0.501290280311348,0.472393917420811,0.442991536017363,0.209265330642426,0.182333972311597],[0.957803915091845,0.953616763448341,0.952380640453455,0.947576788170815,0.948535896361187,0.948538639472467,0.944842132265964,0.949581526855748,0.944767077609579,0.943334873569761,0.944450438898717,0.944236064166792,0.91977181688284,0.91676544726369,0.951268605892867,0.941489586827388,0.870037562189817,0.914552095364604,0.926690717509062,0.904827683108107,0.841801960838419,0.884791718941524,0.806456553325415,0.906337165722781,0.830953365006376,0.844027285986736,0.833482551391606,0.840932284760874,0.840918353501503,0.879103682114089,0.918540665344354,0.882915570502208,0.775722373433614,0.780672846902112,0.884245145450476,0.758621466124438,0.771704204179585,0.815382327431417,0.762436493087885,0.653224704139507,0.762072385085245,0.704439536373654,0.89386421751327,0.793437445821511,0.766000218567756,0.891090049409748,0.752111923890542,0.744617352637941,0.706464353047806,0.757562878505122,0.780161877822067,0.783041412291289,0.758551250717309,0.767412842343852,0.748483093908903,0.66908606023515,0.700001706315798,0.744134010452082,0.711745916536986,0.654080606456651,0.716823081717995,0.695270342805122,0.691085539784308,0.669042077440802,0.749159293465578,0.684786200747729,0.736025429310728,0.678155084913156,0.743437955072919,0.660395764264007,0.737314657726463,0.742860325717646,0.730427256156295,0.708307691021067,0.68621265549984,0.65525942198801,0.591906862918706,0.697882309766985,0.659448812972764,0.588962596869751,0.742980128563652,0.730658762914842,0.749143669775777,0.703708897413964,0.74478405648183,0.676010356055007,0.609426081835696,0.556070915576008,0.763396581351555,0.577054686419169,0.644517558930838,0.53227190411743,0.598758217402733,0.692858428260309,0.73442012185115,0.59487157509128,0.683447326341644,0.605699908475093,0.553477232022001,0.604528899275403,0.687098722680409,0.616524425029286,0.621868018642736,0.60557935848555,0.62148815498014,0.621294984089312,0.630633921482281,0.633223262505751,0.578710496207728,0.695040732714378,0.511623444092569,0.701362601946383,0.544087705566486,0.569172421336956,0.455003889622638,0.577958562325162,0.500667972681192,0.655773576848793,0.511999899000684,0.494070071454027,0.527498175426808,0.460638544793273,0.490923956341363,0.491897143686405,0.483595185020129,0.565774118164158,0.695174636499646,0.479722191738285,0.465604979145559,0.528021676487133,0.466231018209343,0.494265446405758,0.529512149533235,0.507483488812798,0.494137057311903,0.487411837126309,0.432651809050204,0.520645720469814,0.485374360411702,0.550216416977562,0.445046767957594,0.386610790994096,0.51488161366262,0.516816902923574,0.506741643583066,0.503069170575171,0.605839831509632,0.506528862640506,0.581018241219392,0.325106005019303,0.417009266291116,0.480392609292245,0.44812626950551,0.399418057303623,0.375737126229482,0.365025060090887,0.386000256651679,0.307667539038763,0.0514486943848971,0.0870890072259081],[0.993786241692711,0.994701851037041,0.991980294806983,0.993988282859589,0.992013724460622,0.99506580624731,0.993049712772568,0.996579825459522,0.995828278674856,0.982086585151273,0.988280399676669,0.993708948579724,0.991115018791678,0.996941295403966,0.990390938824227,0.993271335367633,0.986546268807926,0.989464387360835,0.942629858821106,0.994954756117938,0.98549973089086,0.978400309491696,0.994079063417376,0.982057084994886,0.996559611399106,0.987144929175452,0.9837928907474,0.940404203612151,0.940843431976507,0.983953910695349,0.987574905675527,0.94726680792584,0.985396560537023,0.986796016344854,0.94664381391733,0.965383724165567,0.986536645895042,0.98368011263962,0.987270569322329,0.990460209032291,0.971802115306596,0.982415070583696,0.954261553333213,0.97866051376821,0.937914401165645,0.949811738654434,0.97689723177387,0.987307049643874,0.975889813100512,0.980058637786287,0.899926100494263,0.898659247353494,0.969161672076499,0.945503433389887,0.91712813601736,0.989304127861101,0.978798109812609,0.979341110466939,0.910371883000783,0.973171223359637,0.960174769348804,0.982653682623637,0.968083123311395,0.986904158356908,0.934225958735063,0.974442333117228,0.954996827504384,0.99076564183403,0.955590283148307,0.990493817690474,0.956687123129837,0.961790728328184,0.95673082982106,0.900054205522056,0.952795755436762,0.90114920219822,0.992079658675822,0.939653204074396,0.929408661112005,0.981700889168002,0.946388497283534,0.935112841965563,0.95544374397137,0.975394554997993,0.955626282208469,0.954486630506664,0.989462500507504,0.95866744429983,0.975946436344359,0.98012811093542,0.947550445512294,0.988599892524954,0.978185040091861,0.951863191502661,0.907491361108929,0.927182061834136,0.95462430446284,0.985426371297051,0.910162740218371,0.955464393688927,0.950744799845211,0.973396190778602,0.974213421805989,0.973722775278203,0.955433197888345,0.95533012961796,0.952283816138126,0.953459707304149,0.949673083687256,0.93869703550626,0.92401686783185,0.970099705839558,0.98792680442853,0.973682298851687,0.949247370865983,0.981245333033812,0.987835301840738,0.935338480984971,0.989929258801073,0.971899610416208,0.888928086696855,0.914298574486609,0.972079142686135,0.98556408520618,0.848974858329019,0.975324085279698,0.866477254141832,0.817167224962162,0.982067605259665,0.908531050064982,0.980852425962591,0.946526433566865,0.814328150208875,0.857672065865106,0.946625575992542,0.972407209746655,0.868721758068375,0.93032158555295,0.972820141369686,0.970211120215266,0.768790709518079,0.988322425189223,0.934038425893098,0.977522736128748,0.935140099343734,0.955141434848212,0.972777245337261,0.873575875731764,0.967259818154219,0.930489710750216,0.972935855168246,0.959540038796426,0.89892117955833,0.914731191098584,0.687350618978253,0.705234803461321,0.630947499254822,0.677805883577544,0.454606971539546,0.339014624644381],[0.951337926121588,0.950833264300144,0.952341388092852,0.954591945373893,0.949434991059844,0.940861875581193,0.952130691949471,0.932771779827304,0.938629151417904,0.942639527210126,0.922965653659399,0.925551079729459,0.95546253439222,0.941167795949687,0.83237250008059,0.822922980625822,0.884630482037037,0.827290207754178,0.846355888122564,0.838151383463517,0.884084768906585,0.853483145077927,0.92616555983033,0.802454851336708,0.95185245203607,0.866266923821398,0.915356620070492,0.844997175606304,0.844633384001797,0.763573398187392,0.688998817458683,0.78921471880491,0.867443683711154,0.861407026177056,0.774084812603039,0.893737357535309,0.849575036733039,0.830429065894852,0.840675536629446,0.917221997634465,0.846434792239416,0.894365497695608,0.690397877106908,0.810919507688979,0.84351651893822,0.68860772462585,0.832546252044721,0.840367113538235,0.888742607369233,0.80855079980006,0.854038214634024,0.854048104727217,0.81366860322419,0.828052500213478,0.846276380661354,0.853569743889264,0.832030308404283,0.813967512707514,0.882553446090623,0.915410317685111,0.83368328282816,0.807311439082024,0.829080337421887,0.827631208869742,0.783943441102848,0.801910823326507,0.770041551687597,0.84924241617742,0.74422951134036,0.831965272982443,0.74171068349984,0.732243000102538,0.745301095959819,0.836899778113813,0.809660497564457,0.847384909932873,0.875686597100233,0.802633888096823,0.831429246962826,0.852782392026578,0.715190400168852,0.74568915605201,0.662717097899376,0.732718835758915,0.660863190506224,0.7529328480947,0.785797377221136,0.900818184299596,0.569301960410612,0.821020232809011,0.762391822495933,0.884935440148381,0.865748197349289,0.693095898457016,0.702506754875703,0.849335956190877,0.733937610745824,0.779380122812243,0.857824858195193,0.761985207203642,0.65531668216182,0.731015963736697,0.71741777699384,0.730406713371435,0.713739306356537,0.713606205633419,0.699802942504657,0.693667647203183,0.812805665324534,0.613757220106415,0.854320907541615,0.542188473337054,0.772808995335431,0.722186126888865,0.870398174177244,0.707627377509877,0.724697758374612,0.650459227784179,0.827179329770331,0.770701986558021,0.783748972751337,0.867753674193367,0.748454953305255,0.705303296294767,0.868121032947931,0.627086915211293,0.583911544931394,0.865583923154702,0.717789567754129,0.713847444392859,0.701219819928941,0.7344322429914,0.770884627436936,0.733453001228449,0.719616759356228,0.632386440908473,0.829963662790698,0.67196860123454,0.632301561305819,0.613873387862759,0.851602096640016,0.832586474687264,0.642150111197384,0.676030347453062,0.640099116330102,0.560187914987166,0.152739900503476,0.434050960124274,0.175581395348837,0.726063052643483,0.331906533307056,0.221781856559101,0.293127652930529,0.333514308406344,0.611583900264735,0.57530061703453,0.43369301149656,0.38290846621824,0.139373821495914,0.10558358929355],[0.931969155936188,0.924381572346501,0.925640336000966,0.918488042413052,0.919153598955348,0.920763347424091,0.914617774612087,0.915018922709499,0.912893107707738,0.911320969516664,0.9167900144298,0.90869920648068,0.879050056644982,0.86450151417597,0.915055503312101,0.906556131451529,0.8682527435098,0.870994796461918,0.875295313609725,0.846552078370391,0.869070708736446,0.851854006077556,0.839168727532797,0.873111693271812,0.773622410364091,0.85408382764977,0.809552942437167,0.841252415851194,0.840986715641152,0.839836306551035,0.863668580544123,0.832335804893325,0.818312301576795,0.816671754041862,0.833411562273941,0.819612948214375,0.828522652105341,0.802149729106718,0.800608079263276,0.824664566859302,0.803575955612005,0.801651828974184,0.840972388019276,0.793219452107714,0.824254279889573,0.840648272465152,0.806864224593203,0.794317243868554,0.794212118307252,0.815286714456135,0.824802955488511,0.822554220210878,0.8083859771253,0.806720871405693,0.830419335730453,0.787134903143197,0.786919142229833,0.759398384597224,0.791818299999625,0.746797068905402,0.777944559980641,0.79987940814253,0.793325234374188,0.788663227721511,0.791348396304007,0.789635365299103,0.783334871626457,0.724352461589181,0.784899875907775,0.744447007232058,0.78723391090976,0.782474627518812,0.785841048241485,0.768364005355907,0.753897349272425,0.789618398563386,0.727370349880503,0.745910170584109,0.752779250791823,0.748824344914934,0.763744356962018,0.755467680647442,0.792080982120081,0.746628699634044,0.796568451794531,0.768837433272922,0.76246641859583,0.726477637236468,0.818581742718128,0.73284661030937,0.752162885898546,0.699166197090512,0.660051536932734,0.761152646068665,0.748771930526641,0.718120100921115,0.715482262869346,0.700938720486816,0.737553401450125,0.733501228201688,0.754846915041635,0.724557399071965,0.728368334758004,0.719967977288773,0.733743731033593,0.731186885034596,0.721409276188814,0.72047261511958,0.659611269690431,0.751079590436289,0.705741335167766,0.779712023962193,0.687622746235271,0.721105373860528,0.70926905440822,0.714655936116545,0.739901813401903,0.704463552514923,0.607617150104758,0.698347023409628,0.729279872010494,0.675214988486011,0.696634903392698,0.723703291097942,0.695769925126304,0.727666413144314,0.742567857245879,0.719783966039411,0.708044003518084,0.721158463158809,0.708708409917688,0.665965055247522,0.721636408619978,0.734485895766659,0.666479443245593,0.702415944961861,0.661653063273833,0.669470243487552,0.694184037582324,0.648881065716213,0.704214734276844,0.54692093074368,0.623810553946766,0.541069909357684,0.625232532691663,0.604179365433557,0.766714469184042,0.65952028989671,0.741966263140768,0.435685296642972,0.627628727810315,0.630224100023654,0.624659397389614,0.55506578458096,0.376588181512124,0.359600640658655,0.438934902280184,0.403584255234904,0.191631835149346,0.19764866808255],[713,22250,948,764,850,20428,1678,3990,21919,1398,1119,703,2158,683,621,2189,19823.3333333333,1249,610,635,4059,18061,1778,2128,808,22306,663,621,894,25350,21090,817,17416.3333333333,11043,1199,1107.66666666667,19159,24909,627.666666666667,849,3050,21140,1167,7980,906,1375,10679,3669,2838.66666666667,2899,867,935,1055,1177,886.333333333333,1267,3618,549,1184.66666666667,1811,8180,11372.6666666667,771.333333333333,2534,1238,713.666666666667,1172.33333333333,625.333333333333,658.333333333333,606.333333333333,774,1588,882.333333333333,1068,1000.66666666667,1077.33333333333,713,4810,772,22350,1119,2047,923,1395,857,873,2796,1198,2041.33333333333,4230,703,644,776.333333333333,817,672,3470.33333333333,1008,549,1538.33333333333,20350,712,653,778,896,998,1337.66666666667,1510.66666666667,1641.33333333333,712,1924.33333333333,1659,20830,540,896,2689,1077,2206,666.333333333333,644,1599,3252,745,1577,19380,1088,3969,3018,1689,735,1740,778,1158,1448,1079,857,1320,3790,1279,1656,8316.66666666667,5220,809,2180,8480,1558,1332,2347,20629,21050,1340,8290,1261,1598,664,2800,27779,3075.33333333333,21302.6666666667,15500,3408],[365.8,2140.9,178.6,183,212.1,2613,267.6,333,2545,173.9,198.7,164.5,379.9,110.8,106.7,226.5,2266.3,303.7,93.7,142.6,940.9,2314.9,312.9,176.5,167.4,2592.73333333333,234.7,96.7,155.7,2610.4,2410.1,86.2,2557.93333333333,945.833333333333,94.9,206.8,2343.1,2321.1,101.533333333333,173,463.5,2554.8,112.6,2607.4,157.9,204,1142.6,1079.1,732.7,363.633333333333,225.1,273.7,195.933333333333,241.8,280.766666666667,827.1,700,112.3,225.066666666667,441.1,2403.5,2162.66666666667,168.2,604.166666666667,176.2,195.5,226,128.433333333333,94.2,128.766666666667,96.3666666666667,1238.2,131.7,223.5,223.7,295.266666666667,85.6,1196.3,186.6,2521.4,292.5,235.8,100.3,217.1,132.7,130.1,829.5,200,681.3,183.4,147.3,106,169.566666666667,110.9,323.5,973.3,225,122.7,785.833333333333,2406.4,99.9,89,92.1,106.7,93.5,98.9333333333333,195.466666666667,124.266666666667,176.6,205,978.8,2389.36666666667,137.7,121.5,739.1,199.5,799.6,238,151.8,185.1,1297.53333333333,142.4,141.5,4404.5,277.8,359.8,101.9,551.6,274.7,1413.7,135,99,439.1,251.4,97.2,97.1,1282.5,186.8,102.9,2157.93333333333,1649.4,164.7,118.7,968.1,197.3,316.633333333333,579.2,101,2351.6,443.5,3102.2,289.3,202.7,155.8,99.4,100.5,100.8,100.766666666667,100.8,101.1],[3.61328125,6.73828125,4.8828125,3.41796875,13.4765625,4.78515625,3.3203125,2.24609375,3.7109375,5.078125,2.05078125,3.125,32.71484375,2.34375,1.953125,19.3359375,10.64453125,2.44140625,3.02734375,2.83203125,88.76953125,14.0625,3.90625,2.34375,7.32421875,5.859375,7.32421875,3.515625,5.2734375,5.76171875,28.80859375,6.34765625,3.67838541666667,5.63151041666667,9.765625,6.93359375,11.1328125,12.01171875,2.11588541666667,4.58984375,25.5859375,7.03125,21.97265625,3.41796875,5.56640625,17.67578125,363.28125,42.3828125,38.4114583333333,14.6484375,7.6171875,7.51953125,17.0572916666667,8.69140625,5.43619791666667,19.140625,16.0156249990234,2.05078125,7.09635416666667,31.5429687490234,587.109375,298.4375,4.91536458333333,19.9218749996745,17.1875,4.23177083333333,2.18098958333333,2.79947916666667,3.28776041666667,3.02734375,3.97135416666667,18.45703125,7.12890625,8.59375,2.50651041666667,5.72916666666667,2.34375,42.3828125,5.76171875,3.90625,2.1484375,2.9296875,4.1015625,21.2890625,7.91015625,7.51953125,25.87890625,7.2265625,19.7591145833333,2.63671875,4.6875,3.41796875,8.85416666666667,8.69140625,8.69140625,37.9882812496745,2.34375,2.9296875,19.82421875,24.8046875,3.3203125,3.515625,4.296875,8.203125,6.99869791666667,13.0859374996745,22.7864583333333,29.19921875,8.69140625,2.79947916666667,17.7734375,27.9296875,2.83203125,8.30078125,40.13671875,20.5078125,39.84375,8.85416666666667,3.125,27.24609375,22.8515625,2.734375,35.64453125,443.26171875,7.6171875,15.0390625,4.8828125,22.55859375,4.8828125,23.828125,5.56640625,13.4765625,5.078125,5.078125,6.93359375,7.71484375,40.0390625,2.34375,16.0156249990234,590.8203125,18.84765625,10.546875,29.98046875,488.0859375,23.4375,22.3307291666667,21.484375,15.13671875,30.17578125,18.1640625,697.265625,27.5390625,3.125,10.546875,3.61328125,13.28125,4.45963541666667,15.8203125,19.04296875,4.8828125]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>ARI<\/th>\n      <th>Graph connectivity<\/th>\n      <th>Isolated label F1<\/th>\n      <th>NMI<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":8,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":9,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7,8,9]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7,8,9]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render","options.columnDefs.6.render","options.columnDefs.7.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **Random Integration by Batch**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **BBKNN (full/scaled)**<sup><a href="/bibliography#polanski2020bbknn" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/Teichlab/bbknn).

<!-- -->

-   **BBKNN (full/unscaled)**<sup><a href="/bibliography#polanski2020bbknn" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/Teichlab/bbknn).

<!-- -->

-   **BBKNN (hvg/scaled)**<sup><a href="/bibliography#polanski2020bbknn" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/Teichlab/bbknn).

<!-- -->

-   **BBKNN (hvg/unscaled)**<sup><a href="/bibliography#polanski2020bbknn" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/Teichlab/bbknn).

<!-- -->

-   **Random Graph by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Combat (full/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (full/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **FastMNN embed (full/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (full/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (hvg/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN embed (hvg/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (full/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (full/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (hvg/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (hvg/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">10</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **Harmony (full/scaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (full/unscaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (hvg/scaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Harmony (hvg/unscaled)**<sup><a href="/bibliography#korsunsky2019fast" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/lilab-bcb/harmony-pytorch).

<!-- -->

-   **Liger (full/unscaled)**<sup><a href="/bibliography#welch2019single" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/welch-lab/liger).

<!-- -->

-   **Liger (hvg/unscaled)**<sup><a href="/bibliography#welch2019single" target="_blank">11</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/welch-lab/liger).

<!-- -->

-   **MNN (full/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (full/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **No Integration**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration**<sup><a href="/bibliography#openproblems" target="_blank">12</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **SCALEX (full)**<sup><a href="/bibliography#xiong2021online" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **SCALEX (hvg)**<sup><a href="/bibliography#xiong2021online" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **Scanorama (full/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (full/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (hvg/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama (hvg/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (full/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (full/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **scANVI (full/unscaled)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scANVI (hvg/unscaled)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scVI (full/unscaled)**<sup><a href="/bibliography#lopez2018deep" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scVI (hvg/unscaled)**<sup><a href="/bibliography#lopez2018deep" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Integration by Batch**: Missing 'method_description'.

<!-- -->

-   **Random Graph by Celltype**: Missing 'method_description'.

<!-- -->

-   **Random Integration by Celltype**: Missing 'method_description'.

<!-- -->

-   **No Integration**: Missing 'method_description'.

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
  Task id: batch_integration_graph
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_graph
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_graph
  Field: dataset_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_graph
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_graph
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_graph
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_graph
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_graph
  Field: method_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_graph
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_graph
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_graph
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_graph
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_graph
  Field: metric_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_graph
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_graph
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
