---
title: Approve or reject a release task
description: Review a release task and approve or reject it.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Approve or reject a release task

Review a release task and approve or reject it.

## Before you begin

Role required: approver\_user

## Procedure

1.  Navigate to **All** &gt; **Service Desk** &gt; **My Approvals**.

2.  In the My Approvals list, click a record to open for approval.

3.  Review the record and either approve or reject:

    -   To approve the record, click **Approve**.
    -   To reject the record, enter comments for rejection in the **Comments** field and click **Reject**.

## Result

The following table shows the result of approve and reject actions on the approval record of a release task.

<table id="table_xst_hbd_hlb"><thead><tr><th>

Approve

</th><th>

Reject

</th></tr></thead><tbody><tr><td>

-   The approval record's state updates from Requested to Approved.

If the requested item was assigned to a user group for approval, then the state of the approval records for the remaining users updates from Requested to No Longer Required.

-   The **State** field on the release task updates from Open to Closed Complete.
-   The **Approval** field on the release task updates from Requested to Approved.

</td><td>

-   The approval record's state updates from Requested to Rejected.

If the requested item was assigned to a user group for approval, then the state of the approval records for the remaining users updates from Requested to No Longer Required.

-   The **State** field on the release task remains Open.
-   The **Approval** field on the release task updates from Requested to Rejected.
-   The rejection comments posted by the approver is added to the release task's Activities section.

</td></tr></tbody>
</table>**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

