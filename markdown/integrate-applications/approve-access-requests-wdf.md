---
title: Review and approve data access requests
description: Review and act on requests from consumers who need access to a data product or data interface.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 1
breadcrumb: [Data Products, Workflow Data Fabric]
---

# Review and approve data access requests

Review and act on requests from consumers who need access to a data product or data interface.

## Before you begin

You must be a member of the Data Catalog approvers group. An administrator manages group membership.

Roles required: approval\_user and dcg\_catalog\_readable

## About this task

When a consumer requests access to a data product or data interface, a task is created. The task is routed to the Data Catalog approvers group. Any member of the group can approve or reject the request — only one approval is required. After approval, the requesting user is automatically granted the role needed to query the data asset and the task closes.

**Note:** Access requests are only available for data products and data interfaces, not other data asset types.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Approvals**.

    The Approval Center opens, listing all pending approvals assigned to you or your group.

2.  Find and open the pending Data Catalog access request.

    The short description identifies the requesting user and the data asset they need to access, for example: `User requesting access to resource: Travel Analytics`.

3.  Review the request details to verify the user and data asset.

    The request record shows the requesting user, the data product or data interface name, and the current approval state. Use this information to evaluate whether to grant access.

4.  Select **Approve** or **Reject**.

    -   Approve: The requesting user is automatically granted the role required to query the data asset. The access request task closes.
    -   Reject: Access is not granted. The requesting user is notified and the task closes.

## Result

After approval, the requesting user can query the data product or data interface through workflows, dashboards, or APIs. No further action is required — role assignment and task closure happen automatically.

