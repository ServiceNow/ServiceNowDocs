---
title: MID Server resource threshold alerts
description: The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server resource threshold alerts

The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.

The MID Server Issue \[ecc\_agent\_issue\] table warns users when a MID Server exceeds configured thresholds of its allocated CPU and memory resources. These warnings are published before the MID Server experiences performance degradation or an out-of-memory error, enabling the administrator to increase resources and avoid downtime. Administrators can use a registered event to send email notification to selected recipients, advising them of any threshold breaches, or to create a custom script to do some other type of work. The instance continues to update the MID Server Issue \[ecc\_agent\_issue\] table to keep unresolved issues current.

By default, CPU and memory threshold alerts are disabled and no alerts are published to the MID Server Issue \[ecc\_agent\_issue\] table. To enable both types of alerting, add these properties to the System Property \[sys\_properties\] table, and then set their values to **true**:

-   **mid.threshold.resource.breach.enable.cpu.alerts**
-   **mid.threshold.resource.breach.enable.memory.alerts**

For details on adding system properties to the platform, see [Add a property using sys\_properties.list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

## Evaluation process

This processing occurs whether or not alerting is enabled:

1.  Every 10 minutes, each MID Server transmits its CPU and memory consumption metrics to the instance. The instance inserts CPU metrics into the **Mean CPU used %** field of the ECC Agent Scalar Metrics \[ecc\_agent\_scalar\_metric\] table and memory metrics into the **Max memory used %** field of the ECC Agent Memory Metrics \[ecc\_agent\_memory\_metric\] table.
2.  After a successful insert, the following business rules run on each table, invoking a script include that calls an appropriate function. Each function takes an average of the metric sets inserted into the tables, based on the configured sampling intervals.

    -   **Update cpu mean on MID Server Status**: Calls the MIDResourceThresholdBreach.checkCpuUsage\(\) script include.
    -   **Update max memory on MID Server Status**: Calls the MIDResourceThresholdBreach.checkMemoryUsage script include.
    Each function takes an average of the metric sets inserted into the tables, based on the configured thresholds and sampling intervals. The instance first looks at each MID Server for configuration parameters that set custom threshold values or sampling intervals for that MID Server. If no configuration parameters for these attributes are found, the instance looks in the System Properties \[sys\_properties\] table for custom values to use. If no properties are found, the instance uses the default threshold and interval values from the code.

    **Note:** Both the threshold percentages and the sampling intervals are configurable. See [Configuring thresholds and sampling intervals](mid-resource-threshold-alerts.md#sec_config-threshold-and-intervals) for details.


## Alerting process

When alerting for CPU or memory thresholds is enabled, this processing occurs:

1.  If the aggregated average metric value equals or exceeds the configured percent threshold, the instance triggers the **mid.threshold.resource.breach** event. Administrators can use this event to create [email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md) for threshold breach alerts or to create a custom script.
2.  The instance inserts a record of the breach into the MID Server Issue \[ecc\_agent\_issue\] table with a **State** value of **New** and a **Count** of 1, and then publishes a message containing all the pertinent details of the breach. An example of this message is `Mean CPU used % has exceeded threshold (96>=91) for a 40 minute interval span, occurring after start date 2017-01-11 14:25:19`. This message appears in the **Short description** field of the MID Server Issue form and in the event. You can copy any part of the message into your email notifications.

## MID Server issue states

When the administrator first examines an issue in the MID Server Issue \[ecc\_agent\_issue\] table, the administrator can change the **State** of the issue to **Acknowledged** to indicate that the issue is being addressed. Each time the instance detects a breach, it attempts to match the breach with an existing issue. If a MID Server already has an issue record for that breach in a **State** of **New** or **Acknowledged**, the instance updates the **Last Detected** field with the current date/time and increments the **Count** field in the existing record. This prevents the creation of duplicate records in the MID Server Issue \[ecc\_agent\_issue\] table and records the number of times after the initial incident that the breach reoccurred. The administrator can increase MID Server resources gradually and watch the effect on the **Count** field. When the counter stops incrementing, the administrator knows that the MID Server has adequate resources. When the MID Server resource have been adjusted appropriately, the administrator sets the **State** to **Resolved**. If a new threshold breach is logged that matches a MID Server issue with a **State** of **Resolved**, the instance creates a new issue record.

**Note:** Any record in the MID Server Issue \[ecc\_agent\_issue\] table that has not been updated in 30 days is deleted, regardless of its state.

## Recommendations for resolving resource issues

Administrators have the opportunity to resolve any resource issues with a MID Server when they receive notification of the event. Follow these recommendations for reducing the strain on MID Server resources:

-   **JVM memory**:
    -   Allocate more max memory to the MID Server. For more information, see [Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md).
    -   Add additional MID Servers to share the workload. For more information, see [MID Server clusters](../task/t_ConfigureAMIDServerCluster.md#).
    -   Reduce the amount of concurrent processing for the MID Server. This includes segmenting IP Address ranges into smaller segments for a Discovery schedule or loading smaller segments of data within an import job.
-   **CPU**: Reduce the activity on the host or migrate the MID Server to a new host with more available resources.

    **Note:** MID Server can create a resource usage spike during Discovery, especially discovering against a large number of targets or executing multiple Power Shell sessions concurrently. The MID Server host’s resource utilization automatically returns to normal after the Discovery execution successfully stops. To decrease CPU utilization, host the MID Server on a dedicated machine. If you encounter resource usage issues, make sure only one MID Server is run on each dedicated host machine. If the MID Server is hosted on a public cloud, add more CPU resources and avoid the noisy neighbor issue. For more information, see [High CPU Usage on Host with MID Server\(s\) \[KB0597639\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597639).


## Tables used for resource threshold evaluation

<table id="table_qbq_4th_qy"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID Server Issue \[ecc\_agent\_issue\]

</td><td>

Stores data on various types of MID Server issues, including breaches of configured CPU and memory thresholds. Fields used for resource threshold breaches are:-   **count**: Number of times a previously reported threshold breach occurs, if the event is not marked **Resolved**.
-   **last\_detected**: Current date and time a threshold breach is detected. This field is updated each time a previously detected breach is found, if it is not marked **Resolved**.
-   **message**: Descriptive message summarizing the conditions that triggered the threshold breach event. This message includes the actual percentage of CPU and memory calculated and the configured thresholds that were breached.
-   **mid\_server**: Name of the MID Server experiencing the resource threshold breach.
-   **source**: The issue source for the breach. These are the possible sources:
    -   **CpuMIDResourceThresholdBreach**: CPU threshold issue sources.
    -   **MemoryMIDResourceThresholdBreach**: Memory threshold issue sources.

</td></tr><tr><td>

MID Server Status \[ecc\_agent\_status\]

</td><td>

Stores the percentages used for the CPU and memory resources, averaged over configurable intervals for each resource. The fields used are:-   Mean CPU used %
-   Max Memory used %

</td></tr><tr><td>

ECC Agent Scalar Metric \[ecc\_agent\_scalar\_metric\]

</td><td>

Stores the CPU usage data inserted by each MID Server every 10 minutes. The table field used by resource threshold alerting is **mean**.

</td></tr><tr><td>

ECC Agent Memory Metric \[ecc\_agent\_memory\_metric\]

</td><td>

Stores the memory usage data inserted by each MID Server every 10 minutes. The table field used by resource threshold alerting is **max\_used\_pct**.

</td></tr></tbody>
</table>## Business rules that check for threshold breaches

|Business rule|Description|
|-------------|-----------|
|Update cpu mean on MID Server Status|Runs after the MID Server inserts a record into the ECC Agent Scalar Metric \[ecc\_agent\_scalar\_metric\] table. This business rule triggers the MIDResourceThresholdBreach script include function that evaluates threshold settings to determine if the MID Server has breached its configured CPU resource thresholds.|
|Update max memory on MID Server Status|Runs after the MID Server inserts a record into the ECC Agent Memory Metric \[ecc\_agent\_memory\_metric\] table. This business rule triggers the MIDResourceThresholdBreach script include function that evaluates threshold settings to determine if the MID Server has breached its configured memory resource thresholds.|

## Configuring thresholds and sampling intervals

You can use the default threshold percentages and sampling intervals or configure custom values using either of these methods:

-   [Add system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) to the instance and change the default values for all MID Servers.
-   Add [configuration parameters](mid-server-parameters.md#) to change the default resource values for individual MID Servers.

The system properties and the configuration parameters use the same names.

<table id="table_eyy_vh3_qy"><thead><tr><th>

Property/configuration parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.threshold.mean\_cpu.aggregate\_interval\_span

</td><td>

Number of 10 minute units in the interval for sampling CPU usage data. The default interval is 30 minutes \(3 x 10 min.\)**Default**: 3

</td></tr><tr><td>

mid.threshold.mean\_cpu.percent

</td><td>

Usage percentage of the total CPU resources that initiates a threshold breach alert. **Default**: 95

</td></tr><tr><td>

mid.threshold.mean\_max\_memory.aggregate\_interval\_span

</td><td>

Number of 10 minute units in the interval for sampling memory usage data. The default interval is 30 minutes \(3 x 10 min.\)**Default**: 3

</td></tr><tr><td>

mid.threshold.mean\_max\_memory.percent

</td><td>

Usage percentage of the total memory resources that initiates a threshold breach alert. **Default**: 95

</td></tr></tbody>
</table>## MID Server resource reporting

The [MID Server dashboard](../concept/c_MIDServerDashboard.md) contains two reports that give you views into the consumption of CPU and JVM memory resources. These reports show usage over the previous 30 days.

-   **Avg Percentage of CPU Used**: Trending the daily average on CPU usage helps illustrate the amount of CPU processing that the MID Server host consumes. MID Servers deployed on the same host will report the same CPU usage.
-   **Avg Percentage of Max Memory Used**: The maximum used percentage \(**max\_used\_pct**\) is a useful metric for determining if the MID Server has enough memory resources. This metric is a percentage of the max used memory over the total available memory. Trending this over time provides a visualization of how much memory is needed by the MID Server.

**Parent Topic:**[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

