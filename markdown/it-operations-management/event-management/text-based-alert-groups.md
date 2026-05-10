---
title: Text-based alert grouping
description: In text-based alert grouping, alerts are organized and correlated based on specific text patterns or keywords within the alert content. This approach dynamically groups alerts that share similar textual characteristics, such as error messages or event descriptions, allowing for more flexible and adaptive management of alerts.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Text-based alert grouping

In text-based alert grouping, alerts are organized and correlated based on specific text patterns or keywords within the alert content. This approach dynamically groups alerts that share similar textual characteristics, such as error messages or event descriptions, allowing for more flexible and adaptive management of alerts.

The EM Alert Clustering Solution is a method used to correlate alerts based on similarities in specific fields and form clusters or groups. In ServiceNow Event Management, it creates clusters based on the Description, Metric name, and Configuration item.Class fields. This solution organizes alerts into text-based groups, and when a new alert arrives, the ML Predictor identifies the appropriate cluster, grouping alerts within the same cluster.

**Note:** The ML Predictor job is asynchronous and assigns real-time alerts to clusters, which may result in slight delays. This delay can cause text-based groups to be created several minutes later, as the alert grouping job runs once per minute. If prediction results are not available during a run, they are rechecked in the next grouping job.

For text-based logic to execute, you must have the Predictive Intelligence plugin \(com.glide.platform\_ml\) installed and the EM Alert Clustering Solution definition activated.

There are specific settings or limits used to control the behavior of text-based alert grouping. These thresholds define the criteria for how alerts are grouped based on text patterns or attributes. The text-based thresholds are:

-   Cluster quality threshold: The Cluster quality threshold \(**sa\_analytics.alert\_grouping\_tb\_cluster\_quality\_threshold**\) determines the minimum quality required for an alert cluster to be considered valid. This threshold ensures that only clusters with a minimum level of similarity and reliability are used. Clusters that meet this threshold are considered valid, improving the precision of the groupings and reducing noise from irrelevant or low-quality clusters. The range of the threshold is from 1 to 100 and the default value is 70.
-   Alert rank threshold: The Alert rank threshold \(**sa\_analytics.alert\_grouping\_tb\_alert\_rank\_threshold**\) defines the minimum rank required for an alert to be included in a group. This threshold ensures that only alerts with a certain level of similarity are grouped together, filtering out lower-ranked alerts to maintain the quality of the alert group. The default value is 0.3, where smaller values indicate better similarity.

**Note:** To use these properties, you need to create properties with the same names and assign the required values to them. For more information on how to create a property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

The EM Alert Clustering Solution definition is located in the \[ml\_capability\_definition\_clustering\] table. To access it, navigate to **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

To verify if the solution definition is active, see [Verify text-based clustering solution](../task/NLP-alerts.md). To disable the EM Alert Clustering Solution definition, disable text-based alert grouping by setting the property **sa\_analytics.text\_based\_group\_enabled** to `false` and clearing the **Active** check box in the EM Alert Clustering Solution definition.

## Example of text-based alert grouping

<table id="table_ncc_lw3_ncc"><thead><tr><th>

Scenario

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Network Connectivity Problems: There are widespread network connectivity issues affecting multiple departments.

</td><td>

Alerts from various network monitoring tools might report issues like Network segment down, High packet loss, or Connectivity issues in subnet. Text-based alert grouping uses the EM Alert Clustering Solution and ML Predictor to streamline alert management. The EM Alert Clustering Solution employs Natural Language Processing \(NLP\) algorithms to analyze and identify common text patterns in alerts such as Network segment down or High packet loss. It then clusters these alerts based on their text similarity, grouping related issues together. The ML Predictor further enhances this process by evaluating new alerts in real time and assigning them to the appropriate existing clusters based on their text patterns.

 This dynamic grouping provides a consolidated view of the connectivity problems, allowing network engineers to quickly diagnose and address the root cause of the issues more efficiently.

</td></tr></tbody>
</table>