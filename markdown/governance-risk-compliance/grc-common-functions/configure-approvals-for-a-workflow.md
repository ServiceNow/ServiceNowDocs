---
title: Configure approvals for a workflow
description: Attach approvals to a workflow so issues or remediation tasks require approval before certain actions can be completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Configure approvals for a workflow

Attach approvals to a workflow so issues or remediation tasks require approval before certain actions can be completed.

## Before you begin

An approval configuration record must already exist for the approval that you want to attach. See [Set up an approval configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-up-approval-configurator.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

An approval can apply to an issue or to a remediation task. A **State Change** approval prevents an issue from progressing beyond a specified state until the approval is granted. A **Due Date Extension** approval is used when a due date extension request requires approval and is not associated with a specific workflow state.

## Procedure

1.  On the **Approvals** step, select **Add**.

2.  Fill in the approval fields.

    |Field|Description|
    |-----|-----------|
    |**Approval name**|A name for the approval.|
    |**Applicable table**|The table to apply this approval to, either **Issue** or **Remediation Task**.|
    |**Approval**|An approval defined in the approval configuration. This field becomes available after you enter a name and select a table. The available approval records depend on the selected table. To create an approval configuration record, select **Create new**.|
    |**Approval type**|Whether this approval requires a **State Change** or a **Due Date Extension** request.|
    |**State**|The state in which the approval can be requested. Available only when **Approval type** is set to **State Change**. The list contains the states defined in the workflow's state model.|

3.  Select **Add**.

4.  Add any remaining approvals that the workflow requires.


## Result

The approvals are associated with the workflow.

For a State Change approval, an issue can't move beyond the associated state until the approval is granted. Actions that move the issue to the next state are unavailable while the approval is pending.

## What to do next

Review and activate the workflow. See [Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

