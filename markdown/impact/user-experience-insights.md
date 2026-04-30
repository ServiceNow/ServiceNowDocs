---
title: User Experience
description: Explore real-time user monitoring to analyze user experience and performance insights in Instance Observer​ telemetry into node, transaction type, URL, and user level breakdowns for Impact Total customers.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analytics, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# User Experience

Explore real-time user monitoring to analyze user experience and performance insights in Instance Observer​ telemetry into node, transaction type, URL, and user level breakdowns for Impact Total customers.

-   Access the [User Experience](user-experience-insights.md) to visualize quickly your user base issues based on transaction type and volume, outage or service degradations, and access the specific affected URL​ for Impact Total customers.
-   Search for a specific URL that is causing increases in transaction response time.​
-   Analyze node and transaction type level data for outliers and trending​ transactions.
-   Identify which users are impacted by an outage or service degradation.​
-   Quickly visualize your user base based on transaction volume.​
-   Monitor your applications for performance issues and track the cause of performance issues.

The overview page breaks down user history and transaction count into various widgets and charts into a dashboard view.

![Overview page with populated chart data for the selected instance and timeframe.](../image/io-ux-overview.png)

<table id="table_ut1_5ff_bbc"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   Transaction count
-   Transaction response time
-   Unique user count
-   Max response time

</td><td>

Displays the current value, a percentage of decrease or increase in historical trend, and a visual graph of the activity.

</td></tr><tr><td>

Top 100 most active users

</td><td>

-   Hover on a user block to see an encrypted user ID and the number of transaction reports for that time period.
    -   Green blocks represent users without a threshold warning
    -   Red blocks indicate a transaction volume that surpasses the general threshold.
-   Select a user block to view the details of the entry.

 **Note:** The user ID is anonymized. Administrators have the capability to opt-in to the collection of non-anonymized data.

</td></tr><tr><td>

Node performance by response time

</td><td>

-   Hover on a tile to see the node name and the response time for that node.
    -   Green blocks represent nodes with average response times.
    -   Red blocks indicate increased response time outside of average parameters for the node.
-   Select a node block to view the details of the entry.

</td></tr><tr><td>

Application performance by response time

</td><td>

Track applications that have performance issues by using the average response time metric.The metrics are:

-   Total transaction processing time
-   Total semaphore wait time
-   Total UI time \(Average response time\)
-   Network latency
-   Content download time

For more information, see [Track the response time of applications to monitor their performance](../task/monitor-apps-user-experience-io.md).

</td></tr><tr><td>

Node transaction count

</td><td>

Select a point on the graph to view additional actions and drill into the transaction details.

</td></tr><tr><td>

Node response time

</td><td>

Select a point on the graph to view additional actions and drill into the transaction details.

</td></tr></tbody>
</table>**Note:** User Experience in Instance Observer may not be available to customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected datacenters, to self-hosted customers, or in other restricted environments, or to managed service providers.

