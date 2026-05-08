---
title: Operational Technology change approval
description: The Operational Technology \(OT\) change approval lets reviewers approve your requested changes and suggest improvements as necessary.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Operational Technology change approval

The Operational Technology \(OT\) change approval lets reviewers approve your requested changes and suggest improvements as necessary.

## Change approval overview

An OT change approval with the Advanced OT Change Model enables approvers to review a change request, edit the request as necessary, and approve the change request.

**Note:** The change approval only applies to the Advanced OT Change Model. There’s no change approval policy applied to the Basic OT Change Model.

|Requirement|Description|
|-----------|-----------|
|Site level|Site or area where the change takes place.|
|Site approval group|Members assigned to an approval group that can review and approve change requests.|
|Role required|Approvers must have the sn\_ot\_change\_read role.|
|Percentage of approvals|51% of the approval group has to approve the change for it to move forward.|

## OT change approval flow

The OT change approval flow is as follows.

1.  Create the change request.
2.  The flow is invoked based on the change model.
3.  The flow applies the change approval policy.
4.  Various decision records are evaluated.
5.  Matching approval definitions are executed.
6.  Add a list of site level approvers to the change record.

The Advanced OT Change Model contains a change approval policy. You can also create your own approval policy. For more information about how to create an approval policy, see Create change approval policies.

-   **[Add an approver to review a change request](../task/select_an_approval_group.md)**  
Add a group member, or approver, manually to your approval group to review your Operational Technology \(OT\) change request.

**Parent Topic:**[Using Operational Technology Change Management](../concept/using-operational-technology-change-management.md)

