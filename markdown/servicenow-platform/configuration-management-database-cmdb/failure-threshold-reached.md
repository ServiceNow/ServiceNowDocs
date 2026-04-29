---
title: CMDB Health process status: failure threshold reached
description: The CMDB Health Dashboard shows the string ‘failure threshold reached' when the number of CIs that are failing the metric tests, reaches the failure threshold set for the metric.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Tracking and troubleshooting, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Health process status: failure threshold reached

The CMDB Health Dashboard shows the string ‘failure threshold reached' when the number of CIs that are failing the metric tests, reaches the failure threshold set for the metric.

CMDB Health stops processing for this metric in the current cycle, and therefore there is no aggregated health score for the metric. Processing will be attempted again in the next cycle. Also, status in the CMDB Health Metric Status \[cmdb\_health\_metric\_status\] table is set to **Max Failures** for this metric.

When the health score of a metric cannot be evaluated, then the processing status of the respective KPI \(for example, correctness\) is set to **Incomplete**. The CMDB Health Dashboard shows the string **Incomplete score** for the respective KPI. Also, aggregated health scores for the metric are not available for any class in the CMDB hierarchy.

Review and refine the rules defined for the metric which has reached max failures. If a rule associated with the metric is too generic, resulting in large number of failures, attempt to refine it as follows:

-   Completeness:

    Review the mandatory fields for the associated classes and remove those that aren't critical for the health score. Also, review the recommended fields that are causing failures and remove those that aren't critical for the health score.

    For more information see [Set a CI attribute to be mandatory](../task/t_SetCIFieldMandatory.md) and [Set a CI field to be recommended](../task/t_MakingAFieldRecommended.md).

-   Compliance:

    Review the audit failures from the audit jobs and adjust the audits to reduce the number of failures. For more information, see [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

-   Correctness:

    -   Orphan: Review the orphan rules and adjust them to remove excessive orphan failures. For more information, see [Create a CMDB Health orphan rule](../task/t_CreateCMDBHealthOrphanRule.md).
    -   Staleness: Review the effective duration for the classes that are causing failures and adjust the duration to reduce the number of failures. For more information, see [Create a CMDB Health staleness rule](../task/t_CreateCMDBHealthStaleRule.md).
    -   Duplicate: Review the de-duplication tasks and remediate the tasks to remove duplicate CIs and to avoid creating failure records. For more information, see [Remediate a de-duplication task \(manual\)](../task/reconcile-dup-task.md).

For more troubleshooting information about failure threshold related issues, see the [How to Resolve Max Failure Threshold Errors for CMDB Health Dashboard \[KB2487349\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2487349) article in the Now Support Knowledge Base.

**Parent Topic:**[CMDB Health process tracking and troubleshooting](c_CMDBHealthTroubleshooting.md)

