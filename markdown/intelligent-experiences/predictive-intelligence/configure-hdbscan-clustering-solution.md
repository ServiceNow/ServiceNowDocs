---
title: Configure HDBSCAN for a clustering solution
description: Consider applying the Hierarchical Density Based Spatial Clustering of Applications with Noise \(HDBSCAN\) algorithm to your clustering solution. HDBSCAN is available as an alternative to the default clustering algorithm, k-means.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure HDBSCAN for a clustering solution

Consider applying the Hierarchical Density Based Spatial Clustering of Applications with Noise \(HDBSCAN\) algorithm to your clustering solution. HDBSCAN is available as an alternative to the default clustering algorithm, k-means.

## Before you begin

**Note:** Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that your use case benefits from what the technology offers. For more information, see the [Dive deeper with Clustering Advanced Parameters](https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847) article on ServiceNow Community.

-   Create a clustering solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

You can apply the HDBSCAN algorithm to help the system identify data samples that aren't assigned to any cluster. For example, you can apply HDBSCAN to support Topic Discovery.

Predictive Intelligence implements the k-means algorithm by default in its clustering framework. HDBSCAN is similar to the DBSCAN clustering algorithm except that it works with minimum-sized clusters and can help deliver more stable and persistent clusters. For a summary of how HDBSCAN works, see [this article](https://hdbscan.readthedocs.io/en/latest/how_hdbscan_works.html). For a comparison between DBSCAN and HDBSCAN, see [this article](https://hdbscan.readthedocs.io/en/latest/comparing_clustering_algorithms.html#dbscan) and [this article](https://hdbscan.readthedocs.io/en/latest/comparing_clustering_algorithms.html#hdbscan).

**Note:** Clustering solutions trained with HDBSCAN do not support cluster updates. Updates on these solutions fail and the solutions are not logged in the ml\_cluster\_detail\_table. Use DBSCAN or k-means training methods if you want to enable cluster updates.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

    ![The Predictive Intelligence navigation path to the Clustering Definitions list view where you create a new clustering solution definition.](../images/configure-hdbscan-clustering-solution1.png)

2.  Select **New**.

3.  Create a new clustering solution definition form or use an existing one.

    In this example scenario, you create the hdbscan-sf clustering definition form as in the image below. Configure the fields as follows:

    -   **Label**: `hdbscan-sf`
    -   **Word Corpus**: `incident_wc`, or any other word corpus that has incident record data \(from the Washington DC release, a word corpus is not needed, so this field does not appear\).
    -   **Table**: Incident \[incident\]
    -   **Fields**: Short description
    -   **Update Frequency**: Do not update
    -   **Stopwords**: Default English Stopwords
    -   **Training Frequency**: Every 30 days
    -   **Processing Language**: English
    ![An example clustering solution definition you create on which you will apply the DBSCAN parameter.](../images/configure-hdbscan-clustering-solution2.png)

4.  Select **Submit &amp; Train**.

5.  On the Advanced Solution Settings tab in the Related Links section of the trained form, select **Solution Parameters** from the picker, then select **New**.

    ![How to select the Solution Parameters option for creating the parameter.](../images/configure-hdbscan-clustering-solution3.png)

6.  Create a parameter record.

    1.  In the **Solution Parameters** field, click the search icon.

    2.  In the ML Solution Parameters screen, select **Use HDBSCAN algo for clustering**.

        ![How to create the parameter record by selecting the Search button, and then selecting the HDBSCAN key's Short Description.](../images/configure-hdbscan-clustering-solution4.png)

7.  Select **Submit**.

    The Advanced Solution Setting record appears with the HDBSCAN algorithm applied to the record. The field **User Inputs** is grayed out because it does not apply to this algorithm.

    ![The new Solution Parameter record you create from the values you just assigned.](../images/configure-hdbscan-clustering-solution5.png)

8.  Select **Submit**.

    **Result**: HDBSCAN is configured for your clustering solution. Its solution parameter appears on the Advanced Solution Settings tab of your clustering solution definition form.

    ![When you submit the record you created, the HDBSCAN solution parameter appears on your clustering solution definition form.](../images/configure-hdbscan-clustering-solution6.png)


**Related topics**  


[Create and train a clustering solution](create-clustering-solution.md)

