---
title: "Batch integration feature"
summary: "Removing batch effects while preserving biological variation (feature output)"
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
that can output feature matrices. Other sub-tasks for batch integration can be found
for:

-   [graphs](../batch_integration_graph/), and
-   [embeddings](../batch_integration_embed/)

This sub-task was taken from a [benchmarking study of data integration
methods](https://openproblems.bio/bibliography#luecken2022benchmarking).

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="928" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **ARI**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Cell Cycle Score**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Graph connectivity**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **HVG conservation**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">1</a></sup>: Missing 'metric_description'.

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

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-d7cb6c392ee9703c98bf" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-d7cb6c392ee9703c98bf">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Combat (hvg/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","Combat (full/unscaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","MNN (hvg/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","MNN (hvg/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","SCALEX (hvg) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","MNN (full/unscaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Combat (hvg/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Combat (full/scaled) <sup><a href=\"/bibliography#hansen2012removing\" target=\"_blank\">3<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","MNN (full/scaled) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","FastMNN feature (hvg/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","FastMNN feature (hvg/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","SCALEX (full) <sup><a href=\"/bibliography#xiong2021online\" target=\"_blank\">5<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","FastMNN feature (full/unscaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","FastMNN feature (full/scaled) <sup><a href=\"/bibliography#lun2019fastmnn\" target=\"_blank\">6<\/a><\/sup>","Scanorama gene output (hvg/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/scaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (hvg/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>","Scanorama gene output (full/unscaled) <sup><a href=\"/bibliography#hie2019efficient\" target=\"_blank\">7<\/a><\/sup>"],["Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Immune (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Overall mean","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Lung (Viera Braga et al.) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">1<\/a><\/sup>"],[0.644251638481522,0.594844615353959,0.584018069800118,0.581083163586028,0.580804805156022,0.578532613041282,0.575576579430491,0.561396806079461,0.558224344298629,0.555521287587852,0.553453040578377,0.551376592183627,0.549259535733115,0.549162088082861,0.545201373144746,0.542028134480566,0.539241844514218,0.539168193153663,0.535824913054471,0.534976457069411,0.534085299766617,0.534079484009085,0.529896000224123,0.529442445087294,0.527899365965476,0.52659793340411,0.525729031883912,0.516106675494774,0.51608704209847,0.514162958366938,0.510076337299904,0.50469604129846,0.50446674020034,0.503828476034564,0.502042000704648,0.496480051955658,0.494597848798437,0.494065835154713,0.490520340011402,0.49018924355466,0.489368203989295,0.487372569423726,0.481493000345201,0.480260712721069,0.477065069464133,0.475932837989838,0.475322788483883,0.472976728281243,0.47254607303645,0.469690461053698,0.469302564757766,0.468753646085113,0.464981006742122,0.464338987805095,0.461750176475991,0.459383727641094,0.446223379384561,0.436709992849372,0.432454044223906,0.426006412616637,0.425034291419104,0.422145370747151,0.419994808228587,0.419133353677648,0.399402292130161,0.399053245404639,0.39618675904826,0.385668430119188,0.380693912356935,0.376186778289421,0.365036086261074,0.330822271425168],[0.944229445658343,0.737595194068854,0.945418688449439,0.746521617937208,0.92803175922013,0.712999119061598,0.806635448508606,0.737102381093265,0.694679846481378,0.644560113083717,0.593884128761391,0.567280867542976,0.947570566166123,0.681248166789545,0.747358144363997,0.752650498889427,0.693988994324327,0.374236645328985,0.550207798442735,0.685961075484683,0.569981518906446,0.65948957973253,0.898815493393237,0.717007215761262,0.467849900803989,0.493443735512939,0.605526757058576,0.690902389932484,0.748510841959778,0.926415381659534,0.559643482716383,0.615530057347192,0.658898192009791,0.841080352172894,0.743340317340905,0.67724889870148,0.409461386378313,0.745103334529398,0.613990053620196,0.559553363549287,0.696345864941794,0.66795725958279,0.726819277580433,0.884299332869935,0.499513857791175,0.883922829360186,0.352798986041983,0.942259893998512,0.537028812578972,0.652560838138667,0.501348527763972,0.625711406891677,0.465647023898798,0.50962412622158,0.716231264945813,0.474661426858718,0.427407484061559,0.590388979245192,0.62736864974517,0.556244123039232,0.553968248328161,0.545412802638751,0.66823162198905,0.656720583559591,0.499391152292159,0.503778166149371,0.457923058879148,0.444037123736735,0.447480915027854,0.482045048335014,0.463596645163908,0.451438615858097],[0.865901635506016,0.747141468919332,0.901053024532649,0.76548023581928,0.709592533877097,0.826399572192476,0.847392520364584,0.632797410985744,0.771141505174925,0.85438621864556,0.79927542446562,0.859374397386097,0.679755163818876,0.790892880152329,0.694389213832823,0.740326131358654,0.740331194137372,0.761067451318899,0.758910862425853,0.606501021076747,0.907344737467613,0.770252338920565,0.620279435471904,0.656244669371291,0.772971640191484,0.907298167252321,0.796903074629596,0.677528365787809,0.425927839234685,0.649984319137671,0.514747735299583,0.569447398785462,0.455734877286212,0.649985778367205,0.379627932948503,0.57111096010994,0.750825634450428,0.735140510763871,0.55402662580843,0.549317205980075,0.735138413560902,0.538951547274032,0.442799754475636,0.346421852401202,0.77814465117307,0.34641871046444,0.841325785749039,0.070417508584384,0.652640453160028,0.64474619632753,0.650083666283346,0.644729202589922,0.582577594623985,0.422377048320059,0.255800674186012,0.36608973107152,0.386555437315116,0.247619660331007,0.255822880521949,0.815111081795288,0.81509826817813,0.48182747105061,0.0434113499578001,0.0738214293094488,0.680467588116244,0.680475141050537,0.271056674738966,0.24371275374901,0.25262926710705,0.314019279307894,0.296969496742627,0.0743628672634089],[0.994190947471566,0.990982652648334,0.993541576547953,0.992700851982172,0.984716024993095,0.974406891965675,0.994553924234945,0.971957369279238,0.948510184871135,0.947065102977506,0.961649932362852,0.936392496377435,0.994448880112125,0.991110349079426,0.980260121471228,0.955481914697042,0.955454492871355,0.936679102702434,0.981964625447952,0.963176990713195,0.946670854855,0.928755443373845,0.974383546689474,0.972169324377659,0.955856448728948,0.944956107018966,0.930748839515591,0.967982263754692,0.909943243130903,0.943161253030609,0.946880879596301,0.974948927243695,0.905422635629313,0.946533118578704,0.892375711532818,0.993098180938761,0.966928937052693,0.957521451874121,0.96826873314651,0.975281418586493,0.958292291913869,0.962154728326754,0.992570270163822,0.951446025189185,0.987794470354998,0.951689064317773,0.99374991725583,0.985166429787709,0.968614957426687,0.95681119457733,0.970357791199816,0.955994800859038,0.980742467778105,0.981487089760118,0.912758193686193,0.98323841592119,0.781830226566135,0.884361604282651,0.908370371465241,0.973921187894712,0.972889264291549,0.965199758694487,0.980251359444467,0.98408605318972,0.971582270368965,0.972073664559217,0.843164908139966,0.767410817774173,0.817902753327923,0.848649349673186,0.764654628868634,0.907223404548998],[0.0623003194888177,0.0929273707580084,-0.698615548455805,0.0596379126730561,-0.181043663471779,0.0603949079910399,-0.273695420660277,-0.116079923882017,-0.158579130986362,0.087535680304472,0.0554242287480077,0.0808753568030448,-0.784345047923323,-0.133970070907075,-0.392828826947763,-0.104979384712972,-0.104979384712972,0.205201395496353,0.03134872417983,0.27592768791627,-0.0196638122423088,-0.183317475420235,-0.403088391906283,-0.0285583020988998,0.0257594167679222,-0.0190294957183633,-0.187757691087853,-0.476138621592446,-0.172851252775135,-0.67199148029819,0.182048842372344,-0.465492178277464,-0.18046305106248,-0.67199148029819,-0.191880748493498,-0.77422790202343,-0.0832249509097497,-0.385438242974559,-0.478599071683603,-0.363791008505468,-0.385276234064069,-0.177446557013541,-0.790202342917998,-0.695953141640043,-0.221142162818955,-0.696485623003195,-0.264110756123536,-0.754131779040429,-0.180558930741191,-0.357550014259639,-0.190765492102066,-0.356918068264872,-0.460753341433779,-0.457837181044957,-0.462497786627869,-0.4636695018226,-0.207421503330162,-0.418008914144306,-0.481064632367413,-0.379343863912515,-0.378857837181045,-0.311300121506683,-0.703940362087327,-0.798336234878486,-0.355771567436209,-0.356500607533414,-0.460510328068044,-0.369623329283111,-0.385105366398092,-0.452976913730255,-0.380801944106926,-0.567092651757189],[0.923893186364932,0.856193687064716,0.952908073897662,0.850230145023413,0.690113593112518,0.80149575371007,0.927619107900222,0.847634525774276,0.84025184300071,0.764247872487196,0.779975493130624,0.785192792154027,0.955220094253613,0.836306274958067,0.864881380807807,0.661633684660939,0.724206938012658,0.851788088012738,0.716346202278083,0.667326707626637,0.733217071562198,0.802541337083434,0.6881281465287,0.652995673388936,0.704503542214432,0.731167522793116,0.786178044148204,0.81934930749019,0.820785192281565,0.84342322861283,0.736915424265475,0.883578815979387,0.817311096553562,0.844726823200782,0.848655688170858,0.940730977515112,0.861285921199579,0.746333567718015,0.858054050137674,0.794101542751482,0.766357179159375,0.611544987752848,0.948447637280496,0.792396429368297,0.725106029909262,0.743901597739901,0.884845322793616,0.93862359425336,0.601546719427654,0.702333964631304,0.847224352792382,0.718527891422772,0.700286491133521,0.839536468984322,0.876675926562311,0.869753627422339,0.856179768757628,0.861604182573129,0.865231856040324,0.733943789880275,0.730137776264686,0.409591392464368,0.925028985132659,0.916463061643235,0.632019722106903,0.629883224591814,0.870618993152008,0.842472466033166,0.80631513439137,0.83057681830688,0.830319242659661,0.732446391756822],[0.353523774636964,0.373596234810896,0.479936351237055,0.266587676252791,0.271396925495703,0.304347072781742,0.410474965427223,0.329057783061767,0.29895065971823,0.289715247132426,0.306240333853733,0.318460884377092,0.314934675124685,0.35379440294472,0.376616594908378,0.298140332450444,0.298143160339736,0.365563734943662,0.269802196575836,0.231329049110448,0.282616268298207,0.330393123387442,0.17412815713454,0.20725726138507,0.333672440931317,0.282573038180618,0.321473638271165,0.336156369803309,0.324126424374456,0.284206590325571,0.244022730870141,0.344171178350564,0.329395089161775,0.284206459949732,0.3908898233296,0.372694086695034,0.313676116517433,0.203079191763746,0.31770166460988,0.320855650426311,0.202930090265575,0.171877165649281,0.280379904625499,0.225299224729909,0.277312008596039,0.225300562828365,0.322891030662432,0.570305633101097,0.119045809549059,0.16719805133204,0.252573583946204,0.167223176790542,0.3631413108978,0.351251450932977,0.418463073449138,0.360868788638427,0.383148881052703,0.391810051946572,0.430322967324903,0.0268906525152235,0.0264406505072565,0.0974806089431623,0.454531855350682,0.461569412771628,-0.00620273253889981,-0.00632267713045158,0.360957162871862,0.391503211327261,0.370013271570732,0.438509665873482,0.381206467322548,0.345684466336946],[0.118287439141978,0.14779166811808,0.137655449864027,0.117639650731941,0.250331001523392,0.0651404286067137,0.138410290895766,0.142476063623581,0.142108888642925,0.0252492182465136,0.0719604634937109,0.0487439736176383,0.193009400988345,0.114142017078491,0.121607456861215,0.260091091730702,0.258163472267597,0.121464863882696,0.051884628431649,0.0539659127960188,0.328309265717209,0.0522738996898476,0.290095820928468,0.181682127173782,0.0494977661315531,0.325376099111397,0.0666756619757208,0.102939331940748,0.184181311601792,0.373954011410567,0.0730855058221636,0.121571680991631,0.194870472095353,0.374807927629885,0.127966631560958,0.181264781612306,0.0877915741656775,0.263685618734259,0.0887892302276516,0.0846908570960358,0.261669813677607,0.190044670550992,0.163976914438857,0.333851937711083,0.0562240922216263,0.335894291485947,0.115710550794154,0.257240091892262,0.240749467201934,0.271361816339254,0.0261993078201825,0.271249780003952,0.0635346951440513,0.0357151142683776,0.184397680279281,0.0413413727196622,0.181328183670765,0.171256806262891,0.125505808006429,0.157011753061507,0.15203804113534,0.206952684902346,0.191783896347144,0.198946699291219,0.154521303189377,0.149881891814606,0.111771637343788,0.127116050346177,0.134845794577354,0.0496040931671111,0.0714114867949979,0.1517977132663],[0.908611219634532,0.814210727342077,0.915112706101453,0.81077496723566,0.884031378484379,0.791564621742338,0.839185941468643,0.79324713702359,0.78119896321871,0.752129462271547,0.741522419072153,0.720534502761892,0.918409489097194,0.796858041885632,0.812476911118495,0.791469801066417,0.758851246530095,0.672104852204338,0.713953183320934,0.729505739047027,0.664859295013593,0.752710034743589,0.836299983114597,0.762345342530125,0.693257787218908,0.665162942923108,0.706037915015047,0.793224077741097,0.786971060982499,0.875146558985168,0.682947241419685,0.742846357151465,0.733561696648282,0.841293138741767,0.784328617376299,0.74915532057062,0.682611990184025,0.795556820598887,0.731199147018085,0.729070890230443,0.774010505433898,0.727891212475047,0.8011861014523,0.833462570200038,0.737177456846177,0.832981260037761,0.641280353162516,0.908206106461288,0.673498910058968,0.73321808331669,0.73445076518522,0.733941340473616,0.708552709382509,0.686373424586909,0.798534052990379,0.698184787665064,0.684737597968778,0.724636196420183,0.7770716501032,0.720054101745074,0.721887131029831,0.66442641289086,0.767089069657453,0.829861016082519,0.703198508297702,0.701813694898718,0.700424991527351,0.673257822954813,0.696564379672575,0.717025316850782,0.7137373801155,0.691218160933445],[0.999956070047314,0.864685427613618,0.840902387086322,0.999972505202841,0.99833740998259,0.999967560972164,0.670480851605308,0.924623998917968,0.953419030292143,0.999991699094366,0.999946964118913,0.999968595225946,1,0.688810915999322,0.871568619159846,0.859887167942458,0.859888754779988,0.856751807513698,0.999954913774811,0.997015824334277,0.811106249428653,1,0.999757577785856,0.998298551227313,0.999899791927952,0.81112175486866,1,1.00000000001214,0.894502495352187,0.700189118707678,0.998977549395726,0.940362291004581,0.916967431711269,0.700166901755423,0.801984103103795,0.948462751586207,0.724890971001945,0.670662650440317,1.00000000001214,0.849179471475248,0.670595373241004,0.999518238234225,1,0.864223714675326,0.531266468779041,0.864225395258288,0.721850973957267,0.738972536762127,0.999542419365072,0.770894191203053,0.596070131534871,0.770893654845717,1.00000000003641,1.00000000003641,0.759614982115542,0.919205091135393,0.628935024681014,0.74820999409158,0.544366510296392,0.451911664670815,0.4517304631876,0.999819587521095,0.703952920214405,0.529342158963302,0.637335494993166,0.637350928922217,0.645369914232312,0.623709630349067,0.392323822834361,0.30177326882208,0.250185758500842,0.297850685321225],[0.300567028798123,0.284419252761588,0.311808034672505,0.215378249775028,0.325290585469586,0.262703883116054,0.326270439434233,0.270510330005799,0.25051375627248,0.23558360645757,0.229058425955899,0.250564401171707,0.311784579047028,0.299603783597743,0.281878285490831,0.287262548688824,0.287256475942506,0.258657863496705,0.251961014092469,0.224848757350424,0.186214928391168,0.251902932449258,0.218105342566776,0.240687410162582,0.22123262692096,0.1862120886409,0.250655724445951,0.274685735649295,0.293510102426085,0.556018728892717,0.197350001779921,0.226279306833196,0.268195878740381,0.556018728892717,0.318494670107855,0.216221954371022,0.245301923795656,0.37759855969726,0.229210173453963,0.263316491794188,0.377620287653202,0.189070037136576,0.217577303614235,0.494581138123192,0.288121658597408,0.494579167522219,0.228656419144747,0.396441706349131,0.171922887667734,0.287093213904914,0.248591488745515,0.287091629250014,0.260369695451598,0.219397492301702,0.317020401208148,0.212102209856087,0.246569758958516,0.23480072390704,0.326090249954042,0.289514401510238,0.289585658124383,0.151754767063032,0.232713941288229,0.371818226100721,0.180481660985949,0.180485545801356,0.261109394849227,0.203492351692511,0.227753515718414,0.28795785365355,0.214470871851336,0.222219916345389],[0.615306956548152,0.633747084788049,0.644478023868036,0.566990986812916,0.528055308029528,0.564438931314227,0.644014304556147,0.642037790990862,0.61827224059865,0.510269942765498,0.549045632399242,0.497754246602042,0.511067092379605,0.621986207333272,0.639007203525356,0.460345692514289,0.460354945163731,0.527334319789785,0.567739894629031,0.449182262307788,0.464281920035009,0.509873110139659,0.531950890758081,0.463737622681117,0.582391663782767,0.464295306861555,0.506577386751029,0.490544209923204,0.461350204514358,0.17528483157216,0.474220316761219,0.598412618873355,0.449239823430285,0.175285487389288,0.426679260773037,0.585520561435186,0.481026832946809,0.325480723556534,0.513083133774501,0.630505795717169,0.325366658099091,0.479534973691978,0.51286818308393,0.252838756303637,0.588197232655619,0.252833961876533,0.389552089884663,0.14924228894424,0.413975297706035,0.337927536079533,0.526194089165978,0.337845292073868,0.450692427250347,0.519803831488543,0.302253478440957,0.591445054586229,0.539186313528122,0.367130636427148,0.377908175372723,0.340811646583153,0.340459541744253,0.432433713556634,0.356888253219893,0.386174484421228,0.296401813056411,0.296666726327057,0.296167941864274,0.295263832631266,0.426909548096738,0.320870780923905,0.409646914958682,0.331895415803411],[994,3730,1509,1218,3829,978.666666666667,1459,2987,7370,1089,1131.33333333333,1098,1079,2819,2435,764,1149,11090,853,3945,2578,1068,6485,3780.33333333333,1078,1446,1248,952,1609,1129,6760,14023,2417,1099,1480,7219,8096.66666666667,898.666666666667,1303,2809,1071.66666666667,7715,1236,1019,3268,1249,7090,1319,3567,2142,6110,1603.33333333333,709,1425,1412.33333333333,27480,1486,3209,1319.33333333333,803,967,9900,3489,1229,2345,2599,1309,3721,3098.33333333333,1249,5440,2369],[205,762.9,421,155.3,725.3,153.966666666667,442,521.5,3573,125,203.433333333333,294.5,158.4,560.366666666667,517.166666666667,205.9,93.8,1233.6,131.9,507.9,88.9,120.7,2388.3,568.9,160.5,219.5,304,165.3,334.4,145,2482.1,2620.9,455,149.8,321,1005.6,2347.7,170.7,280.9,609,114.6,2417.2,309.8,211.7,476.2,108.6,1229.8,391.2,473.5,106.333333333333,4579.7,195.6,216.8,228.9,297.033333333333,3284.1,926.8,1013.1,287.866666666667,161.2,100.2,2381.2,1253.4,352.5,155.6,121.5,165.5,1330.9,1112.03333333333,190.1,1827.4,581.9],[3.125,35.05859375,65.5273437490234,13.4765625,19.43359375,4.23177083333333,71.875,63.4765625,586.328125,4.6875,17.08984375,17.28515625,3.61328125,45.2799479166667,64.5182291660156,8.69140625,8.10546875,368.1640625,4.8828125,18.5546875,31.25,5.76171875,28.80859375,20.60546875,20.5078125,23.4375,21.2890625,5.01302083333333,8.59375,5.56640625,25,473.6328125,42.578125,5.078125,7.6171875,129.78515625,377.24609375,7.68229166666667,22.3307291666667,64.5507812490234,7.12890625,28.1575520833333,18.1640625,17.67578125,28.90625,21.97265625,321.19140625,4.78515625,23.828125,30.2083333333333,442.3828125,22.7864583333333,5.6640625,27.5390625,6.70572916666667,704.78515625,17.7734375,38.1510416666667,5.82682291666667,8.7890625,8.203125,30.6640625,31.73828125,4.58984375,27.24609375,37.40234375,6.73828125,40.13671875,19.7591145833333,5.2734375,23.828125,17.67578125]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>ARI<\/th>\n      <th>Cell Cycle Score<\/th>\n      <th>Graph connectivity<\/th>\n      <th>HVG conservation<\/th>\n      <th>Isolated label F1<\/th>\n      <th>Isolated label Silhouette<\/th>\n      <th>kBET<\/th>\n      <th>NMI<\/th>\n      <th>PC Regression<\/th>\n      <th>Silhouette<\/th>\n      <th>Batch ASW<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":15,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":14,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":16,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":8,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":9,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":10,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":11,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":12,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":13,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15,16]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7,8,9,10,11,12,13,14,15,16]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render","options.columnDefs.6.render","options.columnDefs.7.render","options.columnDefs.8.render","options.columnDefs.9.render","options.columnDefs.10.render","options.columnDefs.11.render","options.columnDefs.12.render","options.columnDefs.13.render","options.columnDefs.14.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **Random Integration by Batch**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Embedding by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Graph by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration by Celltype**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Combat (full/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (full/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/scaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **Combat (hvg/unscaled)**<sup><a href="/bibliography#hansen2012removing" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scanpy.readthedocs.io/en/stable/api/scanpy.pp.combat.html).

<!-- -->

-   **FastMNN feature (full/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (full/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (hvg/scaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **FastMNN feature (hvg/unscaled)**<sup><a href="/bibliography#lun2019fastmnn" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://doi.org/doi:10.18129/B9.bioc.batchelor).

<!-- -->

-   **MNN (full/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (full/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/scaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **MNN (hvg/unscaled)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/chriscainx/mnnpy).

<!-- -->

-   **No Integration**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **No Integration by Batch**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Random Integration**<sup><a href="/bibliography#openproblems" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **SCALEX (full)**<sup><a href="/bibliography#xiong2021online" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **SCALEX (hvg)**<sup><a href="/bibliography#xiong2021online" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/jsxlei/SCALEX).

<!-- -->

-   **Scanorama gene output (full/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (full/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/scaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

<!-- -->

-   **Scanorama gene output (hvg/unscaled)**<sup><a href="/bibliography#hie2019efficient" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/brianhie/scanorama).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Integration by Batch**: Missing 'method_description'.

<!-- -->

-   **Random Embedding by Celltype**: Missing 'method_description'.

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
  Task id: batch_integration_feature
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_feature
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_feature
  Field: dataset_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_feature
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: batch_integration_feature
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_feature
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_feature
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_feature
  Field: method_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_feature
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: batch_integration_feature
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_feature
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_feature
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_feature
  Field: metric_description
"> 1.000000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_feature
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: batch_integration_feature
  Field: metric_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_scaled
  Metric id: ari
  Best score: 4.259046750564723%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_scaled
  Metric id: ari
  Best score: 4.259046750564723%
"> Best score combat_hvg_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_scaled
  Metric id: ari
  Best score: 4.259046750564723%
"> 4.259047 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_scaled
  Metric id: ari
  Best score: 4.259046750564723%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_scaled
  Metric id: ari
  Best score: 4.259046750564723%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_unscaled
  Metric id: ari
  Best score: 4.2463505911218995%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_unscaled
  Metric id: ari
  Best score: 4.2463505911218995%
"> Best score combat_hvg_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_unscaled
  Metric id: ari
  Best score: 4.2463505911218995%
"> 4.246351 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_unscaled
  Metric id: ari
  Best score: 4.2463505911218995%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_hvg_unscaled
  Metric id: ari
  Best score: 4.2463505911218995%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_scaled
  Metric id: ari
  Best score: 4.2462040635536%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_scaled
  Metric id: ari
  Best score: 4.2462040635536%
"> Best score scanorama_feature_hvg_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_scaled
  Metric id: ari
  Best score: 4.2462040635536%
"> 4.246204 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_scaled
  Metric id: ari
  Best score: 4.2462040635536%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_scaled
  Metric id: ari
  Best score: 4.2462040635536%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_scaled
  Metric id: ari
  Best score: 4.246050993658297%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_scaled
  Metric id: ari
  Best score: 4.246050993658297%
"> Best score mnn_hvg_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_scaled
  Metric id: ari
  Best score: 4.246050993658297%
"> 4.246051 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_scaled
  Metric id: ari
  Best score: 4.246050993658297%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_scaled
  Metric id: ari
  Best score: 4.246050993658297%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_hvg performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_hvg
  Metric id: ari
  Best score: 4.170490370409384%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_hvg performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_hvg
  Metric id: ari
  Best score: 4.170490370409384%
"> Best score scalex_hvg ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_hvg performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_hvg
  Metric id: ari
  Best score: 4.170490370409384%
"> 4.170490 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_hvg performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_hvg
  Metric id: ari
  Best score: 4.170490370409384%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_hvg performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_hvg
  Metric id: ari
  Best score: 4.170490370409384%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_unscaled
  Metric id: ari
  Best score: 4.1652179188408756%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_unscaled
  Metric id: ari
  Best score: 4.1652179188408756%
"> Best score fastmnn_feature_hvg_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_unscaled
  Metric id: ari
  Best score: 4.1652179188408756%
"> 4.165218 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_unscaled
  Metric id: ari
  Best score: 4.1652179188408756%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_unscaled
  Metric id: ari
  Best score: 4.1652179188408756%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_full performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_full
  Metric id: ari
  Best score: 4.040067787785484%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_full performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_full
  Metric id: ari
  Best score: 4.040067787785484%
"> Best score scalex_full ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_full performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_full
  Metric id: ari
  Best score: 4.040067787785484%
"> 4.040068 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_full performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_full
  Metric id: ari
  Best score: 4.040067787785484%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scalex_full performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scalex_full
  Metric id: ari
  Best score: 4.040067787785484%
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_scaled
  Metric id: ari
  Best score: 3.975977072211627%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_scaled
  Metric id: ari
  Best score: 3.975977072211627%
"> Best score fastmnn_feature_full_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_scaled
  Metric id: ari
  Best score: 3.975977072211627%
"> 3.975977 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_scaled
  Metric id: ari
  Best score: 3.975977072211627%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_scaled
  Metric id: ari
  Best score: 3.975977072211627%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_unscaled
  Metric id: ari
  Best score: 3.9750039990404034%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_unscaled
  Metric id: ari
  Best score: 3.9750039990404034%
"> Best score fastmnn_feature_full_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_unscaled
  Metric id: ari
  Best score: 3.9750039990404034%
"> 3.975004 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_unscaled
  Metric id: ari
  Best score: 3.9750039990404034%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_full_unscaled
  Metric id: ari
  Best score: 3.9750039990404034%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_unscaled
  Metric id: ari
  Best score: 3.809247678706888%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_unscaled
  Metric id: ari
  Best score: 3.809247678706888%
"> Best score mnn_hvg_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_unscaled
  Metric id: ari
  Best score: 3.809247678706888%
"> 3.809248 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_unscaled
  Metric id: ari
  Best score: 3.809247678706888%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_hvg_unscaled
  Metric id: ari
  Best score: 3.809247678706888%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_scaled
  Metric id: ari
  Best score: 3.7824295721368313%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_scaled
  Metric id: ari
  Best score: 3.7824295721368313%
"> Best score fastmnn_feature_hvg_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_scaled
  Metric id: ari
  Best score: 3.7824295721368313%
"> 3.782430 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_scaled
  Metric id: ari
  Best score: 3.7824295721368313%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method fastmnn_feature_hvg_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: fastmnn_feature_hvg_scaled
  Metric id: ari
  Best score: 3.7824295721368313%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_unscaled
  Metric id: ari
  Best score: 3.356053735743325%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_unscaled
  Metric id: ari
  Best score: 3.356053735743325%
"> Best score combat_full_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_unscaled
  Metric id: ari
  Best score: 3.356053735743325%
"> 3.356054 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_unscaled
  Metric id: ari
  Best score: 3.356053735743325%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_unscaled
  Metric id: ari
  Best score: 3.356053735743325%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_scaled
  Metric id: ari
  Best score: 3.2675624709318094%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_scaled
  Metric id: ari
  Best score: 3.2675624709318094%
"> Best score combat_full_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_scaled
  Metric id: ari
  Best score: 3.2675624709318094%
"> 3.267562 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_scaled
  Metric id: ari
  Best score: 3.2675624709318094%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method combat_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: combat_full_scaled
  Metric id: ari
  Best score: 3.2675624709318094%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_scaled
  Metric id: ari
  Best score: 2.9892904222543057%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_scaled
  Metric id: ari
  Best score: 2.9892904222543057%
"> Best score scanorama_feature_full_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_scaled
  Metric id: ari
  Best score: 2.9892904222543057%
"> 2.989290 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_scaled
  Metric id: ari
  Best score: 2.9892904222543057%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_scaled
  Metric id: ari
  Best score: 2.9892904222543057%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_unscaled
  Metric id: ari
  Best score: 2.9583654410867406%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_unscaled
  Metric id: ari
  Best score: 2.9583654410867406%
"> Best score scanorama_feature_hvg_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_unscaled
  Metric id: ari
  Best score: 2.9583654410867406%
"> 2.958365 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_unscaled
  Metric id: ari
  Best score: 2.9583654410867406%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_hvg_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_hvg_unscaled
  Metric id: ari
  Best score: 2.9583654410867406%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_full_scaled
  Metric id: ari
  Best score: 2.9412850577804988%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_full_scaled
  Metric id: ari
  Best score: 2.9412850577804988%
"> Best score mnn_full_scaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_full_scaled
  Metric id: ari
  Best score: 2.9412850577804988%
"> 2.941285 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_full_scaled
  Metric id: ari
  Best score: 2.9412850577804988%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method mnn_full_scaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: mnn_full_scaled
  Metric id: ari
  Best score: 2.9412850577804988%
"> ✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_unscaled
  Metric id: ari
  Best score: 2.1980782626064426%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_unscaled
  Metric id: ari
  Best score: 2.1980782626064426%
"> Best score scanorama_feature_full_unscaled ari </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_unscaled
  Metric id: ari
  Best score: 2.1980782626064426%
"> 2.198078 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_unscaled
  Metric id: ari
  Best score: 2.1980782626064426%
"> best_score &lt;= 2 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method scanorama_feature_full_unscaled performs a lot better than baselines.
  Task id: batch_integration_feature
  Method id: scanorama_feature_full_unscaled
  Metric id: ari
  Best score: 2.1980782626064426%
"> ✗ </td>
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
