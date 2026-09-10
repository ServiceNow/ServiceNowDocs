---
title: Clone an issue workflow
description: Create a copy of an existing workflow to use as a starting point for a new workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/clone-an-issue-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Clone an issue workflow

Create a copy of an existing workflow to use as a starting point for a new workflow.

## Before you begin

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Cloning a workflow copies its layout, state model, playbook, state-to-stage mappings, and approvals. The cloned workflow does not copy the trigger condition or priority, and is created with a status of In Progress.

## Procedure

1.  Navigate to **All** &gt; **GRC Issue Administration** &gt; **Issue Workflows**.

2.  Open the workflow that you want to clone.

3.  Select **Clone workflow**.

4.  Enter a name for the cloned workflow.

    If you don't provide a name, the new workflow is named after the original, with `(copy)` appended.

5.  Select **Clone**.


## Result

The cloned workflow opens with a status of In Progress. You must set the trigger condition and priority, then activate the workflow before it takes effect.

## What to do next

Set the trigger condition and priority. See [Set the trigger condition and priority for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/set-the-trigger-condition-and-priority-for-a-workflow.md). Then review and activate the workflow. See [Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

