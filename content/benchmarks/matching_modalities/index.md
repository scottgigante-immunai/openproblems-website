---
title: "Multimodal Data Integration"
summary: "Alignment of cellular profiles from two different modalities"
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

Cellular function is regulated by the complex interplay of different types of biological
molecules (DNA, RNA, proteins, etc.), which determine the state of a cell. Several
recently described technologies allow for simultaneous measurement of different aspects
of cellular state. For example, [sci-CAR](https://openproblems.bio/bibliography#cao2018joint)
jointly profiles RNA expression and chromatin accessibility on the same cell and
[CITE-seq](https://openproblems.bio/bibliography#stoeckius2017simultaneous) measures
surface protein abundance and RNA expression from each cell. These technologies enable
us to better understand cellular function, however datasets are still rare and there are
tradeoffs that these measurements make for to profile multiple modalities.

Joint methods can be more expensive or lower throughput or more noisy than measuring a
single modality at a time. Therefore it is useful to develop methods that are capable
of integrating measurements of the same biological system but obtained using different
technologies on different cells.

Here the goal is to learn a latent space where cells profiled by different technologies in
different modalities are matched if they have the same state. We use jointly profiled
data as ground truth so that we can evaluate when the observations from the same cell
acquired using different modalities are similar. A perfect result has each of the paired
observations sharing the same coordinates in the latent space.

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="691" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **kNN Area Under the Curve**<sup><a href="/bibliography#stanley2020harmonic" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Mean squared error**<sup><a href="/bibliography#lance2022multimodal" target="_blank">2</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-14ae95bc7a34ed75a2d4" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-14ae95bc7a34ed75a2d4">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Procrustes superimposition <sup><a href=\"/bibliography#gower1975generalized\" target=\"_blank\">3<\/a><\/sup>","Mutual Nearest Neighbors (log CP10k) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Procrustes superimposition <sup><a href=\"/bibliography#gower1975generalized\" target=\"_blank\">3<\/a><\/sup>","Mutual Nearest Neighbors (log scran) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Procrustes superimposition <sup><a href=\"/bibliography#gower1975generalized\" target=\"_blank\">3<\/a><\/sup>","Procrustes superimposition <sup><a href=\"/bibliography#gower1975generalized\" target=\"_blank\">3<\/a><\/sup>","Mutual Nearest Neighbors (log scran) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Mutual Nearest Neighbors (log CP10k) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Harmonic Alignment (log scran) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Harmonic Alignment (log scran) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Harmonic Alignment (log scran) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Mutual Nearest Neighbors (log CP10k) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Harmonic Alignment (sqrt CP10k) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Mutual Nearest Neighbors (log scran) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Harmonic Alignment (sqrt CP10k) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Harmonic Alignment (sqrt CP10k) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Harmonic Alignment (log scran) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Harmonic Alignment (sqrt CP10k) <sup><a href=\"/bibliography#stanley2020harmonic\" target=\"_blank\">1<\/a><\/sup>","Mutual Nearest Neighbors (log scran) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>","Mutual Nearest Neighbors (log CP10k) <sup><a href=\"/bibliography#haghverdi2018batch\" target=\"_blank\">4<\/a><\/sup>"],["CITE-seq Cord Blood Mononuclear Cells <sup><a href=\"/bibliography#stoeckius2017simultaneous\" target=\"_blank\">5<\/a><\/sup>","sciCAR Cell Lines <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","Overall mean","sciCAR Cell Lines <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Cell Lines <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Mouse Kidney <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","Overall mean","Overall mean","sciCAR Mouse Kidney <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Cell Lines <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","Overall mean","sciCAR Mouse Kidney <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Mouse Kidney <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Mouse Kidney <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","sciCAR Cell Lines <sup><a href=\"/bibliography#cao2018joint\" target=\"_blank\">6<\/a><\/sup>","Overall mean","CITE-seq Cord Blood Mononuclear Cells <sup><a href=\"/bibliography#stoeckius2017simultaneous\" target=\"_blank\">5<\/a><\/sup>","CITE-seq Cord Blood Mononuclear Cells <sup><a href=\"/bibliography#stoeckius2017simultaneous\" target=\"_blank\">5<\/a><\/sup>","CITE-seq Cord Blood Mononuclear Cells <sup><a href=\"/bibliography#stoeckius2017simultaneous\" target=\"_blank\">5<\/a><\/sup>","CITE-seq Cord Blood Mononuclear Cells <sup><a href=\"/bibliography#stoeckius2017simultaneous\" target=\"_blank\">5<\/a><\/sup>"],[0.435806156927487,0.228459850100573,0.210852744118932,0.172844028640248,0.11887406646772,0.0778780089615889,0.0536274327095491,0.0432790674998052,0.0201594019565613,0.0164726147337095,0.0134589406821261,0.0111295033114947,0.0107612659222571,0.0105370096957875,0.00418917016631072,0.00411333405677155,0.00374480535610754,-0.00261043391825317,-0.0224987402073886,-0.109752150912652],[0.310815040486504,0.13574548653414,0.149901577194481,0.0653313884238423,0.0570569893734789,0.081832701723461,0.0308564587919914,0.0511666676331338,0.026937371422141,0.017552977303677,0.019380176657298,0.0628283738619363,0.00804836148609552,0.0460474540898378,-0.00771813645207627,0.000549296507813393,0.0136501812460761,0.00131766448942093,-0.0188094661377059,-0.0450738574966744],[0.560797273368471,0.321174213667007,0.271803911043383,0.280356668856654,0.180691143561962,0.0739233161997168,0.0763984066271067,0.0353914673664766,0.0133814324909816,0.015392252163742,0.00753770470695418,-0.0405693672389469,0.0134741703584187,-0.0249734346982629,0.0160964767846977,0.00767737160572971,-0.00616057053386099,-0.00653853232592727,-0.0261880142770712,-0.17443044432863],[331,750,316.666666666667,701,340,279,723.666666666667,576.666666666667,859,1013,975.333333333333,490,429,750,701,593.333333333333,1054,650,720,490],[65.2,91.8,146.2,94.5,230.3,143.1,97.8666666666667,92.6666666666667,120.2,151.3,137.166666666667,99.6,193.3,99.4,225.3,205.733333333333,140,198.6,99.7,86.6],[0.47626953125,1.953125,0.6978515625,3.22265625,0.67626953125,0.941015625,3.80859375,2.01822916666667,4.1015625,3.22265625,3.80859375,2.1484375,1.26953125,4.1015625,0.99990234375,0.96689453125,4.1015625,0.63125,4.1015625,1.953125]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>kNN Area Under the Curve<\/th>\n      <th>Mean squared error<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **Harmonic Alignment (log scran)**<sup><a href="/bibliography#stanley2020harmonic" target="_blank">1</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/harmonic-alignment).

<!-- -->

-   **Harmonic Alignment (sqrt CP10k)**<sup><a href="/bibliography#stanley2020harmonic" target="_blank">1</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/harmonic-alignment).

<!-- -->

-   **Mutual Nearest Neighbors (log CP10k)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/LTLA/batchelor).

<!-- -->

-   **Mutual Nearest Neighbors (log scran)**<sup><a href="/bibliography#haghverdi2018batch" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/LTLA/batchelor).

<!-- -->

-   **Procrustes superimposition**<sup><a href="/bibliography#gower1975generalized" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://docs.scipy.org/doc/scipy/reference/generated/scipy.spatial.procrustes.html).

<!-- -->

-   **Random Features**<sup><a href="/bibliography#openproblems" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **True Features**<sup><a href="/bibliography#openproblems" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Features**: Missing 'method_description'.

<!-- -->

-   **True Features**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **CITE-seq Cord Blood Mononuclear Cells**<sup><a href="/bibliography#stoeckius2017simultaneous" target="_blank">5</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **sciCAR Cell Lines**<sup><a href="/bibliography#cao2018joint" target="_blank">6</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **sciCAR Mouse Kidney**<sup><a href="/bibliography#cao2018joint" target="_blank">6</a></sup>: Missing 'dataset_description'.

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
  Task id: matching_modalities
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: matching_modalities
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: matching_modalities
  Field: dataset_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: matching_modalities
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: matching_modalities
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: matching_modalities
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: matching_modalities
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: matching_modalities
  Field: method_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: matching_modalities
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: matching_modalities
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: matching_modalities
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: matching_modalities
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: matching_modalities
  Field: metric_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: matching_modalities
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: matching_modalities
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
