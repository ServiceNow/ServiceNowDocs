---
title: Security Exposure Management Approvals View
description: The approval process in Security Exposure Management for vulnerability and compliance exceptions is unified to simplify workflows, improve visibility, and streamline actions for Approvers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Approvals View

The approval process in Security Exposure Management for vulnerability and compliance exceptions is unified to simplify workflows, improve visibility, and streamline actions for Approvers.

The Approvals landing page provides a comprehensive view of all approval requests initiated by remediation owners to view specific requests, with navigation widgets such as:

-   **Today’s approvals**: Approvals due for action today \(e.g., an unassignment request expiring by end of day\).
-   **Pending approvals**: Approvals awaiting action beyond today across all request types.
-   **Exception approvals**: Approvals specifically for exception requests \(e.g., a request to allow delayed patching of a high-risk vulnerability\).
-   **False positive approvals**: Approvals for requests flagged as false positives \(e.g., scanner incorrectly reporting a vulnerability on a host\).
-   **All approvals**: Consolidated list of all approvals, including exception, false positive, risk reduction, and unassignment \(e.g., a single view of everything awaiting your approval\).
-   **Overdue approvals**: Approvals that have crossed their due date \(e.g., a risk reduction request that was supposed to be approved yesterday\).
-   **Expiring exceptions**: Exceptions scheduled to expire within the next 7 days.
-   **Exception extensions**: Deferral extension requests raised after an initial exception request was approved. The initial request may still be in an approved state or may have already expired. This widget covers two scenarios:
    -   An extension request raised directly against an existing finding.
    -   A new vulnerability change approval \(VCA\) created after a previously approved VCA's finding expired. This new request is treated as a continuation of the original exception.
-   **Repeated rejections**: Approvals where a remediation owner has resubmitted a VCA for the same deferral exception after a prior VCA was rejected.

Each approval request contains interactive links that provide access to detailed information, including Record Reference for findings, Request Type, Request Number, Risk Rating, Remediation Status, Approval Assignment Group, and Current State. You can also access click-able links to view details related to associated findings. See [Configure Approval List and Form View](../task/sem-configure-approval-view.md).

When opening a finding record \(e.g., VIT, AVIT, CVIT, Test Results\), users can view detailed attributes such as state, remediation status, assignment group, information about the finding, relevant detections, change approvals, and requested approvals.

You can defer a finding or remediation task directly from its respective form in the Security Exposure Management workspace. Once submitted, the request is sent for approval. This unification offers:

View the requester, purpose, impacted services, approval levels, and comments all in one place.

Approvers can approve or reject requests directly within the same record. See [Reviewing an Approval Request](../task/sem-review-approval-request.md).

Every comment and approval action is recorded and attributed.

You can use generative AI to streamline the approval process for exceptions and false positive requests with AI-driven recommendations. For more information, see: [Approval Recommendation](../../now-assist-vulnerability-response/task/sem-approval-recommendation-skill.md)

All requests including pending, overdue, or completed, are easy to locate and manage in the single view. Links to legacy approval requests are available for items that remain in the old flow during the migration period.

