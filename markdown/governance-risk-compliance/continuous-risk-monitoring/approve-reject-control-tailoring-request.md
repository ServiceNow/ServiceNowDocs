---
title: Approve or reject a control tailoring request
description: As an Authorizing Official \(AO\) or AO Delegate, review and approve or reject control tailoring requests to ensure governance and oversight of baseline control modifications.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request control tailoring, Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Approve or reject a control tailoring request

As an Authorizing Official \(AO\) or AO Delegate, review and approve or reject control tailoring requests to ensure governance and oversight of baseline control modifications.

## Before you begin

-   A pending control tailoring request assigned to you
-   Understanding of the authorization package's current baseline and assessment status

Role required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.authorization\_official

## About this task

Control tailoring requests allow users to modify baseline controls after the Select step. As the AO, you review these requests to ensure that proposed changes align with security and compliance requirements. When you approve a request, the system triggers an item generation job that applies the changes to baseline controls and updates related controls. When you reject a request, no changes are applied to the package.

The approval process ensures that all baseline modifications are subject to appropriate oversight and that changes are traceable for audit purposes.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** &gt; **Tasks**.

2.  Select the **In Review** filter to view pending control tailoring requests assigned to you.

3.  Select the control tailoring request record to open it.

4.  On the **Details** tab, review the request reason and authorization package information.

5.  Select the **Requested Changes** tab to view proposed modifications.

    The tab displays:

    -   Previous allocation - The control's current allocation type
    -   Requested allocation - The proposed allocation type
    -   Controls grouped by change type \(added, removed, allocation changed\)
6.  To approve the request:

    1.  Select **Approve**.

        The request state changes to Approved. The system triggers an asynchronous item generation job to apply changes to the package.

        When approved, the authorization package work notes record the approval decision and timestamp. The requester can view the approval status in their My Items task list.

7.  To request more information:

    1.  Select **Request More Information**.

    2.  Enter comments explaining what additional information is needed.

        The request returns to the submitter in Draft state for modifications.

8.  To reject the request:

    1.  Select **Reject**.

    2.  Enter rejection reason in the comments.

        The request state changes to Rejected. No changes are applied to the package.


