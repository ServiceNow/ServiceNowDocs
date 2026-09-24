---
title: Unified Approvals View
description: The approval process in Security Exposure Management for vulnerability and compliance exceptions is unified to simplify workflows, improve visibility, and streamline actions for Approvers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-approval-view.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Unified Approvals View

The approval process in Security Exposure Management for vulnerability and compliance exceptions is unified to simplify workflows, improve visibility, and streamline actions for Approvers.

The Approvals landing page provides a comprehensive view of all approval requests initiated by remediation owners to view specific requests, with navigation widgets such as:

-   **All approvals**: Consolidated list of all approvals, including exception, false positive, risk reduction, and unassignment \(e.g., a single view of everything awaiting your approval\).
-   **Overdue approvals**: Approvals that have crossed their due date \(e.g., a risk reduction request that was supposed to be approved yesterday\).
-   **Pending approvals**: Approvals awaiting action beyond today across all request types.
-   **Today’s approvals**: Approvals due for action today \(e.g., an unassignment request expiring by end of day\).
-   **Exception approvals**: Approvals specifically for exception requests \(e.g., a request to allow delayed patching of a high-risk vulnerability\).
-   **False positive approvals**: Approvals for requests flagged as false positives \(e.g., scanner incorrectly reporting a vulnerability on a host\).
-   **Expiring exceptions**:
-   **Exception extensions**
-   **Repeated rejections**

Each approval request contains interactive links that provide access to detailed information, including Record Reference for findings, Request Type, Request Number, Risk Rating, Remediation Status, Approval Assignment Group, and Current State. You can also access click-able links to view details related to associated findings. See [Configure Approval List and Form View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-configure-approval-view.md).

When opening a finding record \(e.g., VIT, AVIT, CVIT, Test Results\), users can view detailed attributes such as state, remediation status, assignment group, information about the finding, relevant detections, change approvals, and requested approvals.

You can defer a finding or remediation task directly from its respective form in the Security Exposure Management workspace. Once submitted, the request is sent for approval. This unification offers:

View the requester, purpose, impacted services, approval levels, and comments all in one place.

Approvers can approve or reject requests directly within the same record. See [Reviewing an Approval Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-review-approval-request.md).

Every comment and approval action is recorded and attributed.

You can use generative AI to streamline the approval process for exceptions and false positive requests with AI-driven recommendations. For more information, see: [Generate approval recommendations with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-approval-recommendation-skill.md)

All requests including pending, overdue, or completed, are easy to locate and manage in the single view. Links to legacy approval requests are available for items that remain in the old flow during the migration period.

Each change approval request includes additional attributes such as **Risk Rating** \(Critical, High, Medium, Low, None\), **Remediation Status** \(No Target, In-flight, Approaching Target, Target Missed, Target Met\), **Decision date**, **Impacted services**, and **Approval levels**. Approvers can also use the bulk approve and reject capability to process multiple eligible approval requests simultaneously.

## Bulk approve or reject requests

From any list view in the Unified Approvals View, approvers can act on multiple requests at once:

1.  Select the checkboxes beside the requests to act on, or use the header checkbox to select all visible requests.
2.  Select **Bulk Approve** or **Bulk Reject** from the action bar at the top of the list.
3.  Optionally, enter a single justification that applies to all selected requests; the justification is recorded against each approval record.
4.  Select **Confirm**. The system processes each request in turn and reports a per-request outcome.

Only requests in the **Requested** state are eligible for bulk action. Requests in other states are skipped and listed in the result panel. If a single request fails \(for example, because the approval rule requires individual approval\), the remaining requests still process; failures do not block the batch.

**Note:** Bulk action runs the same approval logic as individual approvals, including multi-level routing. A request that requires a second-level approval moves to the next level after the bulk action approves the first level.

