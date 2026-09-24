---
title: Review and activate a workflow
description: Review the workflow configuration and activate the workflow so it can be applied to new issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Review and activate a workflow

Review the workflow configuration and activate the workflow so it can be applied to new issues.

## Before you begin

The workflow's basic details, workflow components, state-to-stage mappings, and trigger condition and priority must be configured.

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

The **Review** step provides a summary of the workflow's configuration, including its name, table, layout, state model, playbook, trigger condition, priority, state-to-stage mappings, and approvals. Reviewing this information helps you identify configuration issues before the workflow becomes active.

The **Activate workflow** button is available only when the workflow reaches the **Review** step. Approvals are optional and don't have to be configured before you activate the workflow. See [Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md).

## Procedure

1.  On the **Review** step, review the workflow summary.

2.  View additional details about a component, such as the state model or playbook, by selecting the information icon next to it.

    You can view or modify the underlying record by selecting **Open record**.

3.  If the summary shows a configuration that you want to change, select the appropriate workflow step, make the changes, and return to the **Review** step.

4.  Activate the workflow by selecting **Activate workflow**.

    The state attributes on the state model that the workflow uses are checked. If a required state attribute isn't applied to any state, a warning is displayed.


## Result

-   The workflow status changes to **Active**.
-   The workflow is evaluated for new issues created on the selected table.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

