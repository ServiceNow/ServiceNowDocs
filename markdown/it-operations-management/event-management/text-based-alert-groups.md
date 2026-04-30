---
title: Text-based alert grouping
description: In text-based alert grouping, the EM Alert Clustering Solution forms clusters based on the Description, Metric name, and Configuration item.Class fields. Using this solution, text-based groups are created. When a new alert arrives, the ML Predictor determines which cluster it belongs to, and alerts in the same cluster form a group.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Text-based alert grouping

In text-based alert grouping, the EM Alert Clustering Solution forms clusters based on the Description, Metric name, and Configuration item.Class fields. Using this solution, text-based groups are created. When a new alert arrives, the ML Predictor determines which cluster it belongs to, and alerts in the same cluster form a group.

The ML Predictor job is asynchronous and assigns real-time alerts to clusters. There may be slight delays in receiving the predictor's results, causing the creation of text-based groups to be delayed by several minutes, as the alert grouping job runs once per minute. If the prediction results are not ready during the current run, it will recheck during the next run of the grouping job.

For text-based logic to execute, you must have the Predictive Intelligence plugin installed and the EM Alert Clustering Solution definition is activated. Text-based thresholds are:

-   Cluster quality threshold: **sa\_analytics.alert\_grouping\_tb\_cluster\_quality\_threshold**, default is 70.
-   Alert rank threshold: **sa\_analytics.alert\_grouping\_tb\_alert\_rank\_threshold**, default is 0.3 \(smaller values are better\).

**Note:** To use these properties, you need to create properties with the same names and assign the required values to them. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

The EM Alert Clustering Solution definition is located in the ml\_capability\_definition\_clustering table. To access it, navigate to **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

To verify if the solution definition is active, see [Verify text-based clustering solution](../task/NLP-alerts.md).

**Note:** To disable the EM Alert Clustering Solution definition, disable text-based alert grouping by setting the property **sa\_analytics.text\_based\_group\_enabled** to `false` and clearing the **Active** check box in the EM Alert Clustering Solution definition.

