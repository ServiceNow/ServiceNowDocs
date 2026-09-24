---
title: Reassign an issue's workflow
description: Change the workflow that an existing issue follows so the issue uses the states, layout, and approval rules of a different workflow on the same table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/reassign-an-issue-s-workflow.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 2
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Reassign an issue's workflow

Change the workflow that an existing issue follows so the issue uses the states, layout, and approval rules of a different workflow on the same table.

## Before you begin

The issue must already have an assigned workflow.

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

An issue is not reassigned to a different workflow automatically, even if a higher-priority workflow's trigger condition would now match it. Reassigning a workflow resets the issue to the new workflow's initial state, regardless of its current state. Any playbook activity that is in progress on the issue is cancelled, and any approval requests that are awaiting a decision are cancelled. A state change in the new workflow that requires an approval needs a new approval request.

Reassignment preserves the issue's attachments and related records, including remediation tasks, child issues, impacted entities, and impacted items. Field data is retained only where the field exists in both the current and the target workflow. Active remediation tasks are carried over from the previous workflow and need review for applicability under the new one.

## Procedure

1.  Open the issue.

2.  Select the More Actions icon next to **Save**, and then select **Reassign workflow**.

3.  Fill in the reassignment fields.

    |Field|Description|
    |-----|-----------|
    |**Reassign to**|The workflow to assign to the issue. Selecting a workflow that changes the issue's grouping status displays an additional warning.|
    |**Reason for reassignment**|The business justification for the reassignment.|
    |**Notify stakeholders**|The stakeholders to notify about the reassignment. Review and update the list as needed.|

4.  Review the warning and confirm the reassignment.

    The warning and the confirmation label depend on the issue's grouping status.

<table id="choicetable_reassignment_confirmation"><thead><tr><th align="left" id="d229044e154">

Issue grouping status

</th><th align="left" id="d229044e157">

Action

</th></tr></thead><tbody><tr><td id="d229044e163">

**Standalone issue, or an issue in a group managed from the child \(__Manage child__\)**

</td><td>

A warning indicates that the issue's current workflow will be replaced. Select **Change workflow**.

</td></tr><tr><td id="d229044e181">

**Child issue in a group managed from the parent \(__Manage parent__\)**

</td><td>

A warning indicates that the issue will be removed from the group and become a standalone issue, because all issues in a **Manage parent** group must use the same workflow. Select **Change workflow and remove from group**.

</td></tr><tr><td id="d229044e202">

**Parent issue in a group managed from the parent \(__Manage parent__\)**

</td><td>

A warning indicates that the parent issue and all child issues will be reassigned to the new workflow and reset to its initial state. Select the confirmation control, which indicates the number of child issues affected.

</td></tr></tbody>
</table>
## Result

-   The issue uses the new workflow's states, layout, and approval rules and starts from the new workflow's initial state.
-   A work note records the previous workflow, previous state, new workflow, reason for reassignment, user, and date. If the reassignment affects a group, an additional work note records the impact on the parent or child issues.
-   The stakeholders selected in the **Notify stakeholders** field receive an email notification.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

**Related topics**  


[Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md)

[Deactivate an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/deactivate-an-issue-workflow.md)

[Cancel an approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/cancel-an-approval.md)

