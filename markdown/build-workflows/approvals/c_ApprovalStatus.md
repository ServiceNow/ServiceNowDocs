---
title: Approval status
description: The approval status of a change request is determined by looking at the current status of all the approvers.
locale: en-US
release: xanadu
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Build workflows]
---

# Approval status

The approval status of a change request is determined by looking at the current status of all the approvers.

If any approver has rejected the change, the approval status will be Rejected. If all approvers have approved the change, the approval status will be Approved. If all approvers are in the Not Requested status or if there are no approvers, the change status will be Not Requested, otherwise the status will be Requested.

For added flexibility when creating approvals, including the ability to set up an "one of" approval where only one person of a group of approvers needs to approve, consider using [Workflows](../../using-workflows/concept/wf-approvals-n-rollbacks.md#) .

**Related topics**  


[Classic approvals](../reference/r_Approvals.md)

