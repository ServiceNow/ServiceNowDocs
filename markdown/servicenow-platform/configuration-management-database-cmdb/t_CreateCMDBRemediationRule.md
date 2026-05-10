---
title: Create a CMDB remediation rule
description: A CMDB remediation rule is associated with a task that was created for a failed CMDB health test. A CMDB remediation rule is applied automatically or manually to execute a remediation workflow that can, for example, delete stale CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB remediation rule

A CMDB remediation rule is associated with a task that was created for a failed CMDB health test. A CMDB remediation rule is applied automatically or manually to execute a remediation workflow that can, for example, delete stale CIs.

## Before you begin

You must first create and publish a remediation workflow that addresses the CI issue, stored in the Workflow \[wf\_workflow\] table. The workflow can be a regular workflow or an Orchestration workflow, and must adhere to the following requirements:

-   The table in the workflow must match the task type in the remediation rule.
-   The workflow isn't configured with any filter conditions by setting **If condition matches** to `None`, so that the filters of the CMDB remediation rule will apply.

For more information about using Classic Workflows, see [Classic Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowOverview.md).

Role required: sn\_cmdb\_admin or itil\_admin \(on top of sn\_cmdb\_editor or itil\)

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Remediations**.

2.  Select **New** and then fill out the CMDB Remediation Rule form.

<table id="table_xfq_njn_q5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Remediation name.

</td></tr><tr><td>

Task type

</td><td>

Type of CMDB health-related tasks to apply the remediation to.

</td></tr><tr><td>

Task filter

</td><td>

Filters tasks to apply remediation to. Also applies [dot-walking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md) on CI fields so that remediation is applied to tasks associated with matching CIs.

</td></tr><tr><td>

Execution

</td><td>

-   Manual: Remediation is applied manually.
-   Automatic: The workflow is applied once, upon the creation of a task that matches the **Task type** and **Task filter**.


</td></tr><tr><td>

Active

</td><td>

Allowing the workflow to run.

</td></tr><tr><td>

Workflow

</td><td>

The CMDB remediation workflow \(regular or Orchestration\) that will execute automatically or manually, depending on the **Execution** setting. You can click the **Lookup using list** icon, and then click **New** to create a new workflow.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

If **Execution** is set to Automatic, then the business rule **Run remediations for CMDBHealth task** applies the remediation workflow to CIs that match the Task filter. If **Execution** is set to Manual, then you can manually apply the remediation workflow defined in the rule.

-   **[Apply CMDB remediation](t_ApplyCMDBRemediation.md)**  
Manually initiate a workflow to remediate a CI that failed a CMDB health test. For example, you can remediate CIs that are orphan or stale.

**Parent Topic:**[CMDB Health](../concept/c_CMDBHealth.md)

**Related topics**  


[Exploring CMDB Health](../concept/exploring-cmdb-health-parent.md)

[CMDB Health experience in CMDB Workspace and in Service Graph Workspace](../concept/cmdb-health-exp-cmdb-workspace.md)

[View CMDB Health Dashboard](../concept/c_MonitorCMDBHealth.md)

[View relationships health](t_ViewRelationshipsHealth.md)

[View CI health](t_ViewCIHealth.md)

[CMDB Health process tracking and troubleshooting](../concept/c_CMDBHealthTroubleshooting.md)

[CMDB Health reference](../concept/cmdb-health-ref-parent.md)

[Dot-Walking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md)

