---
title: Components installed with Metric Intelligence
description: Several types of components are installed with activation of the Metric Intelligence \(com.snc.sa.metric\) plugin, including tables, scheduled jobs, and properties.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Components installed with Metric Intelligence

Several types of components are installed with activation of the Metric Intelligence \(com.snc.sa.metric\) plugin, including tables, scheduled jobs, and properties.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Scheduled jobs installed

<table id="table_edf_dw2_xs"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric Intelligence — Metric Learner job

</td><td>

Runs daily and builds the statistical models used for anomaly detection.

</td></tr><tr><td>

Metric Intelligence — Purge old metric schemas and anomaly scores

</td><td>

Cleans up the **sa\_metric\_anomaly\_score** and the **sa\_metric\_schema\_definition** tables.

</td></tr><tr><td>

Metric Intelligence — Sync metric schema to mid

</td><td>

Synchronizing data from the instance to the MID Server in the metric schema table **sa\_metric\_schema\_definition**.

</td></tr><tr><td>

Metric Intelligence — Sync tables with mid

</td><td>

Synchronizing data from the instance to the MID Server in tables.

</td></tr><tr><td>

Metric Intelligence — Table cleanup

</td><td>

Cleaning up tables related to various deletion operations.

</td></tr><tr><td>

Metric Intelligence — Observation Interval Learner job

</td><td>

Calculates the observation interval using collected data points for all data series.

</td></tr><tr><td>

Metric Intelligence — Process Stale Anomaly Score – Daily

</td><td>

Daily job that cleans stale anomaly scores, for a specified window of time, in the Metric Anomaly Score \[sa\_metric\_anomaly\_score\] table. Uses the properties **sa\_metric.anomaly\_score\_stale\_interval\_in\_days** and **sa\_metric.anomaly\_score\_next\_stale\_interval\_in\_days** to calculate the window of time for cleaning.

</td></tr><tr><td>

Metric Intelligence — Sync CI Anomaly Scores

</td><td>

Keeps anomaly scores up to date with any deletion of metrics.

</td></tr><tr><td>

Metric Intelligence — Metric configuration job

</td><td>

Synchronizes metric configurations from the instance to all Metric Intelligence MID Servers.

</td></tr><tr><td>

Metric Intelligence — Local level kalman filter model learner job

</td><td>

Builds local level kalman filter models on which to run change detection.

</td></tr><tr><td>

Metric Intelligence — Anomaly Model Test

</td><td>

On-demand scheduled job which runs when user clicks **Run Anomaly Test**.

</td></tr><tr><td>

Metric Intelligence — Validate MID Distributed cluster

</td><td>

1.  Checks the status of the cluster node.

If status is **Started** and the status of the Metric Intelligence extension is not any of **Started**/**Starting**/**Warning** \[warning with specific errors\], then the job changes the status of the cluster node to **Stopped**.

This happens when MID Server stops unexpectedly without notifying the instance that it is stopping.

2.  Checks the status of all cluster nodes on all MID Servers in the cluster.
    -   If the status of all nodes is **Stopped** and the status of the cluster itself is **Started**, then the job changes the status of the cluster to **Stopped**.
    -   If the status of the cluster is **Stopped** but there are MID Servers with a cluster node that is running, then the job changes the status of the cluster to **Started**.
3.  Checks the number of Cluster Leaders: If two are detected, then the job stops the entire cluster.

This happens when MID Servers are not able to connect with other members of the cluster and form multiple sub-clusters.


</td></tr><tr><td>

Event Management - process metric binding events \[1000-1020\]

</td><td>

Process Metric Intelligence metric binding events separately from Event Management events \(bucket range 1000-1020\).

</td></tr><tr><td>

Event Management - process metric binding events \[1020-1040\]

</td><td>

Process Metric Intelligence metric binding events separately from Event Management events \(bucket range 1020-1040\).

</td></tr><tr><td>

Event Management - process metric binding events \[1040-1060\]

</td><td>

Process Metric Intelligence metric binding events separately from Event Management events \(bucket range 1040-1060\).

</td></tr><tr><td>

Event Management - process metric binding events \[1060-1080\]

</td><td>

Process Metric Intelligence metric binding events separately from Event Management events \(bucket range 1060-1080\).

</td></tr><tr><td>

Event Management - process metric binding events \[1080-1100\]

</td><td>

Process Metric Intelligence metric binding events separately from Event Management events \(bucket range 1080-1100\).

</td></tr><tr><td>

Metric Intelligence - Stationary nonparametric model learner job

</td><td>

Learns the stationary nonparametric model.

</td></tr><tr><td>

Metric Intelligence - Combined Model Learner Job

</td><td>

Constructs all the information required for performing real time anomaly detection \(calculating data frequency and building statistical models\) on a subset of all series for which data is being collected.

</td></tr></tbody>
</table>## Tables installed

<table id="table_aqf_gwm_zw"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric Time Series Model\[sa\_time\_series\]

</td><td>

Statistical models built for metric data.

</td></tr><tr><td>

Alert Anomaly\[em\_alert\_anomaly\]

</td><td>

Anomaly alerts that were created from anomaly events that were sent by Metric Intelligence so users can review. Anomaly alerts are kept separately from regular system alerts.

</td></tr><tr><td>

Metric Anomaly Score\[sa\_metric\_anomaly\_score\]

</td><td>

Stores anomaly scores for the metric.

</td></tr><tr><td>

Metric To CI Mapping Deleted SysIds\[sa\_metric\_map\_deleted\]

</td><td>

SysIds of deleted metric-to-CI mapping records.

</td></tr><tr><td>

Metric To CI Mapping\[sa\_metric\_map\]

</td><td>

Mappings currently in effect of metric types to CIs.

</td></tr><tr><td>

SA Metric Type Registration\[sa\_metric\_registration\]

</td><td>

Details about metric type registration.

</td></tr><tr><td>

Metric Type Registration Deleted SysIds\[sa\_metric\_registration\_deleted\]

</td><td>

SysIds of records that were deleted from the SA Metric Type Registration \[sa\_metric\_registration\] table.

</td></tr><tr><td>

Metric Schema Definition\[sa\_metric\_schema\_definition\]

</td><td>

Map of metrics being received based on CI class. It is used to optimize the metric data payload being sent from the MID Server to the instance.

</td></tr><tr><td>

Metric Type\[sa\_metric\_type\]

</td><td>

Metric type source.

</td></tr><tr><td>

Monitoring System Metric Type Deleted SysIds\[sa\_source\_metric\_type\_deleted\]

</td><td>

SysIds of deleted monitoring system metrics.

</td></tr><tr><td>

Monitoring System Metric Type\[sa\_source\_metric\_type\]

</td><td>

Metric types per CI class, active/inactive status, and metric source.

</td></tr><tr><td>

Metric Settings\[sa\_metric\_config\_setting\]

</td><td>

Default configuration settings for Metric Intelligence MID Servers.

</td></tr><tr><td>

Metric Configuration Rules\[sa\_metric\_config\_rule\]

</td><td>

Rules to override configuration settings for MID Servers.

</td></tr><tr><td>

Metric overridden configurations\[sa\_metric\_config\_rule\_setting\]

</td><td>

Maps overridden configurations to custom defined rules.

</td></tr><tr><td>

Metric Staged Configurations\[sa\_metric\_config\_staging\]

</td><td>

Saved encoded configurations for the MID Servers.

</td></tr><tr><td>

Metric learned parameters\[sa\_metric\_learned\_param\]

</td><td>

Parameters learned for CI/metric combinations, that will be synced to the MID Servers.

</td></tr><tr><td>

Metric To CI Mapping Deleted Details\[sa\_metric\_map\_deleted\_detail\]

</td><td>

Details about deleted entries from metric to CI mapping table. Includes CI, metric, and SysId of the deleted entry in the Metric To CI Mappings \[sa\_metric\_map\] table.

</td></tr><tr><td>

Track unique CIs created in metric map\[sa\_metric\_ci\_tracker\]

</td><td>

All unique CIs for which metric map entry was created.

</td></tr><tr><td>

Metric Class\[sa\_metric\_class\]

</td><td>

Metric classes that can be associated with specific metrics to override bounds and widths learned values.

</td></tr><tr><td>

Metric Change Score\[sa\_metric\_change\_score\]

</td><td>

Change events information.

</td></tr><tr><td>

Anomaly Test Rules\[sa\_metric\_anomaly\_test\_rule\]

</td><td>

Anomaly test rules used for anomaly model testing.

</td></tr><tr><td>

Anomaly test results\[sa\_metric\_anomaly\_test\_result\]

</td><td>

Results from anomaly model testing, such as bounds and anomaly scores.

</td></tr><tr><td>

Metric anomaly test config customized parameters\[sa\_metric\_anomaly\_test\_config\_custom\_param\]

</td><td>

Customized parameters for selected series in anomaly model testing.

</td></tr><tr><td>

Metric Intelligence Properties\[sa\_metric\_property\]

</td><td>

Metric Intelligence properties by domain.

</td></tr><tr><td>

Track host name with metric CI\[sa\_metric\_ci\_host\]

</td><td>

CIs that are bind with node name from the binding event.

</td></tr><tr><td>

Functions supported by metric expression language\[sa\_metric\_expr\_function\]

</td><td>

Functions supported by metric expression language.

</td></tr><tr><td>

Argument types for functions supported by metric expression language\[sa\_metric\_expr\_func\_arg\]

</td><td>

Argument types for functions supported by metric expression language.

</td></tr><tr><td>

Track CI Types to metric entries valid for different sources\[sa\_metric\_ci\_type\_map\]

</td><td>

Track CI Types to metric entries that are valid for different sources.

</td></tr><tr><td>

CI Type To Resource Class\[sa\_ci\_type\_to\_resource\_class\]

</td><td>

Contains mappings of CI type to resource class. Used for resource binding during resource lookups given a CI and a **resource\_path** in the event.

 The \[sa\_ci\_type\_to\_resource\_class\] table contains some default mapping records, and the evt\_mgmt\_admin role is required to manage this table.

</td></tr><tr><td>

CI Resource \[ci\_resource\]

</td><td>

Parent table used for resource binding.

</td></tr><tr><td>

CI Resource Hardware\[ci\_resource\_hardware\]

</td><td>

An extension of the CI Resource \[ci\_resource\] table, used for resource binding.

</td></tr><tr><td>

CI Resource Application\[ci\_resource\_appl\]

</td><td>

An extension of the CI Resource \[ci\_resource\] table, used for resource binding.

</td></tr><tr><td>

CI Resource Service\[ci\_resource\_service\]

</td><td>

An extension of the CI Resource \[ci\_resource\] table, used for resource binding.

</td></tr><tr><td>

CI Resource VM\[ci\_resource\_vm\_object\]

</td><td>

An extension of the CI Resource \[ci\_resource\] table, used for resource binding.

</td></tr><tr><td>

CI Resource Database\[ci\_resource\_database\]

</td><td>

An extension of the CI Resource \[ci\_resource\] table, used for resource binding.

</td></tr><tr><td>

Series Event History \[sa\_series\_event\_history\]

</td><td>

Information about CIs start and end maintenance mode. Metric Intelligence stores historical information about the times CIs enter and exit maintenance mode if the system property sa.model\_learner.maint\_event\_record\_history\_enabled is set to true \(default\). And if the system property sa\_metric.maint\_exclusion is also set to true \(default\), metrics from CIs that are in maintenance mode are excluded from model learning.

</td></tr><tr><td>

Metric Dashboard Metadata\[sa\_metric\_dashboard\_metadata\]

</td><td>

Chart configurations per CI class, for the metrics that are displayed for a CI associated with an alert, in Agent Workspace.

</td></tr><tr><td>

Metric Config Anomaly Detection Staging\[sa\_metric\_config\_anomaly\_detection\_staging\]

</td><td>

Internal table that is used to help calculate the action level for each entry in the Metric to CI Mapping \[sa\_metric\_map\] table.

</td></tr></tbody>
</table>## Properties installed

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter. To open the Metric Settings \[sa\_metric\_config\_setting\] table, enter `sa_metric_config_setting.list` in the navigation filter.

<table id="table_g4d_wn2_xs"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

sa.metric.map.with.ci.expiration.sec

</td><td>

Length of time \(in seconds\) that records for mapping of raw data to CIs remains in effect if the mapping to CI is found.-   **Type**: numeric
-   **Default value**: 432000
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Metric Intelligence](../../agent-client-collector/concept/operational-metrics.md)

</td></tr><tr><td>

sa.metric.map.without.ci.expiration.sec

</td><td>

Length of time \(in seconds\) that records for mapping of raw data to CIs remains in effect if the mapping to CI is not found.-   **Type**: numeric
-   **Default value**: 86400
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Metric Intelligence](../../agent-client-collector/concept/operational-metrics.md)

</td></tr><tr><td>

sa\_metric.anomaly\_score\_stale\_interval\_in\_days

</td><td>

The starting day of the window of time that the **Operational Metrics – Process Stale Anomaly Score – Daily** scheduled job uses when checking staleness status of anomaly score.

 The window of time spans from today, until the past number of days specified in this property.

 -   **Type**: numeric
-   **Default value**: 3
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa\_metric.anomaly\_score\_next\_stale\_interval\_in\_days

</td><td>

Number of days by which to extend the window of time used by the **Operational Metrics – Process Stale Anomaly Score – Daily** scheduled job. Applies if the job runs, but fails to return any data using the window of time specified by the **sa\_metric.anomaly\_score\_stale\_interval\_in\_days** property.

 -   **Type**: numeric
-   **Default value**: 7
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

max\_records\_per\_rest\_request

</td><td>

Maximum number of records to download from the instance to the MID Server in each synchronization cycle.This property is for internal use.

 -   **Type**: integer
-   **Default value**: 10000
-   **Other possible values**:
    -   **Minimum value**: 1000
    -   **Maximum value**: 20000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

normalized\_metric\_max\_queue\_size

</td><td>

Size of metrics queue. Anomaly detector reads through this queue and determines for each metric whether it is anomalous. This property is for internal use.

 -   **Type**: integer
-   **Default value**: 3000000
-   **Other possible values**:
    -   **Minimum value**: 1000000
    -   **Maximum value**: 5000000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

normalized\_metric\_queue\_consumer\_count

</td><td>

Number of threads that concurrently perform anomaly detection.This property is for internal use.

 -   **Type**: integer
-   **Default value**: 12
-   **Other possible values**:
    -   **Minimum value**: 8
    -   **Maximum value**: 16
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

ignite\_data\_streamer\_thread\_count

</td><td>

Number of threads that data streamers use to write data to the cache. The data streamer creates batches from individual data entries and adds these batches to the cache.

 This property is for internal use.

 -   **Type**: integer
-   **Default value**: 8
-   **Other possible values**:
    -   **Minimum value**: 8
    -   **Maximum value**: 32
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

ignite\_data\_streamer\_flush\_frequency

</td><td>

Frequency of automatic flush of data streamers.The data streamer creates batches from individual data entries and adds these batches to the cache.

 This property is for internal use.

 -   **Type**: integer
-   **Default value**: 1000
-   **Other possible values**:
    -   **Minimum value**: 0
    -   **Maximum value**: 30000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

ignite\_data\_streamer\_buffer\_size

</td><td>

Buffer size of data streamers.The data streamer creates batches from individual data entries and adds these batches to the cache.

 This property is for internal use.

 -   **Type**: integer
-   **Default value**: 102400
-   **Other possible values**:
    -   **Minimum value**: 1024
    -   **Maximum value**: 1024000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

ignite\_data\_streamer\_batch\_size

</td><td>

Size of the batch that is added to a data streamer.The data streamer creates batches from individual data entries and adds these batches to the cache.

 This property is for internal use.

 -   **Type**: integer
-   **Default value**: 5000
-   **Other possible values**:
    -   **Minimum value**: 1
    -   **Maximum value**: 10000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

ignite\_data\_streamer\_batch\_flush\_frequency

</td><td>

Frequency of automatic flush of internal batching before adding data to data streamers.The data streamer creates batches from individual data entries and adds these batches to the cache.

 This property is for internal use.

 -   **Type**: integer
-   **Default value**: 5000
-   **Other possible values**:
    -   **Minimum value**: 1000
    -   **Maximum value**: 30000
-   **Location**: Metric Settings \[sa\_metric\_config\_setting\] table.

</td></tr><tr><td>

sa.metric.use.resource.binding

</td><td>

Enables resource binding.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Metric binding to resources](../concept/resource-binding.md)

</td></tr><tr><td>

sa.metric.display.mid.setup.action

</td><td>

Displays the **Setup Metric Intelligence** related link on the MID Server form, for a MID Server that has been validated and that is running.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [MID Server and MID Server distributed cluster for Metric Intelligence](../concept/ops-intelligence-mid-server.md)

</td></tr><tr><td>

sa.model\_learner.maint\_event\_record\_history\_enabled

</td><td>

Stores historical information about CIs start and end maintenance mode, in the Series Event History \[sa\_series\_event\_history\] table.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Understanding Metric Intelligence](../concept/operational-intelligence-overview.md)

</td></tr><tr><td>

sa\_metric.maint\_exclusion

</td><td>

Excludes metrics for CIs that are in maintenance mode, from model learning.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Understanding Metric Intelligence](../concept/operational-intelligence-overview.md)

</td></tr><tr><td>

sa.model\_learner.maint\_history\_batch\_size

</td><td>

Determines the number of data series per batch when storing information about CIs start and end maintenance mode, in the Series Event History \[sa\_series\_event\_history\] table.

 Adjust the setting of this property if there are related performance issues.

 -   **Type**: integer
-   **Default value**: 1000
-   **Location**: System Property \[sys\_properties\] table
-   **Learn more**: [Understanding Metric Intelligence](../concept/operational-intelligence-overview.md)

</td></tr><tr><td>

sa\_metric.scheduled\_jobs\_to\_monitor\_sys\_id\_list

</td><td>

Contains the sys\_ids of the 3 scheduled jobs that self-health monitoring for Metric Intelligence monitors: -   Metric Intelligence — Metric configuration job
-   Metric Intelligence — Sync tables with mid
-   Metric Intelligence — Validate MID Distributed cluster

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](../../agent-client-collector/reference/acc-monitoring-reference.md)

