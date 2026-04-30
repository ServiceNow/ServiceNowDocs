---
title: View metric to CI and resource binding
description: View the metric to CI and resource binding results, including details for failed bindings which you can use to mitigate the failure. If Metric Intelligence cannot map and bind a metric to a CI or to a resource, then that CI or resource is not included in anomaly detection until it is properly mapped.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Get started with Metric Intelligence, Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# View metric to CI and resource binding

View the metric to CI and resource binding results, including details for failed bindings which you can use to mitigate the failure. If Metric Intelligence cannot map and bind a metric to a CI or to a resource, then that CI or resource is not included in anomaly detection until it is properly mapped.

## Before you begin

Role required: evt\_mgmt\_admin

If [resource binding](../concept/resource-binding.md) is not enabled, then no resource binding results appear.

## About this task

Metric Intelligence uses event rules to map metric data with the specific CI or resource that is associated with the metric event. The results of these mappings are stored in the Metric to CI Mappings \[sa\_metric\_map\] table. If mapping fails, then the binding status for the metric indicates the general reason for the failure and further details about the failure are provided. Examine the details for a mapping failure and mitigate the problem to improve accurate and effective metric data processing.

-   If mapping to a CI is successful, then the mapped CI appears in the **Configuration Item** column. If resource binding was attempted but failed, then the mapped CI does not appear, even if the mapping to a CI was successful. Missing or duplicate CIs can cause CI mapping to fail.
-   If mapping to a resource is successful, then the mapped resource appears in the **Resource** column. Missing a resource table that is mapped to the CI type to which the event is bound, or a missing **resource\_path** attribute in the event, cause resource binding to fail.

Records in the CI Mappings \[sa\_metric\_map\] table remain in effect for 24 hours \(by default, if mapping to the CI is not successful\), or for 5 days \(by default, if mapping to the CI is successful\). Later, if within that time period raw data arrives for a metric/CI pair that already has a record, the existing mapping is used to match the data to an existing CI. After Metric to CI Mappings records expire, incoming new raw data requires remapping. These records expire when:

-   The 24-hour or 5-day cycle ends.
-   An event rule has changed — Triggering an immediate expiration of the respective mapping record.

Adjusting mappings to reflect the addition or removal of CIs by Discovery, takes effect only upon the beginning of the next cycle.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Anomaly Detection** &gt; **Metric to CI**.

    The **Metrics to CI Mappings** page appears.

<table id="table_q3n_gdq_2fb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Data source for the metric.

</td></tr><tr><td>

Metric Type Id

</td><td>

Metric that is measured for the CI, such as disk% and cpu%.

</td></tr><tr><td>

Metric Identifier

</td><td>

A string in the form of CI/resource/metric that uniquely identifies a CI and a metric.

</td></tr><tr><td>

Configuration Item

</td><td>

The CI in the CMDB that is mapped to a metric. A missing value indicates that: -   The mapping of the metric to a CI was unsuccessful.
-   Resource binding is enabled, but has failed. **Configuration Item** is missing even though binding to a CI was successful.


</td></tr><tr><td>

Resource

</td><td>

The resource that is mapped to a metric. If resource binding is enabled, then a missing value indicates that the mapping of the metric to a resource was unsuccessful.

</td></tr><tr><td>

Expiration Date

</td><td>

Record expiration date.

</td></tr><tr><td>

Anomaly Detection Action Level

</td><td>

The level of anomaly detection processing and analysis applied to CIs and metrics. The available options are: -   **Metrics Only**: Only gather metrics from the data source without any further processing.
-   **Bounds**: Includes the Metrics Only processing level, and also creates a statistical model and shows bounds in Insights Explorer.
-   **Anomaly Scores**: Includes the Bounds processing level, and also calculates and displays anomaly scores.
-   **Anomaly Alerts**: Includes the Anomaly Scores processing level, and also creates anomaly alerts, as applicable.
-   **IT Alerts**: Includes the Anomaly Alerts processing level, and also creates IT alerts which are based on anomaly alerts, as applicable.


</td></tr><tr><td>

Binding Status

</td><td>

Status of the mapping of the metric to a CI or resource. A **CI Found** status indicates that the mapping was successful, in which case the mapped CI appears in the **Configuration Item** column.

Any other status indicates that the mapping failed, and a general reason for the failure is provided. Further details about the failure are provided in the **Binding Failure Reason** column.

</td></tr><tr><td>

Binding Failure Reason

</td><td>

Specific details about the mapping that failed, such as class and host names, and the queries that were used. Click the respective **Event** link to see further details in the **Processing Notes** field.

</td></tr></tbody>
</table>2.  Examine the **Binding Status** and **Binding Failure Reason** as appropriate.

    Use the details provided to remediate the problem:

<table id="table_ibw_43q_2fb"><thead><tr><th>

Binding Status

</th><th>

Remediation

</th></tr></thead><tbody><tr><td>

Host CI Missing

</td><td>

Run Discovery or use any other method to populate the CMDB with the missing host CI.

</td></tr><tr><td>

Non-Host CI Missing

</td><td>

Run Discovery or use any other method to populate the CMDB with the missing non-host CI.

</td></tr><tr><td>

Non-Host CI Duplicate

</td><td>

Use the [Duplicate CI Remediator](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to remediate the duplication.

</td></tr><tr><td>

Dependent CI Duplicate

</td><td>

Use the [Duplicate CI Remediator](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to remediate the duplication.

</td></tr><tr><td>

Dependent CI Missing

</td><td>

Run Discovery or use any other method to populate the CMDB with the missing dependent CI.

</td></tr><tr><td>

Duplicate Metric Map Entry Exists

</td><td>

Check **Binding Failure Reason** and compare the metric identifiers associated with the duplicate metric map entries. If metric identifiers have changed \(for example, an identifier was added\), set the entry for this series in the CI Mappings \[sa\_metric\_map\] table to expire or delete the entry.

Also check the associated event rule and ensure that it extracts the attributes correctly and that it does not extract the same CI for two different metric identifiers. This error might appear when 2 different metric identifiers map to the same CI/metric.

</td></tr><tr><td>

Resource ID Not Found

</td><td>

Verify that the CI Type To Resource Class \[sa\_ci\_type\_to\_resource\_class\] table contains a mapping record for the respective CI type, or for one of its parents. Then ensure that a table with the name of resource class for this record, exists.

</td></tr></tbody>
</table>
## What to do next

Group **Binding Failure Reason** by **Binding Status** to create a summary report with the number of records per failure category. Use this report to efficiently remediate the problems.

**Related topics**  


[Create an event rule to map metrics to specific CIs](../concept/event-rule-bind-metrics-to-ci.md)

