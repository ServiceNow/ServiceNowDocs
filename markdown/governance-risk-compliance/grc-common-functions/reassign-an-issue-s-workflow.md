---
title: Reassign an issue's workflow
description: Change the workflow assigned to an issue when more than one active workflow exists for the issue's table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/reassign-an-issue-s-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Reassign an issue's workflow

Change the workflow assigned to an issue when more than one active workflow exists for the issue's table.

## Before you begin

The issue must already have an assigned workflow. More than one active workflow must exist for the issue's table.

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Reassigning a workflow changes the layout, state model, and playbook applied to the issue. If the issue is grouped, reassigning the parent issue's workflow cascades to all child issues in the group.

## Procedure

1.  Open the issue.

2.  Select **Change workflow**.

3.  Select the new workflow.

    |Grouping status|Action|
    |---------------|------|
    |Standalone issue|No warning is displayed.|
    |Parent issue|A warning indicates that reassigning the workflow also reassigns the workflow of every child issue in the group.|
    |Child issue|Reassigning is unavailable. Reassign the parent issue's workflow instead.|

4.  Select **Change workflow** to confirm.


## Result

The issue is reassigned to the new workflow. Its layout, state model, and playbook update accordingly. If the issue is a parent, all child issues are reassigned to the same workflow.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

