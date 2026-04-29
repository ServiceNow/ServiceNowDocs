---
title: Configuring advanced settings for your ML solutions
description: Learn about advanced settings for your Predictive Intelligence machine learning \(ML\) solutions. Apply optional technology and algorithms for classification, clustering, similarity, and regression capabilities.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configuring advanced settings for your ML solutions

Learn about advanced settings for your Predictive Intelligence machine learning \(ML\) solutions. Apply optional technology and algorithms for classification, clustering, similarity, and regression capabilities.

Using advanced settings in your ML solutions is optional. If you choose to implement any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that your use case benefits from what the technology offers. For more information about several of these parameters, see the [Dive deeper with Clustering Advanced Parameters](https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847) article on ServiceNow Community.

Most of the advanced settings are limited to only one capability because their functionality is targeted to specific use cases.

## Classification, clustering, similarity, and regression advanced settings

Using the admin or ml\_admin role, you apply these technologies by configuring a parameter in the **Advanced Solution Settings** tab on your ML solution definition form.

To update or remove an existing setting: on the solution definition form, select the **Advanced Solution Settings** tab, then select the name of the solution parameter. For details, see the following procedures.

-   [Configure class recall for a classification solution](../task/configure-class-recall-for-classification-solution.md)
-   [Configure TF-IDF for solutions](../task/configure-tf-idf-classification-similarity.md)
-   [Configure DBSCAN for a clustering solution](../task/configure-dbscan-for-clustering-solution.md)
-   [Configure HDBSCAN for a clustering solution](../task/configure-hdbscan-clustering-solution.md)
-   [Configure XGBoost for classification or regression solutions](../task/configure-xgboost-classification-regression-solutions.md)
-   [Configure Connect Component algorithm and Levenshtein Distance method for a clustering solution](../task/configure-connect-component-levenshtein-distance-for-clustering.md)
-   [Apply purity on a clustering solution](../task/configure-auto-purity-cluster.md)
-   [Analyze a cluster with Cluster Insight](../task/analyze-cluster-data-source.md)

## Advanced Solution Settings for Classification

From the Zurich release, classification solutions offer the following advanced solution settings.

-   [Config parameters for model config in classification](../task/predictive-intel-config-parameters-classification.md)
-   [Configure include only top N labels](../task/predictive-intel-only-top-n-labels.md)
-   [Minimum records needed for label to include it](../task/predictive-intel-minimum-records-needed-label.md)
-   [Remove others label](../task/predictive-intel-remove-others-label.md)
-   [Use LightGBM algo for classification model training](../task/predictive-intel-lightgbm-algo.md)

-   **[Configure class recall for a classification solution](../task/configure-class-recall-for-classification-solution.md)**  
Create and apply a class recall parameter to an ML solution prior to training its data. For example, you set and apply this solution parameter to 90% recall for all records in the Email class.
-   **[Configure TF-IDF for solutions](../task/configure-tf-idf-classification-similarity.md)**  
Apply Term Frequency–Inverse Document Frequency \(TF-IDF\) encoding to classification, clustering, or similarity solutions for Predictive Intelligence.
-   **[Configure XGBoost for classification or regression solutions](../task/configure-xgboost-classification-regression-solutions.md)**  
Apply XGBoost encoding to optimize the training for your classification or regression solutions.
-   **[Configure DBSCAN for a clustering solution](../task/configure-dbscan-for-clustering-solution.md)**  
Consider applying the Density Based Spatial Clustering of Applications with Noise \(DBSCAN\) algorithm to your clustering solution. DBSCAN is available as an alternative to the default clustering algorithm, k-means.
-   **[Configure HDBSCAN for a clustering solution](../task/configure-hdbscan-clustering-solution.md)**  
Consider applying the Hierarchical Density Based Spatial Clustering of Applications with Noise \(HDBSCAN\) algorithm to your clustering solution. HDBSCAN is available as an alternative to the default clustering algorithm, k-means.
-   **[Configure Connect Component algorithm and Levenshtein Distance method for a clustering solution](../task/configure-connect-component-levenshtein-distance-for-clustering.md)**  
Apply Configure Connect Component and Levenshtein Distance method encoding to optimize the training for your clustering solutions.
-   **[Config parameters for model config in classification](../task/predictive-intel-config-parameters-classification.md)**  
Customize the training behavior of your classification solution by passing in a dictionary of parameters in JSON format.
-   **[Use LightGBM algo for classification model training](../task/predictive-intel-lightgbm-algo.md)**  
Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm as an advanced option for training classification models.
-   **[Minimum records needed for label to include it](../task/predictive-intel-minimum-records-needed-label.md)**  
Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
-   **[Configure include only top N labels](../task/predictive-intel-only-top-n-labels.md)**  
Limit your classification model to use only the most common classes when training. You can specify the number of classes to use.
-   **[Remove others label](../task/predictive-intel-remove-others-label.md)**  
Reduce noise in your classification model and enhance predictive accuracy by removing records with the label "others" from training data. These are records with a distribution frequency of under one percent.

**Parent Topic:**[Configure Predictive Intelligence](../task/configure-predictive-intelligence.md)

