---
title: Review and activate a workflow
description: Review the workflow configuration and activate the workflow so it can be applied to new issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Review and activate a workflow

Review the workflow configuration and activate the workflow so it can be applied to new issues.

## Before you begin

The workflow's basic details, workflow components, state-to-stage mappings, and trigger condition and priority must be configured. See [Set the trigger condition and priority for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-the-trigger-condition-and-priority-for-a-workflow.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Once a workflow is activated, it is evaluated for new issues created on the selected table.

The Review step provides a summary of the workflow's configuration, including its name, table, layout, state model, playbook, trigger condition, priority, state-to-stage mappings, and approvals. Reviewing this information helps you identify configuration issues before the workflow is set to active.

The **Activate workflow** button is available only when the workflow reaches the **Review** step. Approvals are optional and don't need to be configured before you activate the workflow. See [Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md).

## Procedure

1.  On the **Review** step, review the workflow summary.

2.  View additional details about a component, such as the state model or playbook, by selecting the information icon next to it.

    You can view or modify the underlying record by selecting **Open record**.

3.  Update the workflow configuration by selecting the appropriate workflow step, making the changes, and returning to the **Review** step.

4.  Select **Activate workflow**.


## Result

The workflow status changes to Active. The workflow appears as active in the issue workflow list and is evaluated for new issues on the selected table.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

**Related topics**  


[Clone an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/clone-an-issue-workflow.md)

[Reassign an issue's workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/reassign-an-issue-s-workflow.md)

