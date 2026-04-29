---
title: CMDB Health process tracking and troubleshooting
description: Use the following information to track and resolve issues with the CMDB Health processes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Health process tracking and troubleshooting

Use the following information to track and resolve issues with the CMDB Health processes.

## Logging

By default, only error messages are logged to the syslog table, with the source name CmdbHealth. To enable logging of 'info' and 'warning' messages \(which are typically logged at the start and end of each processing cycle\), update the system property glide.cmdb.logger.use\_syslog.CMDBHealth. For information about using this property, see [CMDB Health system properties](../reference/r_CMDBHealthProperties.md).

## Processing status

If scheduled jobs are enabled, but data is not displaying on the &lt;ph keyref="var.config-mgmt-database-short"/&gt; dashboard, you can check the processing status in the CMDB Health Metric Status \[cmdb\_health\_metric\_status\] table. Depending on the status of the **inactive** metric, decide how to proceed.

Initially, the state of all metrics is 'In Progress'.

Possible final states of a metric:

-   **Complete**

    All classes are processed and the number of failures is under the maximum failures threshold.

-   **Max Failures**

    The number of failures for this metric reached the maximum failures threshold. Processing has been aborted and will start over in the next run.

-   **Daily Time Out Pause**

    The processor reached the processing time limit. Processing is paused and will resume in the next run.


At the end of a processing cycle, the final state of a KPI depends on the final state of its associated metrics. Possible final state of a KPI:

-   **Complete**

    All associated metrics are in Complete state and score calculation is complete.

-   **Incomplete**

    Score is not calculated because one of the associated metrics reached its maximum failure thresholds.

-   **Daily Time Out Pause**

    Timed out because one of the associated metrics has reached its processing time limit.


## Processing time

If processing of a metric times out, you can find out which class takes too long to process. Use this information to find out if any validation rules are weak.

The progress of each metric is tracked in the CMDB Health Processor Status table \[cmdb\_health\_processor\_status\]. Status for classes that have been processed for a metric is Complete, and for classes that are yet to be processed is Draft. By looking at the update time for each class, you can calculate the length of processing time for each class.

## Orphan records due to broken hierarchy

Orphan rules might detect an orphan CI, which you are not able to access and delete. Or, there might be a mismatch between the list view that displays the orphan records, and the total number of records. These findings are due to records being deleted in the database from only one table in the CMDB hierarchy.

These CI records are not accessible via GlideRecord and must be deleted directly from the database. Therefore, in this case, to delete an orphan CI from the database you must contact Support to get help.

Orphan test results provide the details of where exactly the hierarchy is broken. For example, the message "This cmdb\_ci\_linux\_server CI \[91054fc24f22520053d6e1d18110c713\] is missing record in cmdb\_ci\_computer table" means that a record of that sys\_id must be deleted from the CMDB, cmdb\_ci, cmdb\_ci\_hardware, cmdb\_ci\_server, and the cmdb\_ci\_linux\_server tables \(the Computer class is between the Hardware and the Server classes in the hierarchy.\)

## Scripted audits Skipped

An error message is logged if the results from a scripted audit are not included in the compliance KPI. The reason can be that the script in the audit was not updated to populate its **Last ran date** field. Without a **Last ran date** value, CMDB Health is unable to identify these run results as part of a recent complete audit run, and skips those results.

-   **[CMDB Health process status: failure threshold reached](failure-threshold-reached.md)**  
The CMDB Health Dashboard shows the string ‘failure threshold reached' when the number of CIs that are failing the metric tests, reaches the failure threshold set for the metric.
-   **[CMDB Health process status: incomplete score](incomplete-score.md)**  
The CMDB Health Dashboard shows the string 'incomplete score' for a metric when it fails to calculate the score for the metric.

**Parent Topic:**[CMDB Health](c_CMDBHealth.md)

**Related topics**  


[Exploring CMDB Health](exploring-cmdb-health-parent.md)

[CMDB Health experience in CMDB Workspace and in Service Graph Workspace](cmdb-health-exp-cmdb-workspace.md)

[View CMDB Health Dashboard](c_MonitorCMDBHealth.md)

[View relationships health](../task/t_ViewRelationshipsHealth.md)

[View CI health](../task/t_ViewCIHealth.md)

[Create a CMDB remediation rule](../task/t_CreateCMDBRemediationRule.md)

[CMDB Health reference](cmdb-health-ref-parent.md)

