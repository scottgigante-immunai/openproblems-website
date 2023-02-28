---
title: "Denoising"
summary: "Removing noise in sparse single-cell RNA-sequencing count data"
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

Single-cell RNA-Seq protocols only detect a fraction of the mRNA molecules present
in each cell. As a result, the measurements (UMI counts) observed for each gene and each
cell are associated with generally high levels of technical noise ([Grün et al.,
2014](https://openproblems.bio/bibliography#grn2014validation)). Denoising describes the
task of estimating the true expression level of each gene in each cell. In the
single-cell literature, this task is also referred to as *imputation*, a term which is
typically used for missing data problems in statistics. Similar to the use of the terms
"dropout", "missing data", and "technical zeros", this terminology can create confusion
about the underlying measurement process ([Sarkar and Stephens,
2021](https://openproblems.bio/bibliography#sarkar2021separating)).

A key challenge in evaluating denoising methods is the general lack of a ground truth. A
recent benchmark study ([Hou et al.,
2020](https://openproblems.bio/bibliography#hou2020systematic))
relied on flow-sorted datasets, mixture control experiments ([Tian et al.,
2019](https://openproblems.bio/bibliography#tian2019benchmarking)), and comparisons with
bulk RNA-Seq data. Since each of these approaches suffers from specific limitations, it
is difficult to combine these different approaches into a single quantitative measure of
denoising accuracy. Here, we instead rely on an approach termed molecular
cross-validation (MCV), which was specifically developed to quantify denoising accuracy
in the absence of a ground truth ([Batson et al.,
2019](https://openproblems.bio/bibliography#batson2019molecular)). In MCV, the observed
molecules in a given scRNA-Seq dataset are first partitioned between a *training* and a
*test* dataset. Next, a denoising method is applied to the training dataset. Finally,
denoising accuracy is measured by comparing the result to the test dataset. The authors
show that both in theory and in practice, the measured denoising accuracy is
representative of the accuracy that would be obtained on a ground truth dataset.

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="691" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **Mean-squared error**<sup><a href="/bibliography#batson2019molecular" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Poisson loss**<sup><a href="/bibliography#batson2019molecular" target="_blank">1</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-e97c5a5f31ca4f193f64" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-e97c5a5f31ca4f193f64">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["MAGIC (approximate, reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate, reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate, reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate, reversed normalization) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","ALRA (sqrt norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","MAGIC (approximate) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC (approximate) <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","MAGIC <sup><a href=\"/bibliography#van2018recovering\" target=\"_blank\">2<\/a><\/sup>","DCA <sup><a href=\"/bibliography#eraslan2019single\" target=\"_blank\">4<\/a><\/sup>","DCA <sup><a href=\"/bibliography#eraslan2019single\" target=\"_blank\">4<\/a><\/sup>","KNN smoothing <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">5<\/a><\/sup>","DCA <sup><a href=\"/bibliography#eraslan2019single\" target=\"_blank\">4<\/a><\/sup>","KNN smoothing <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">5<\/a><\/sup>","KNN smoothing <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">5<\/a><\/sup>","DCA <sup><a href=\"/bibliography#eraslan2019single\" target=\"_blank\">4<\/a><\/sup>","KNN smoothing <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">5<\/a><\/sup>","ALRA (log norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (log norm, reversed normalization) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","ALRA (sqrt norm) <sup><a href=\"/bibliography#linderman2018zero\" target=\"_blank\">3<\/a><\/sup>","Iterative KNN smoothing <sup><a href=\"/bibliography#wagner2018knearest\" target=\"_blank\">6<\/a><\/sup>","Iterative KNN smoothing <sup><a href=\"/bibliography#wagner2018knearest\" target=\"_blank\">6<\/a><\/sup>","Iterative KNN smoothing <sup><a href=\"/bibliography#wagner2018knearest\" target=\"_blank\">6<\/a><\/sup>","Iterative KNN smoothing <sup><a href=\"/bibliography#wagner2018knearest\" target=\"_blank\">6<\/a><\/sup>"],["Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Overall mean","Overall mean","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Overall mean","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Overall mean","Overall mean","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Overall mean","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Overall mean","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Overall mean","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Overall mean","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Overall mean","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","1k Peripheral blood mononuclear cells <sup><a href=\"/bibliography#10x2018pbmc\" target=\"_blank\">8<\/a><\/sup>","Tabula Muris Senis Lung <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">7<\/a><\/sup>","Overall mean","Pancreas (inDrop) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">9<\/a><\/sup>"],[0.641371028613244,0.640626872326657,0.640500866121077,0.640376568633655,0.63017390069839,0.629889429644463,0.608790854178657,0.60852380115527,0.502554866692387,0.485205335445055,0.481728497145767,0.471332642497011,0.423601074068488,0.422281504367678,0.416121262867025,0.414690122172609,0.413581152364531,0.411680476800312,0.401021120158079,0.398069803860648,0.0769955027381772,0.069626529009327,0.0661743742939006,0.0556887669317607,0.0493359006179299,0.0388207100558474,0.0204442690477779,0.000951855255711676,-0.121852738629811,-0.129527947133572,-0.172834932236048,-0.267124110944763,-0.472953756580378,-0.596838019938494,-0.652093874332176,-0.665466428902928,-0.884760098334465,-0.95714637506796,-0.992922159768484,-1.13686000590303,-4.60364459095676,-4.73169540563172,-4.81302798622217,-5.10374396207803],[0.298002158306132,0.303818096684305,0.296264382830745,0.303318344456898,0.280609339709975,0.280042057036702,0.240543443822464,0.240007764139487,0.0286832388668031,-0.00818143686287472,-0.0123908578077923,-0.040836691647635,0.304279579597001,0.303740414034867,0.238922851985672,0.239061234809925,0.2801780521795,0.279623532304614,0.297331724955827,0.296068948069051,0.194576880137849,0.172742312826113,0.161148578381683,0.161409771615176,0.129018591453167,0.123972714695015,0.116910121881567,0.0817509742501953,-0.0691544356218285,-0.0882488304977762,-0.0668760724036346,-0.0432249510912992,-0.464504319077655,-0.438829257818491,-0.364552765384014,-0.487430688993804,-0.0173478309878754,-0.040367961649072,-0.0100777281081512,0.0274826083124937,0.174265173801735,0.13822168432963,0.134437999956578,0.0908271417383699],[0.984739898920356,0.977435647969009,0.984737349411409,0.977434792810412,0.979738461686805,0.979736802252224,0.977038264534849,0.977039838171052,0.976426494517971,0.978592107752985,0.975847852099327,0.983501976641657,0.542922568539976,0.540822594700489,0.593319673748379,0.590319009535292,0.546984252549562,0.543737421296009,0.504710515360331,0.500070659652245,-0.0405858746614949,-0.0334892548074586,-0.0287998297938816,-0.0500322377516548,-0.0303467902173076,-0.0463312945833204,-0.076021583786011,-0.0798472637387719,-0.174551041637793,-0.170807063769367,-0.278793792068462,-0.491023270798226,-0.481403194083101,-0.754846782058497,-0.939634983280338,-0.843502168812051,-1.75217236568105,-1.87392478848685,-1.97576659142882,-2.30120262011855,-9.38155435571526,-9.60161249559307,-9.76049397240092,-10.2983150658944],[895,560,876,670,611.666666666667,632,350,380,863,2737.33333333333,639,6710,480,640,400,410,588.333333333333,637.666666666667,885,863,560,2308,480,1126,1047,625.666666666667,510,350,6520,639,2677.33333333333,873,7100,2826.33333333333,659,720,669,6450,2660.66666666667,863,579,1450,793,350],[91.4,194.2,91.5,60.3,145.633333333333,102.166666666667,154.7,151.3,84.5,92.4,94.3,98.4,106.1,56.4,144.3,145.8,117.2,97.6,101.2,90.6,758.5,386.4,405.8,480.333333333333,125.3,251.966666666667,296.1,224.8,99,99,93.7333333333333,83.2,98.7,86.2333333333333,88.1,71.9,95.1,99.5,92.7666666666667,83.7,200.4,302.6,334.933333333333,501.8],[7.6171875,0.62958984375,8.00781249902344,0.4169921875,2.92740885416667,3.13378906217448,0.9765625,0.53544921875,2.24609375,14.9739583333333,3.7109375,38.96484375,0.6890625,0.6962890625,0.78544921875,0.9765625,3.03056640625,3.22688802050781,7.6171875,8.00781249902344,1.85546875,5.6640625,0.42216796875,2.9296875,8.00781249902344,3.13551432259115,1.26953125,0.9765625,45.99609375,3.61328125,17.4153645833333,2.63671875,41.796875,15.91796875,3.7109375,2.24609375,3.3203125,38.8671875,14.74609375,2.05078125,1.07421875,27.44140625,10.0911458333333,1.7578125]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>Mean-squared error<\/th>\n      <th>Poisson loss<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **ALRA (log norm)**<sup><a href="/bibliography#linderman2018zero" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KlugerLab/ALRA).

<!-- -->

-   **ALRA (log norm, reversed normalization)**<sup><a href="/bibliography#linderman2018zero" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KlugerLab/ALRA).

<!-- -->

-   **ALRA (sqrt norm)**<sup><a href="/bibliography#linderman2018zero" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KlugerLab/ALRA).

<!-- -->

-   **ALRA (sqrt norm, reversed normalization)**<sup><a href="/bibliography#linderman2018zero" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KlugerLab/ALRA).

<!-- -->

-   **DCA**<sup><a href="/bibliography#eraslan2019single" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/theislab/dca).

<!-- -->

-   **KNN smoothing**<sup><a href="/bibliography#openproblems" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Iterative KNN smoothing**<sup><a href="/bibliography#wagner2018knearest" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/yanailab/knn-smoothing).

<!-- -->

-   **MAGIC**<sup><a href="/bibliography#van2018recovering" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/MAGIC).

<!-- -->

-   **MAGIC (approximate)**<sup><a href="/bibliography#van2018recovering" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/MAGIC).

<!-- -->

-   **MAGIC (approximate, reversed normalization)**<sup><a href="/bibliography#van2018recovering" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/MAGIC).

<!-- -->

-   **MAGIC (reversed normalization)**<sup><a href="/bibliography#van2018recovering" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/KrishnaswamyLab/MAGIC).

<!-- -->

-   **No denoising**<sup><a href="/bibliography#openproblems" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Perfect denoising**<sup><a href="/bibliography#openproblems" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **No denoising**: Missing 'method_description'.

<!-- -->

-   **Perfect denoising**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **Pancreas (inDrop)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">9</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **1k Peripheral blood mononuclear cells**<sup><a href="/bibliography#10x2018pbmc" target="_blank">8</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Tabula Muris Senis Lung**<sup><a href="/bibliography#tabula2020single" target="_blank">7</a></sup>: Missing 'dataset_description'.

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
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method knn_smoothing performs much worse than baselines.
  Task id: denoising
  Method id: knn_smoothing
  Metric id: poisson
  Worst score: -10.298315065894421%
"> Scaling </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method knn_smoothing performs much worse than baselines.
  Task id: denoising
  Method id: knn_smoothing
  Metric id: poisson
  Worst score: -10.298315065894421%
"> Worst score knn_smoothing poisson </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method knn_smoothing performs much worse than baselines.
  Task id: denoising
  Method id: knn_smoothing
  Metric id: poisson
  Worst score: -10.298315065894421%
"> -10.29832 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method knn_smoothing performs much worse than baselines.
  Task id: denoising
  Method id: knn_smoothing
  Metric id: poisson
  Worst score: -10.298315065894421%
"> worst_score &gt;= -1 </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method knn_smoothing performs much worse than baselines.
  Task id: denoising
  Method id: knn_smoothing
  Metric id: poisson
  Worst score: -10.298315065894421%
"> ✗✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: denoising
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: denoising
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: denoising
  Field: dataset_description
"> 1.00000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: denoising
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: denoising
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: denoising
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: denoising
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: denoising
  Field: method_description
"> 1.00000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: denoising
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: denoising
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: denoising
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: denoising
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: denoising
  Field: metric_description
"> 1.00000 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: denoising
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: denoising
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
