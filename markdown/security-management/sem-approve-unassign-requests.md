---
title: Approve or reject an unassign request
description: Approve requests for the removal of findings from an assignment group or an individual user in the Security Exposure Management Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Approve or reject an unassign request

Approve requests for the removal of findings from an assignment group or an individual user in the Security Exposure Management Workspace.

## Before you begin

Role required: For unassign approvals, one approver is required in the Approver – Level 1 group.

-   sn\_vul.unassign\_approver for AVITs and VITs
-   sn\_vul\_container.unassign\_approver for CVITs

## About this task

By default, an approval configuration is provided and an unassign approval group is created. Users of the Unassign Approver - Level 1 group can approve the request. This group contains an unassign approver role, sn\_vul.unassign\_approver, by default. You can modify or create a new group and update the approval configuration. To configure an approval rule, select any of the following approval rule in the Approval Rules module and navigate to the approval configuration on the **Approval Configurations** tab:

-   **Vulnerable item field change request** for a vulnerable item.
-   **Vulnerability field change request** for a remediation task.
-   **Application vulnerability field change request** for an application vulnerable item \(AVIT\).
-   **Approval for container management** for a container vulnerable item \(CVIT\).

For more information on approval rules and configurations, see [Approval workflow configurations for unassign request](../../vulnerability-response/concept/vr-unassign-approval-rules.md).

**Important:** You can approve or reject requests in the Vulnerability Manager Workspace. .

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **My Approvals** for VITs and AVITs.

    Alternatively, navigate to **All** &gt; **Container Vulnerability Response** &gt; **My Approvals** for CVITs.

2.  Select a request from your queue.

3.  Approve or reject the request by adding the appropriate comments.


