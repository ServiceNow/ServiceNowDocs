---
title: Analyze a cluster with Cluster Insight
description: Analyze a cluster by a field available on the source table. With the Cluster Insight check box, you can add a filter condition on your input field when you review the list of results.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and train a clustering solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Analyze a cluster with Cluster Insight

Analyze a cluster by a field available on the source table. With the Cluster Insight check box, you can add a filter condition on your input field when you review the list of results.

## Before you begin

-   Create a clustering solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

Drill down into a cluster and filter its records with Cluster Insight. You can add cluster insight analysis when creating a solution or editing an existing solution. For more information, see [https://www.servicenow.com/community/intelligence-ml-articles/predictive-intelligence-using-the-cluster-insight-table-to/ta-p/2301006](https://www.servicenow.com/community/intelligence-ml-articles/predictive-intelligence-using-the-cluster-insight-table-to/ta-p/2301006).![Create Cluster Insight table check box in the Clustering Definition page.](../images/clusterinsight_table_check.png)

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  Select a solution definition or create a new one.

3.  On the definition form, select the **Create Cluster Insight table** check box, then update and retrain the model.


## Result

In the **Solutions** \[ml\_solution\] table, open the trained solution, then open the **Cluster Visualization** tab. When you select a cluster, all records included in the cluster are displayed as a list. Using the filter icon \(![](../../../common/image/List_FilterIcon.png)\), open the list's filter conditions. Search for the input field from your source table. For example, if your source table is Incident and the input field is Short Description, you could filter for records containing the word "help" in the Short Description.

To make other dimensions from your source table available for filtering, add them as input fields on the solution definition form.

