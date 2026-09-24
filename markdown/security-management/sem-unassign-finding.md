---
title: Unassign a finding or remediation task
description: Reassign a finding or remediation task away from the current owner or group when the assignment is incorrect, when scope has changed, or when the current owner cannot complete the work. Unassignment requires approval before the new assignment takes effect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-unassign-finding.html
release: brazil
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [unassign, reassign, remediation task, vulnerability finding]
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Unassign a finding or remediation task

Reassign a finding or remediation task away from the current owner or group when the assignment is incorrect, when scope has changed, or when the current owner cannot complete the work. Unassignment requires approval before the new assignment takes effect.

## Before you begin

Role required: sn\_vul.remediation\_owner \(to request an unassignment\); sn\_vul.unassign\_approver \(to approve or reject the request\).

The finding or remediation task must be in an active state \(not Closed, Deferred, or Expired\).

## About this task

Unassignment is appropriate when:

-   The finding was routed to the wrong asset owner or assignment group.
-   Organizational scope has changed and another team now owns the affected asset.
-   The current owner cannot complete the remediation and an alternate owner is available.

Unassignment is not appropriate when the finding cannot be remediated at all. For that case, use **Request Exception** or **Mark as False Positive**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List** &gt; **Remediation Tasks**.

2.  Open the finding or remediation task to unassign.

    Use the filter bar to find a specific record by ID, severity, or current assignee. To narrow the list to your own tasks, set the **Assigned to** filter to **Me**.

3.  Select **Unassign**.

4.  In the **Unassign** dialog box, provide the following:

    -   **Reason** — select from the choice list \(for example, Wrong asset owner, Scope change, Owner unavailable, Other\).
    -   **Justification** — describe why the current assignment is incorrect and what changed.
    -   **Proposed new assignee** — optional. The user or group that should receive the finding after approval. If left blank, the approver routes the finding using the standard assignment rules.
    -   **Evidence** — optional. Attach supporting documents such as the asset ownership record, an organizational change notice, or correspondence from the current owner.
5.  Select **Request Approval**.

    The finding state transitions to **In Review**. A change approval record \(VCA\#\) is generated and routed to a member of the Unassign Approver group. The current owner receives an email notification that the unassignment is pending review.


## Result

The finding remains in the **In Review** state until the unassign approver acts on it. While in review, the finding cannot be remediated; standard work on the task is paused.

On approval, the finding reassigns to the proposed assignee \(or to the standard routing target if no proposed assignee was provided\) and transitions back to the prior active state. Both the original owner and the new owner receive email notifications.

On rejection, the finding reverts to its previous state with the original assignee. The requester receives an email with the approver's justification.

## What to do next

To track the unassignment request, open the finding and navigate to the **Change Approvals** tab; the approval record shows the current state, approver, and decision history.

If multiple findings need to be unassigned to the same new owner, repeat this task for each finding. Bulk unassignment is not supported.

