---
title: Use the Change Approval Policy workflow activity
description: Apply your Change Policy in your Change Request workflow to manage the approvals.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating change approval policies, Using Change Management, Change Management, IT Service Management]
---

# Use the Change Approval Policy workflow activity

Apply your Change Policy in your Change Request workflow to manage the approvals.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Editor**.

2.  Open the change request workflow that you want to use in the **Change Policy** activity.

3.  Drag and drop the **Change Approval Policy** activity from the **Change Policy** section in the **Core** activities tab.

    **Note:** This activity is only available when the workflow runs on a table that extends or is the change\_request table.

4.  Configure the activity by specifying the Change Approval Policy in the workflow.

5.  Configure the Policy input field to setup inputs that are defined on the associated Change Approval Policy record.

6.  Configure the **Finish condition** if the workflow needs to handle a scenario where the activity needs to complete ahead of time because of a change in the Change Request.

    For example, when the change request is on-hold.

7.  Click **Update**.


**Parent Topic:**[Creating change approval policies](../concept/using-change-approval-policies-cf.md)

