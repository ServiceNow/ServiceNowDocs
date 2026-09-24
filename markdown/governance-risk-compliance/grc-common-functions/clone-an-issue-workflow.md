---
title: Clone an issue workflow
description: Create a copy of an existing workflow to use as a starting point for a new workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/clone-an-issue-workflow.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Clone an issue workflow

Create a copy of an existing workflow to use as a starting point for a new workflow.

## Before you begin

An issue workflow must already exist. See [Create an issue workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/create-an-issue-workflow.md).

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Cloning copies the workflow's configuration, including its layout, state model, playbook, trigger condition, priority, and approvals. The cloned workflow's name defaults to the original workflow name followed by `(copy)`.

After a workflow is cloned, each workflow step contains the copied configuration. However, the steps remain in a Pending state until you open them and save the configuration. You can review and modify any configuration before saving it.

## Procedure

1.  Navigate to **All** &gt; **GRC Issue Administration** &gt; **Issue workflows**.

2.  In the **Issue workflows** list, select the workflow that you want to clone.

3.  Select **Clone**.

4.  Update the workflow **Name**, **Description**, or **Table**.

5.  Open each remaining workflow step and save the copied configuration.


## Result

A new workflow is created with the copied configuration.

## What to do next

Review and activate the workflow. See [Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

