---
title: Configure DBSCAN for a clustering solution
description: Consider applying the Density Based Spatial Clustering of Applications with Noise \(DBSCAN\) algorithm to your clustering solution. DBSCAN is available as an alternative to the default clustering algorithm, k-means.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure DBSCAN for a clustering solution

Consider applying the Density Based Spatial Clustering of Applications with Noise \(DBSCAN\) algorithm to your clustering solution. DBSCAN is available as an alternative to the default clustering algorithm, k-means.

## Before you begin

**Note:** Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that your use case benefits from what the technology offers. For more information, see the [Dive deeper with Clustering Advanced Parameters](https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847) article on ServiceNow Community.

-   Create a clustering solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

Predictive Intelligence uses the k-means algorithm by default in its clustering framework. DBSCAN is another clustering algorithm that's also used in data mining and machine learning. Some users prefer DBSCAN as it doesn't require you to specify the number of clusters in the data before clustering. For a summary of the pros and cons for each algorithm, see this [conversation](https://www.researchgate.net/post/What_is_the_difference_between_K-MEAN_and_density_based_clustering_algorithm_DBSCAN) and this [article](https://medium.com/@soroushhashemifar/kmeans-vs-dbscan-d9d5f9dbee8b).

In this example scenario, you apply DBSCAN to a clustering solution.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  Open a clustering solution definition form.

    In this example scenario, you use an Incidents clustering solution definition form.

    ![An example clustering solution definition on which you apply the DBSCAN parameter.](../images/configure-dbscan-clustering1.png)

3.  On the Advanced Solution Settings tab in the Related Links section of the form, select **Solution Parameters** from the picker, then click **New**.

    ![How to select the Solution Parameters option for creating the parameter.](../images/tf-idf-similarity-solution2.png)

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, select the search icon.

    2.  In the ML Solution Parameters screen, select **Use DBSCAN algo for clustering**.

        ![How to create the parameter record by selecting the Search button and then selecting the DBSCAN key's Short Description.](../images/configure-dbscan-clustering3.png)

5.  Select **Submit**.

    The Advanced Solution Setting record appears. The field **User Inputs** is grayed out because it does not apply to this algorithm.

    ![How to create a Solution Parameter record you create from the values you just assigned.](../images/configure-dbscan-clustering4.png)

6.  Select **Submit**.

    **Result:** DBSCAN is configured for your clustering solution. Its solution parameter appears on the Advanced Solution Settings tab of your clustering solution definition form.

    ![When you submit the record you created, the DBSCAN solution parameter appears on your clustering solution definition form.](../images/configure-dbscan-clustering5.png)


**Related topics**  


[Create and train a clustering solution](create-clustering-solution.md)

