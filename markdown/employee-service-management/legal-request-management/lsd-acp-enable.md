---
title: Disable attorney client privilege for a legal request
description: Disable attorney client privilege for a legal request.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work on a legal request, Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Disable attorney client privilege for a legal request

Disable attorney client privilege for a legal request.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

As a fulfiller, you can disable Privilege and Confidential status for a legal request to remove privileged and confidential status. The remove action is available only when the request is in the Assigned or Work in progress state. You can not change the Privileged and Confidential status of requests in Closed Complete, Closed Incomplete, or Cancelled states.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d725791e102">

Option

</th><th align="left" id="d725791e105">

Steps

</th></tr></thead><tbody><tr><td id="d725791e111">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d725791e140">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  Disable Privileged and Confidential status.

    1.  Click the More actions icon \(![More actions icon](../../workplace-central/images/more-actions-move-schedule.png)\).

    2.  Select **Remove Privileged and Confidential**.

        ![Disable privileged and confidential](../image/lr-disable-acp.png)

    3.  In the confirmation modal enter work notes and select **Disable**.


## Result

-   The Privileged and Confidential status is removed.
-   The assignment group permission is retained as it was before removing the privileged and confidential status.
-   Privileged and Confidential field in the secondary header is changed to Disabled.
-   In the Privileged Document Access tab, the document permissions is marked as Public.
-   Stakeholders are notified of the change.

**Parent Topic:**[Work on a legal request](../task/work-on-legal-request.md)

