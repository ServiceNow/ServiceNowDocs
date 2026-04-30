---
title: Track a stack request
description: The system generates a request when you submit the form to launch a stack.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Launch a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Track a stack request

The system generates a request when you submit the form to launch a stack.

## Before you begin

Role required: sn\_cmp.cloud\_service\_user

## About this task

If no approval policy is defined, requests are auto-approved. If a policy is defined, then a user on the approver list must approve the request.

If the quota limit exceeds for you or your user group, then an error message appears or the system triggers a policy-based approval. For more information about the quota limits, see [Viewing resource quota limits](../concept/resource-quota.md).

## Procedure

1.  Go to the **Activities** page or navigate to **Overview** &gt; **View Activities**, then select **Track** &gt; **Requests**.

    The following color codes show you the status of the request:

    -   Green: Completed or Approved.
    -   Orange: Processing.
    -   Red: Rejected, Error, or Canceled.
2.  In the **Requests** list, click an entry.

<table id="table-activities"><tbody><tr><td colspan="2">

**Status** tab

</td></tr><tr><td>

Request Status

</td><td>

Actions taken on the request. Click the down-arrow \(![down-arrow icon](../image/blue-down-arrow.png)\) to toggle between:-   Verbose mode that describes each action and the status of the action
-   Icon-only mode that indicates only the status \(pass/fail\) of an action.


</td></tr><tr><td>

Stack Status

</td><td>

Status of each stack request. If deployment fails, errors from cloud orchestration are listed.

</td></tr><tr><td colspan="2">

**Comments / Work Notes** tab

</td></tr><tr><td>

Item requested and request number

</td><td>

Log of comments and notes made for the request. The **itil** role is required to add a comment or work note.To add a comment or work note:

 1.  Enter text.
2.  Select the **Work notes** check box to add a work note.
3.  Click **Send**.


</td></tr><tr><td>

**Request Details** tab

</td><td>

Values that the requester submitted on the stack request form.

</td></tr><tr><td>

**Tasks** tab

</td><td>

Lists all the catalog tasks created for stacks that failed to provision. Click a catalog task to view more details about that task. See [Resubmit a failed stack request](../../cloud-management-v2/task/resubmit-failed-request.md).

</td></tr></tbody>
</table>
