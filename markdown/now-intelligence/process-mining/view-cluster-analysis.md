---
title: View a cluster analysis
description: View a cluster analysis of the top three clusters for an activity, connection between activities, or route.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cluster analysis, Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# View a cluster analysis

View a cluster analysis of the top three clusters for an activity, connection between activities, or route.

View a completed cluster analysis one of these ways.

-   Select a connection or activity from the process map which has had a cluster analysis performed on it. In the metrics box, select **View**.
-   From the Scheduled tasks panel, select **View result** for the selected cluster task.
-   From the Summary and insights page, select **Requestor intent \(cluster\) View results** in the box for the insight you want to view.

## Cluster analysis results

In the Cluster analysis results dialog, the top biggest clusters and the high quality clusters are displayed.

![Cluster analysis results dialog](../image/cluster-analysis-results.png)

The results dialog shows the title of the connection or activity, or the number of routes the analysis was performed on. Results show these statistics for the top biggest and high-quality clusters.

<table id="table_dht_vzj_5bc"><tbody><tr><td>

Concept

</td><td>

List of the most prominent words or content found in a cluster. We have used `Short description` as the input field type that helps the system identify the records we want to include in the cluster. So, the above cluster analysis result displays the most recurring words that appear in the short description of the records.

</td></tr><tr><td>

Size

</td><td>

Number of records in the cluster.

</td></tr><tr><td>

Quality

</td><td>

Percentage value of how similar the cases are.

</td></tr><tr><td>

Purity

</td><td>

Metric for the class which appears most frequently in the cluster, based on distribution significance. Purity insights help identify the most frequent field value in a cluster.

</td></tr></tbody>
</table>## View clusters in a treemap

To see further details about clusters, including clusters beyond the top three listed on the results dialog, if any, select **View all clusters in a Treemap**.

You can use a treemap visualization to help you better understand different aspects of the clusters, and determine which clusters to focus on first. The treemap plot appears on the Cluster Visualization tab.

![Clustering treemap](../image/clustering-treemap-new.png)

For additional information on using a treemap, see [Create and train a clustering solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-clustering-solution.md).

**Parent Topic:**[Cluster analysis](../concept/cluster-analysis.md)

