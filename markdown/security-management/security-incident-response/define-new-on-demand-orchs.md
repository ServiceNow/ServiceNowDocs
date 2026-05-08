---
title: Define new on-demand orchestrations
description: In the base system, you can select on-demand orchestrations that execute predefined workflows. You can define new on-demand orchestrations to customize how workflows are invoked from the Run Orchestration choice lists.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define new on-demand orchestrations

In the base system, you can select on-demand orchestrations that execute predefined workflows. You can define new on-demand orchestrations to customize how workflows are invoked from the **Run Orchestration** choice lists.

## Before you begin

Role required: sn\_si.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **On-Demand Orchestration**

2.  Select **New**.

    ![Add a new on-demand orchestration](../image/on-demand-orch.png)

3.  Fill in the fields, as appropriate.

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workflow

</td><td>

Select the workflow to be included in the **Run Orchestration** choice list.

</td></tr><tr><td>

Table

</td><td>

Select the table on which the selected workflow is executed. If the table does not match the table configured for the selected workflow, you must select the **Advanced** check box and modify the **Execution script** to pass the correct record to the workflow on execution.

</td></tr><tr><td>

Roles

</td><td>

As needed, select additional roles to restrict who can see this workflow in the **Run Orchestration** choice list.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate this on-demand orchestration record.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to modify the execution script so that it passes the correct record to the selected table for this workflow.

</td></tr><tr><td>

Execution script

</td><td>

Modify the execution script so that it passes the correct record to the selected table for this workflow.This field appears only if the **Advanced** check box is selected.

</td></tr></tbody>
</table>4.  Select and hold \(or right-click\) in the record header, and select **Save**.

    The **Workflow Versions** related list appears.

5.  To make additional modifications to the workflow, you must check it out.


**Related topics**  


[bundle-crworkflow.c_WorkflowVersions]

