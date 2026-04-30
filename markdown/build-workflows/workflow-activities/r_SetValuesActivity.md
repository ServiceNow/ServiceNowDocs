---
title: Set Values workflow activity
description: The Set Values activity sets values on the current record when the workflow quiesces or ends.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Set Values workflow activity

The **Set Values** activity sets values on the current record when the workflow quiesces or ends.

## Input Fields

The values you enter in the following fields determine the behavior of the activity.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set these values

</td><td>

From the list on the left, select the field on the current record whose value you want to set when the workflow quiesces or ends. In the user-input field to the right, select or enter the value to which you want that field set.**Note:** Avoid setting the same fields from different **Set Value** activities. The workflow only sets the value specified by the last **Set Values** activity run before quiescing or ending.

</td></tr></tbody>
</table>**Note:** Using the **Set Values** activity to set the **Approval** field on a task does not cancel pending approvals. To approve a task in a workflow, use the [**Approval Action**](https://www.servicenow.com/docs/access?context=r_ApprovalAction&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) activity instead.

