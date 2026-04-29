---
title: Approve or reject the processing of custodial and non-custodial data
description: Review and approve or reject the processing of a custodial or non-custodial record of a digital forensic request.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Legal Digital Forensics, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Approve or reject the processing of custodial and non-custodial data

Review and approve or reject the processing of a custodial or non-custodial record of a digital forensic request.

## Before you begin

Role required: sn\_lg\_ops.request\_fulfiller

## About this task

The approval flow for permitting a digital forensic team member to access the custodial or non-custodial data for a digital forensic request is automated through the **Digital Forensics - Privacy Approval** flow. The flow must be in the Published state. The flow is triggered when a digital forensic request is assigned to a digital forensic team member. For each custodial and non-custodial record in the digital forensic request, one corresponding approval record is created and is assigned to each member in the legal privacy group. Any member from the group can review and approve or reject the custodian approval.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, under **My Work**, click **Items Pending Approval**.

4.  In the Items Pending Approval list, open a request by clicking **Requested** in the **State** column.

5.  Review the details of custodial and non-custodial data, and approve or reject the request.

    -   To approve, click **Approve**.
    -   To reject, click **Reject**.

## Result

The following table shows the results of approve and reject actions on the approval request.

<table id="table_xst_hbd_hlb"><thead><tr><th>

Approve

</th><th>

Reject

</th></tr></thead><tbody><tr><td>

-   The state of the approval record updates from Requested to Approved.
-   The status of the custodial record and non-custodial record in the legal request updates from Pending Approval to Approved.
-   The state of the legal request updates from Assigned to Work in Progress.

</td><td>

-   The state of the approval record updates from Requested to Rejected.
-   The status of the custodial record and non-custodial record in the legal request updates from Pending Approval to Rejected. A rejected custodian record cannot be moved to a legal matter.
-   The state of the legal request remains Assigned.

</td></tr></tbody>
</table>**Parent Topic:**[Managing digital forensics requests](../concept/managing-legal-dft-request.md)

