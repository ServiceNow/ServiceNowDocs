---
title: Apply CMDB remediation
description: Manually initiate a workflow to remediate a CI that failed a CMDB health test. For example, you can remediate CIs that are orphan or stale.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/t\_ApplyCMDBRemediation.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a CMDB remediation rule, CMDB Health, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Apply CMDB remediation

Manually initiate a workflow to remediate a CI that failed a CMDB health test. For example, you can remediate CIs that are orphan or stale.

## Before you begin

Role required: itil\_admin

To manually apply a CMDB remediation, a CMDB remediation rule must exist, in which **Execution** is set to **Manual**.

## About this task

Except for the duplicate and audit health metrics, you can choose to create tasks for health test failures for a metric.

To remediate failures of the duplicate metric, use [de-duplication tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/t_ResolveDeDuplicationTask.md).

For all metrics except for audit, each CI that failed a metric test is associated with a single task. Because a CI can fail multiple audits, a single CI can be associated with multiple audit tasks. The first of those tasks is in the **Task** field, and any additional tasks are in the **Additional Tasks** field. To remediate failures of the audit metric, refer to the audit tasks for the audits that the CI failed.

CMDB remediation is applied in the [CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  Select **Home** in the CMDB Workspace menu bar and then, in the Quick links section, select the **CMDB Health Dashboard** link.

    Ensure that the CMDB Health Dashboard is in **Class** view.

3.  Select one of the KPI tiles \(Completeness, Correctness, or Compliance\).

4.  Select the metric tab that is associated with the remediation that you want to apply \(such as Stale CIs\) and then select one of the class tiles.

5.  In the list view of the non-compliant CIs for the metric, select the task link \(in the Task column\) for a CI that you want to remediate.

6.  On the remediation form, select **Remediate**.

7.  In the Remediate dialog box, select the remediation workflow that you want to apply.

    The list of remediation workflows is based on the type of health metric \(such as orphan, stale\), and on the filter defined for the workflow in the associated remediation rule.

8.  Select **Next**.


**Parent Topic:**[Create a CMDB remediation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/t_CreateCMDBRemediationRule.md)

**Related topics**  


[Create a CMDB remediation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/t_CreateCMDBRemediationRule.md)

