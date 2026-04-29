---
title: Approve or reject a conflict of interest disclosure request
description: Approve or reject a conflict of interest disclosure request assigned to you or a legal user group of which you're a member.
locale: en-US
release: australia
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Approve or reject a conflict of interest disclosure request

Approve or reject a conflict of interest disclosure request assigned to you or a legal user group of which you're a member.

## Before you begin

Role required: sn\_lg\_ops.coi\_fulfiller or sn\_lg\_ops.request\_fulfiller

## About this task

Before approving or rejecting a request, you can review the risk assessment results to understand the risk level and the factors that contributed to the score. The risk level \(Low, Medium, or High\) is displayed in the request header, and detailed evaluation results are available in the Risk responses tab. For more information, see [View risk assessment details](lsd-coi-view-risk-asmt-dets.md).

The multi-level approval flow for a conflict of interest disclosure request is automated through the **COI Approval flow**. The flow controls the request to advance to the next approval level when approved at one approval level. After the final-level approval, a conflict of interest disclosure record is created. The approval or rejection of the request and the end date specified in the request determines the state of the newly created disclosure record.

For more information on approval flow, see [Conflict of Interest – Approval flow](../concept/conflict-of-interest-overview.md#section_COI_Approal_Flow).

**Note:** If the approval is assigned to an approval group, any member from the group can approve or reject the request.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, under **My Work**, click **Items Pending Approval**.

4.  In the Items Pending Approval list, open a request by clicking the request number in the **Approval for** column.

5.  If it's an existing request that is updated by the requester, review and validate the changes from the Activities stream.

6.  View risk assessment details by viewing the Risk level field on the secondary header and navigating to Risk responses tab.

7.  In the **Approvers** tab, click **Requested** in the **State** column to open the approval form.

8.  Approve or reject the request.

    -   To approve the conflict of interest disclosure request, click **Approve**.
    -   To reject the conflict of interest disclosure request, click **Reject**.

## Result

The approval status of the request is updated in the Approvers tab.

The following table shows the results of approve and reject actions on the approval request.

<table id="table_xst_hbd_hlb"><thead><tr><th>

Approve

</th><th>

Reject

</th></tr></thead><tbody><tr><td>

-   The state of the current approval level in the request updates to Approved.
-   If available, the request advances to the next approval level and is assigned to an approver or approver group set in the approval level. The state of the next approval is set as Requested.
-   If the current approval is the last in the approval flow, the approval moves to the Approved state. The legal request status changes to Closed.
-   For a new request, a corresponding conflict of interest disclosure record is created. For an existing request, the related conflict of interest disclosure record is updated.

The state of the conflict of interest disclosure record is based on the following conditions:

    -   If the end date of the record is empty or later than the approval date, the state is Active.
    -   If the end date of the record is prior to the approval date, the state of the record is Inactive.

</td><td>

-   The state of the current approval level in the request updates to Rejected.
-   All the subsequent approval levels in the approval flow are skipped.
-   The legal request status updates to Closed.
-   The comments for rejection posted by the approver is added to the request.
-   For a new request, a corresponding conflict of interest disclosure record is created in the Rejected state.
-   For an existing request, the related conflict of interest disclosure record is updated without changing its existing state.

</td></tr></tbody>
</table>**Parent Topic:**[Using Legal Conflict of Interest](../concept/lsd-coi-use-landing.md)

