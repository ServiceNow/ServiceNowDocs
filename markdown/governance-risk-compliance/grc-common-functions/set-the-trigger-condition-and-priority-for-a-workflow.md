---
title: Set the trigger condition and priority for a workflow
description: Define which issues a workflow applies to and determine the order in which it is evaluated relative to other workflows on the same table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/set-the-trigger-condition-and-priority-for-a-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Set the trigger condition and priority for a workflow

Define which issues a workflow applies to and determine the order in which it is evaluated relative to other workflows on the same table.

## Before you begin

The workflow's states must already be mapped to playbook stages. See [Map states to playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/map-states-to-playbook-stages.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

When a new issue is created, the system evaluates the workflow's trigger condition. If the condition matches, the workflow can be applied to the issue.

If multiple active workflows on the same table match an issue, the workflow with the lowest priority number is selected. Priority controls the order in which matching workflows are evaluated. When you create a workflow, the system automatically assigns a default priority value that is higher than the highest priority already assigned to a workflow on the table. You can change this value as needed. If another active workflow on the same table uses the same priority value, the system displays a warning. The conflict must be resolved before the workflow can be activated.

## Procedure

1.  Define how the workflow's trigger condition is evaluated.

<table><thead><tr><th align="left" id="d338125e69">

Option

</th><th align="left" id="d338125e72">

Action

</th></tr></thead><tbody><tr><td id="d338125e78">

**No condition**

</td><td>

No action is required. The workflow applies to any issue on the selected table.

</td></tr><tr><td id="d338125e88">

**__Field-based condition__**

</td><td>

Leave **Scripted condition** cleared. Select **Edit conditions**, define the condition criteria, and then select **Set**.

</td></tr><tr><td id="d338125e108">

**__Scripted condition__**

</td><td>

Select **Scripted condition**, and then write a script that sets the result variable to either true or false. The script field includes sample comments to help you get started.

</td></tr></tbody>
</table>2.  Save the trigger condition by selecting **Save**.

3.  In the **Priority** field, review or modify the priority value.

4.  Before selecting a value, review the priority values assigned to other workflows on the same table by expanding **Existing workflows and their orders**.

5.  Save the priority value by selecting **Save**.


## Result

The workflow is evaluated for new issues on the selected table according to its trigger condition and priority relative to other active workflows.

## What to do next

Configure approvals for the workflow. See [Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

