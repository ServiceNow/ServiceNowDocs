---
title: Create an issue workflow
description: Set up a workflow so a specific category of issues, such as vendor risk or compliance issues, follows its own states, layout, and trigger condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/create-an-issue-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Create an issue workflow

Set up a workflow so a specific category of issues, such as vendor risk or compliance issues, follows its own states, layout, and trigger condition.

## Before you begin

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

An issue workflow applies only to the table that you select when you create it. Each category of issue that requires its own states, layout, approval requirements, or guided activities needs its own workflow. This workflow replaces the table's default behavior for issues that match the workflow criteria.

Creating a workflow is the first step in a guided setup process.

## Procedure

1.  Navigate to **All** &gt; **GRC Issue Administration** &gt; **Issue Workflows**.

2.  Select **New**.

3.  Enter the workflow details.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a name that identifies the issue type and purpose of the workflow.|
    |**Description**|Optional. Enter a description of the workflow.|
    |**Table**|Select the table that the workflow applies to. The workflow applies only to issues created on this table.|

4.  Save the workflow details by selecting **Save and continue**.


## Result

The workflow record is created and its status is set to In Progress. The workflow is not set to active until you complete the remaining configuration steps and activate it.

## What to do next

Add the layout, state model, and playbook to the workflow. See [Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

