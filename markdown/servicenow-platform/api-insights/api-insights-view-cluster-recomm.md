---
title: Viewing API clustering recommendations in API Insights
description: Use machine learning-based suggestions to group related API components, improving the organization and mapping of APIs within the system.
locale: en-US
release: xanadu
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimize clustering recommendations, API Insights, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing API clustering recommendations in API Insights

Use machine learning-based suggestions to group related API components, improving the organization and mapping of APIs within the system.

The Proposed API clustering tab of the Data recommendations page in the API Insights workspace provides machine learning-generated recommendations for API clustering.

![AProposed API clustering tab to view machine learning-generated recommendations for API clustering](../image/api-insights-cluster.png "Proposed API clustering tab")

## Accessing the Proposed API clustering tab

To access the Proposed API clustering tab, navigate to **Workspaces** &gt; **API Insights**. On the **Overview** tab, select the count metric in the API clustering recommendations section. The **Proposed API clustering** tab is displayed on the Data recommendations page.

You need the following roles to access the API clustering recommendations section: sn\_cmdb\_admin, ml\_report\_user, and platform\_ml\_read.

## Viewing data

By default, the page displays the following data:

-   **Cluster Concept**

    Displays the API components that the machine learning model has grouped together based on similarities. These concepts represent the core idea or functionality that defines each cluster.

-   **Cluster size**

    Indicates the total number of components within the cluster. A larger size suggests that many components are related and grouped together under the same API concept.

-   **Cluster Quality**

    Reflects the confidence or strength of the relationship between components in the cluster, measured on a scale from `0` to `100`. A higher quality value implies stronger relationships among the API components within the cluster.

-   **Updated**

    Displays the most recent timestamp when the cluster was updated, enabling tracking the recency of the machine learning recommendations and any changes to the clusters.


