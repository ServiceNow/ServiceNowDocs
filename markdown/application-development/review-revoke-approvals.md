---
title: Review and revoke standing approvals
description: Review the actions you have allowed Arc to take without asking, and revoke any you no longer require.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/review-revoke-approvals.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [approvals, standing approvals, Always Allow, revoke approval]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Review and revoke standing approvals

Review the actions you have allowed Arc to take without asking, and revoke any you no longer require.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

A standing approval exists only after you select **Always Allow** on an approval card when Arc asks permission for an action.

## Procedure

1.  Navigate to **Settings** &gt; **Approvals**.

2.  Review the list of standing approvals.

    Each approval's label describes the whole group of actions it covers, such as **Create any ServiceNow incident**, not only the action you approved.

    Approvals for accessing folders outside your workspace appear with a label such as **Allow read access to this path outside workspace**.

3.  Select **Revoke** for each approval to remove the approval.

    If you revoke the permission, Arc requests permission again before running the action.


**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

