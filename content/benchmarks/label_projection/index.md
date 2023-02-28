---
title: "Label Projection"
summary: "Automated cell type annotation from rich, labeled reference data"
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

A major challenge for integrating single cell datasets is creating matching cell type
annotations for each cell. One of the most common strategies for annotating cell types
is referred to as
["cluster-then-annotate"](https://openproblems.bio/bibliography#kiselev2019challenges) whereby
cells are aggregated into clusters based on feature similarity and then manually
characterized based on differential gene expression or previously identified marker
genes. Recently, methods have emerged to build on this strategy and annotate cells
using [known marker genes](https://openproblems.bio/bibliography#pliner2019supervised). However,
these strategies pose a difficulty for integrating atlas-scale datasets as the
particular annotations may not match.

To ensure that the cell type labels in newly generated datasets match existing reference
datasets, some methods align cells to a previously annotated [reference
dataset](https://openproblems.bio/bibliography#hou2019scmatch) and then
*project* labels from the reference to the new dataset.

Here, we compare methods for annotation based on a reference dataset. The datasets
consist of two or more samples of single cell profiles that have been manually annotated
with matching labels. These datasets are then split into training and test batches, and
the task of each method is to train a cell type classifer on the training set and
project those labels onto the test set.

## Summary

<figure>
<img src="index.markdown_strict_files/figure-markdown_strict/summary-1.png" width="850" alt="Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric)." />
<figcaption aria-hidden="true">Overview of the results per method. This figures shows the mean of the scaled scores (group Overall), the mean scores per dataset (group Dataset) and the mean scores per metric (group Metric).</figcaption>
</figure>

## Metrics

-   **Accuracy**<sup><a href="/bibliography#grandini2020metrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **F1 score**<sup><a href="/bibliography#grandini2020metrics" target="_blank">1</a></sup>: Missing 'metric_description'.

<!-- -->

-   **Macro F1 score**<sup><a href="/bibliography#grandini2020metrics" target="_blank">1</a></sup>: Missing 'metric_description'.

## Results

<div class="datatables html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-04df5aada2b7fc85ff9b" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-04df5aada2b7fc85ff9b">{"x":{"filter":"none","vertical":false,"extensions":["Select","SearchPanes","Buttons"],"caption":"<caption>Results table of the scores per method, dataset and metric (after scaling). Use the filters to make a custom subselection of methods and datasets. The \"Overall mean\" dataset is the mean value across all datasets.<\/caption>","data":[["Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Seurat reference mapping (SCTransform) <sup><a href=\"/bibliography#hao2021integrated\" target=\"_blank\">5<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Logistic regression (log CP10k) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","Logistic regression (log scran) <sup><a href=\"/bibliography#hosmer2013applied\" target=\"_blank\">2<\/a><\/sup>","XGBoost (log scran) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","scANVI (All genes) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","Multilayer perceptron (log CP10k) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","XGBoost (log CP10k) <sup><a href=\"/bibliography#chen2016xgboost\" target=\"_blank\">4<\/a><\/sup>","Multilayer perceptron (log scran) <sup><a href=\"/bibliography#hinton1989connectionist\" target=\"_blank\">3<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#xu2021probabilistic\" target=\"_blank\">7<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","K-neighbors classifier (log scran) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","scArches+scANVI (All genes) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","K-neighbors classifier (log CP10k) <sup><a href=\"/bibliography#cover1967nearest\" target=\"_blank\">6<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","scArches+scANVI (Seurat v3 2000 HVG) <sup><a href=\"/bibliography#lotfollahi2020query\" target=\"_blank\">8<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>","Majority Vote <sup><a href=\"/bibliography#openproblems\" target=\"_blank\">9<\/a><\/sup>"],["Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Overall mean","Overall mean","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Overall mean","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","Overall mean","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Overall mean","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Pancreas (random split with label noise) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Tabula Muris Senis Lung (random split) <sup><a href=\"/bibliography#tabula2020single\" target=\"_blank\">11<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Pancreas (by batch) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","Overall mean","Zebrafish (random split) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>","Pancreas (random split) <sup><a href=\"/bibliography#luecken2022benchmarking\" target=\"_blank\">10<\/a><\/sup>","CeNGEN (random split) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","CeNGEN (split by batch) <sup><a href=\"/bibliography#hammarlund2018cengen\" target=\"_blank\">12<\/a><\/sup>","Zebrafish (by laboratory) <sup><a href=\"/bibliography#wagner2018single\" target=\"_blank\">13<\/a><\/sup>"],[0.979584233502044,0.979331660031331,0.96804909672203,0.947357772942168,0.9466603204518,0.946414066470442,0.944197421519154,0.943420538377195,0.942810248947656,0.932702729427754,0.932346046167085,0.926339010766234,0.917898156766557,0.915755324477614,0.914024535699316,0.911699950732907,0.910427757813906,0.902426432318138,0.897968555754436,0.889285054130056,0.886742466697398,0.884352685303029,0.874921839359495,0.868275431686993,0.868221053970786,0.867497439528886,0.860210032877026,0.860010828028297,0.858546140868408,0.854519270870381,0.853451191125112,0.852910208587104,0.846493105736068,0.843119394629617,0.841606733982204,0.838441497596685,0.837333561094953,0.830548767528284,0.828293919035899,0.826402157209829,0.824462813065276,0.822433520274325,0.820653335677235,0.819589686716546,0.817211034646046,0.817091849758233,0.809963565780372,0.806970836202524,0.805904231276224,0.803705520366789,0.801851957450198,0.796707075246728,0.79232520131761,0.790076313162003,0.789431347707689,0.785024321127082,0.783981607468455,0.783973721037746,0.783035241447677,0.78216627348645,0.773225236428418,0.767844128581696,0.766601568596026,0.753540665619103,0.752837287594686,0.750491026719883,0.744118322863857,0.733716914243566,0.731771968874222,0.730937056566701,0.726110381443243,0.725937937660619,0.721190031273837,0.712496159198625,0.710281596799926,0.706118695040098,0.705858469629598,0.704912223290013,0.695887914965164,0.694209970720233,0.68391301792809,0.6834196251732,0.677919220125159,0.661829359055619,0.644455058242368,0.629393714905033,0.62598960463969,0.624225367019751,0.593491517010136,0.588475604536469,0.573836513169914,0.510731451728399,0.500454013274479,0.48737091836539,0.481683993511765,0.479744304043931,0.471135364424646,0.462889170913323,0.44827151133899,0.328210462382397,0.254517898465406,0.235446325222617,0.232542933679096,0.223324688450318,0.221368380133836,0.218065078044102,0.217972567531239,0.217066930316212,0.216410116813207,0.205511255845506,0.202620476823029,0.194859591684858,0.17510726007049,0.166291398816052,0.136588992397882,0.121436651418857,0.0477318413101885,0.0405114959896927,0.0385200239952352,0.0315022480630412,0.0132729955407935,0.00839255299795472,0.00663043108975944,0.00511598685189467,-0.00565764421042996,-0.0280429477657532],[0.984393289114319,0.984783456886461,0.970737417089348,0.953576341127923,0.977370269215763,0.975391498881432,0.960593055013656,0.980881779165041,0.970544369873229,0.956375838926175,0.955130706203668,0.954264099037139,0.924669603524229,0.918502202643172,0.922627235213205,0.947730398899587,0.9215859030837,0.91784140969163,0.935123042505593,0.943325876211782,0.954350370659384,0.903303964757709,0.941196698762036,0.88855951364116,0.916437414030261,0.972298088177916,0.967616074912212,0.960477255779269,0.96420581655481,0.873938602220771,0.847577092511013,0.928784489187174,0.948762035763411,0.855726872246696,0.946011004126547,0.851982378854626,0.861233480176211,0.937414030261348,0.904175988068605,0.855197708888107,0.840440165061898,0.839823142239863,0.846706526654273,0.926066024759285,0.824247600864191,0.929769801014436,0.941540577716644,0.846186440677966,0.835301210872733,0.831381765349588,0.817715922222781,0.829322212731749,0.830696985856088,0.943035505267265,0.944596176355833,0.936614466815809,0.828177966101695,0.827542372881356,0.935123042505593,0.824364406779661,0.81843220338983,0.795280670237921,0.813959063038418,0.793628902778846,0.876595744680851,0.787505082594907,0.784322033898305,0.783262711864407,0.765888610201293,0.854711246200608,0.768008474576271,0.7875,0.845592705167173,0.827963525835866,0.772724845771422,0.824924012158055,0.761565448245221,0.782668500687758,0.850881057268722,0.767710663683818,0.822492401215805,0.768996960486322,0.809726443768997,0.825330396475771,0.78419452887538,0.744626983760876,0.763609246830723,0.757838983050848,0.693720673313893,0.728389830508475,0.762555066079295,0.630667879767452,0.695154185022026,0.660302466964779,0.641945288753799,0.645932773953675,0.613983050847458,0.579147560187483,0.602542372881356,0.325525525525526,0.414711350047732,0.226493159826493,0.22308975642309,0.214014014014014,0.197664330997664,0.215548882215549,0.202202202202202,0.21675008341675,0.203870537203871,0.251671732522796,0.187454120787454,0.337888760488369,0.168234901568235,0.234650455927052,0.107974641307975,0.104904904904905,0.195749440715884,0.146696035242291,0.0668693009118541,0.172971114167813,0.0950653356506429,0.0949152542372881,0.138509559110417,0.0324071747977692,0.00790273556231003,-0.0286286286286286],[0.9843211893875,0.984671301291028,0.970651449032685,0.954117604589021,0.976456634682323,0.974366439917533,0.960125203760691,0.9806886504234,0.969321831230518,0.955433231046378,0.95424463927348,0.954928831583625,0.924134471322242,0.917917901551441,0.921608973460573,0.946911012177004,0.921022367648428,0.916837870253124,0.933607364492913,0.941987814611164,0.95320959769683,0.900943948365798,0.94231987842517,0.888926603416463,0.916360634102099,0.968953439273169,0.964466288729688,0.95560039089396,0.959665705095971,0.875724746357711,0.844693019608479,0.926656331557725,0.94700523572785,0.850529081155939,0.944199725834686,0.85062464963988,0.858549100562585,0.93573778521752,0.908138963257028,0.854119318702577,0.838538705101813,0.842301499020818,0.849234371249699,0.924175956031915,0.837795925153747,0.920175811534622,0.9385705708073,0.844036032611456,0.834197133186785,0.834544299562323,0.823216769704523,0.827939756493131,0.836456379431181,0.930801402021824,0.933045934116485,0.92270850578446,0.827233650338259,0.825718548082985,0.921580941587721,0.824990638451813,0.818825028627606,0.801019819553589,0.822382267043656,0.802101125066471,0.872118614810162,0.795493534802799,0.780247595107084,0.78363908372245,0.767188970034302,0.853388566972129,0.763496135796238,0.782382584200789,0.839449408368848,0.838302679828986,0.776380366833234,0.830035192257465,0.763079349778373,0.786758452375187,0.815872355873323,0.798904188309815,0.827966437461618,0.79885556415361,0.827003575881189,0.781921934387187,0.799878282435875,0.716752081374841,0.724156942651542,0.701686390396316,0.664681900251696,0.662782597916154,0.696863848265775,0.584583842556002,0.591667583874916,0.565598886135642,0.607606753511646,0.561876545400536,0.512232196263091,0.523538992159251,0.489891023953189,0.386592411520371,0.277866837532717,0.258867494743484,0.261811214549055,0.269834390978811,0.213824337901621,0.247093813409049,0.249331515941122,0.278949934637778,0.226057765175618,0.20545928377582,0.19495198215873,0.202438022455311,0.169766836096191,0.175529964383752,0.0960371422633604,0.107807500466051,-0.0240117499002757,-0.00876806656780211,0.0139531540189906,-0.0421675188839463,-0.033091599894716,-0.0396172627215389,-0.0744205984108175,-0.0123243778615806,-0.0232165070302024,-0.0402067177815643],[0.970038222004312,0.968540221916504,0.962758424044057,0.934379373109559,0.886154057457314,0.889484260612362,0.911874005783115,0.868691185543143,0.888564545739221,0.886299118310708,0.887662793024108,0.869824101677939,0.904890395453201,0.91084586923823,0.89783739842417,0.840458441122128,0.888675002709589,0.872600017009661,0.825175260264802,0.782541471567221,0.752667431735981,0.84881014278558,0.74124894089128,0.827340178003358,0.771865113779998,0.661240791135573,0.648547734989177,0.663954837411664,0.651766900954443,0.813894464032661,0.868083461255843,0.703289805016412,0.643712045716941,0.823102230486217,0.63460947198538,0.812717464295549,0.792218102546063,0.618494487105982,0.672566805782064,0.769889444038804,0.794409569032116,0.785175919562293,0.766019109127733,0.60852707935844,0.7895895779202,0.601329936725642,0.549779548817173,0.73069003531815,0.748214349769156,0.745190496188455,0.764623180423291,0.732859256515303,0.70982223866556,0.496392032196921,0.490651932650749,0.495749990780976,0.696533205965412,0.698660242148898,0.492401740249718,0.697143775227875,0.682418477267818,0.70723189595358,0.663463375706003,0.664891969011993,0.509797503293047,0.668474462761943,0.667785339586182,0.634248947143841,0.662238326387072,0.484711356527365,0.646826533957222,0.607931228781067,0.478527980285489,0.471222271931023,0.581739577795121,0.463396880704774,0.592930610865199,0.545309716807093,0.420910331753446,0.516015060167066,0.401280215106846,0.482406350879668,0.397027640725291,0.3782357463039,0.349292363415847,0.426802079579381,0.390202624436806,0.41315072761209,0.42207197746482,0.374254385184778,0.262090625164672,0.316942632861742,0.214540270926494,0.236211401995749,0.195499938269848,0.231423592777583,0.287190846163388,0.285980960393236,0.252381137182425,0.272513450101293,0.0709755078157706,0.220978321097875,0.212727830065143,0.186125660358128,0.252616471502223,0.191552538507708,0.202383984450391,0.155500772894107,0.219302048060132,0.159402751237903,0.225455327522902,0.0442519921108957,0.187320042547045,0.0886937761373534,0.205755193622312,0.151597548885615,-0.0285421668850424,-0.0163934807054105,0.0347376170548608,-0.0362968510947431,-0.0221547491335464,-0.0301203325218851,-0.0441976674303217,-0.0047348363805046,-0.00165916116339748,-0.0152934968870666],[529,628,1056,430,1899,579,2028,2002,1751,1108,519,359,568,418,769,1910,1630,1568,419,1729,1307,1486,1480,1343,1668,2879,4448,7679,4259,3197,368,1368,2791,1206,5643,1739,1507,8939,1477,1079,520,2728,410,1439,3188,1417,2990,1589,2370,677,8268,3809,2180,23550,1948,3756,1418,419,4127,419,1718,1843.125,2040.5,688.5,1438,3533.75,1418,1019,424.375,3727,1899,409,3350,9350,1900.75,5270,1613,1369,8423,548,1468,3159,490,3669,3068,7466.25,1518,4959,6106.5,9589,5527,8882.25,7265,6500,14580,10728,5357,5280.75,8230,1646,7540,260,1499,1589,6288,439,889,1093,5048,10520,5627,8917,1197,10970,3550,260,389,458,5590,350,388.75,348,478,399,349,339],[121.4,205.7,302.4,169.1,110.2,121.8,218.1,256.3,109.7,374.3,97.1,207,384.9,148.3,478.9,109.7,165.7,114.6,113.8,290.2,107.8,122.6,145.9,280.7,236.9,542.3,630.8,1860.6,667.3,162.2,127.5,95.9,337.8,100.2,2762.1,330.1,290,2151.9,353.9,492.5,87,712.7,134.5,121.7,138.5,103.2,328.4,129.3,101.1,165.4625,752.9,105.6,115.2125,2606.3,320.4,521.2,106.4,118.7,677.5,290.1,162.9,791.4125,197.3625,314.0375,253,403.4875,331.9,102.1,111.6125,219,451.9,98.2,119.2,741.9,118.2875,3562.8,101.025,99.9,2801.4,447.1,343.2,145.7,108.2,361.2,103.5,2236.95,101.1,2198.6,1255.2625,2729.8,2559,2349.2875,2359.4,2793.7,2792,1184.6,2746.9,1151.95,2354.3,115.4,2733.6,110.7,115.1,205.9,2718.5,141.8,278.3,113,2616.4,1185.1,2371.9,664.2,97.7,2702.7,355.3,126.6,25.4,10.1,2312.4,23.8,23.1875,30.7,28.6,25.9,12.5,28.5],[2.1484375,2.1484375,2.5390625,2.24609375,44.62890625,2.1484375,8.10546875,8.30078125,50.29296875,2.5390625,2.34375,2.24609375,1.26953125,1.26953125,2.63671875,105.6640625,5.2734375,5.17578125,2.24609375,8.10546875,8.30078125,555.17578125,8.30078125,1.85546875,8.30078125,2.24609375,3.515625,5.859375,3.61328125,6.640625,2.1484375,8.30078125,2.1484375,5.2734375,4.39453125,5.56640625,1.46484375,5.76171875,8.30078125,1.66015625,2.5390625,1.953125,2.734375,8.30078125,6.640625,8.30078125,2.24609375,367.1875,6.640625,1.85546875,6.640625,852.5390625,322.15576171875,5.76171875,2.24609375,2.63671875,4.8828125,1.5625,4.78515625,1.5625,4.8828125,2.1240234375,6.65283203125,1.806640625,1.7578125,6.8115234375,1.85546875,4.8828125,2.52685546875,6.640625,5.37109375,2.44140625,543.1640625,6.640625,6.640625,1.85546875,6.65283203125,8.30078125,3.80859375,2.1484375,1.5625,6.640625,2.5390625,1.5625,6.640625,5.6884765625,8.30078125,7.6171875,4.8828125,4.98046875,5.76171875,7.666015625,9.08203125,9.86328125,11.42578125,6.25,5.859375,5.810546875,7.51953125,58.59375,12.59765625,1.85546875,4.8828125,5.76171875,3.90625,1.85546875,2.1484375,4.8828125,5.37109375,6.4453125,6.93359375,3.61328125,4.8828125,15.4296875,1.66015625,3.22265625,1.46484375,0.826953125,17.48046875,1.46484375,0.95537109375,0.2283203125,1.46484375,0.22626953125,0.96875,0.99814453125]],"container":"<table class=\"stripe compact\">\n  <thead>\n    <tr>\n      <th>Method<\/th>\n      <th>Dataset<\/th>\n      <th>Mean score<\/th>\n      <th>Accuracy<\/th>\n      <th>F1 score<\/th>\n      <th>Macro F1 score<\/th>\n      <th>Runtime (s)<\/th>\n      <th>CPU (%)<\/th>\n      <th>Memory (GB)<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"Bt","paging":false,"columnDefs":[{"targets":7,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":6,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"targets":8,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":3,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":4,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":5,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"searchPanes":{"show":false},"targets":[2,3,4,5,6,7,8]},{"searchPanes":{"preSelect":"Overall mean"},"targets":1},{"className":"dt-right","targets":[2,3,4,5,6,7,8]}],"buttons":["searchPanes","csv","excel"],"language":{"searchPanes":{"collapse":"Filter datasets / methods"}},"scrollX":true,"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render","options.columnDefs.2.render","options.columnDefs.3.render","options.columnDefs.4.render","options.columnDefs.5.render","options.columnDefs.6.render"],"jsHooks":[]}</script>

## Details

<details>
<summary>
Methods
</summary>

-   **K-neighbors classifier (log CP10k)**<sup><a href="/bibliography#cover1967nearest" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html).

<!-- -->

-   **K-neighbors classifier (log scran)**<sup><a href="/bibliography#cover1967nearest" target="_blank">6</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html).

<!-- -->

-   **Logistic regression (log CP10k)**<sup><a href="/bibliography#hosmer2013applied" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html).

<!-- -->

-   **Logistic regression (log scran)**<sup><a href="/bibliography#hosmer2013applied" target="_blank">2</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html).

<!-- -->

-   **Majority Vote**<sup><a href="/bibliography#openproblems" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **Multilayer perceptron (log CP10k)**<sup><a href="/bibliography#hinton1989connectionist" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPClassifier.html).

<!-- -->

-   **Multilayer perceptron (log scran)**<sup><a href="/bibliography#hinton1989connectionist" target="_blank">3</a></sup>: Missing 'method_description'. Links: [Docs](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPClassifier.html).

<!-- -->

-   **Random Labels**<sup><a href="/bibliography#openproblems" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **scANVI (All genes)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scANVI (Seurat v3 2000 HVG)**<sup><a href="/bibliography#xu2021probabilistic" target="_blank">7</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scArches+scANVI (All genes)**<sup><a href="/bibliography#lotfollahi2020query" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **scArches+scANVI (Seurat v3 2000 HVG)**<sup><a href="/bibliography#lotfollahi2020query" target="_blank">8</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/YosefLab/scvi-tools).

<!-- -->

-   **Seurat reference mapping (SCTransform)**<sup><a href="/bibliography#hao2021integrated" target="_blank">5</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/satijalab/seurat).

<!-- -->

-   **True Labels**<sup><a href="/bibliography#openproblems" target="_blank">9</a></sup>: Missing 'method_description'. Links: [Docs](https://github.com/openproblems-bio/openproblems).

<!-- -->

-   **XGBoost (log CP10k)**<sup><a href="/bibliography#chen2016xgboost" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://xgboost.readthedocs.io/en/stable/index.html).

<!-- -->

-   **XGBoost (log scran)**<sup><a href="/bibliography#chen2016xgboost" target="_blank">4</a></sup>: Missing 'method_description'. Links: [Docs](https://xgboost.readthedocs.io/en/stable/index.html).

</details>
<details>
<summary>
Baseline methods
</summary>

-   **Random Labels**: Missing 'method_description'.

<!-- -->

-   **True Labels**: Missing 'method_description'.

</details>
<details>
<summary>
Datasets
</summary>

-   **CeNGEN (split by batch)**<sup><a href="/bibliography#hammarlund2018cengen" target="_blank">12</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **CeNGEN (random split)**<sup><a href="/bibliography#hammarlund2018cengen" target="_blank">12</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (by batch)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">10</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (random split)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">10</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Pancreas (random split with label noise)**<sup><a href="/bibliography#luecken2022benchmarking" target="_blank">10</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Tabula Muris Senis Lung (random split)**<sup><a href="/bibliography#tabula2020single" target="_blank">11</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Zebrafish (by laboratory)**<sup><a href="/bibliography#wagner2018single" target="_blank">13</a></sup>: Missing 'dataset_description'.

<!-- -->

-   **Zebrafish (random split)**<sup><a href="/bibliography#wagner2018single" target="_blank">13</a></sup>: Missing 'dataset_description'.

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
  Task id: label_projection
  Field: dataset_description
"> Dataset info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: label_projection
  Field: dataset_description
"> Pct 'dataset_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: label_projection
  Field: dataset_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: label_projection
  Field: dataset_description
"> percent_missing(dataset_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Dataset metadata field 'dataset_description' should be defined
  Task id: label_projection
  Field: dataset_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: label_projection
  Field: method_description
"> Method info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: label_projection
  Field: method_description
"> Pct 'method_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: label_projection
  Field: method_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: label_projection
  Field: method_description
"> percent_missing(method_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Method metadata field 'method_description' should be defined
  Task id: label_projection
  Field: method_description
"> ✗✗ </td>
  </tr>
  <tr>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: label_projection
  Field: metric_description
"> Metric info </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: label_projection
  Field: metric_description
"> Pct 'metric_description' missing </td>
   <td style="text-align:right;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: label_projection
  Field: metric_description
"> 1 </td>
   <td style="text-align:left;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: label_projection
  Field: metric_description
"> percent_missing(metric_info, field) </td>
   <td style="text-align:left;color: red !important;" data-toggle="tooltip" data-container="body" data-placement="right" title="Metric metadata field 'metric_description' should be defined
  Task id: label_projection
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
