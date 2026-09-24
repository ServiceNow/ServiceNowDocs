---
title: Employee service center for Vulnerability Response
description: Employee Service Center provides a standardised approval experience and process for Business Unit Heads, Service Owners, and IT Heads, who may not regularly log in to USEM. It enables them to manage approvals from a central location, such as Employee Center Approval Requests, ensuring that requests are routed to the right approvers, decisions are tracked transparently, and actions are completed efficiently. This improves operational efficiency, accountability, and the overall approver experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/employee-center-vr-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Employee service center for Vulnerability Response

Employee Service Center provides a standardised approval experience and process for Business Unit Heads, Service Owners, and IT Heads, who may not regularly log in to USEM. It enables them to manage approvals from a central location, such as Employee Center Approval Requests, ensuring that requests are routed to the right approvers, decisions are tracked transparently, and actions are completed efficiently. This improves operational efficiency, accountability, and the overall approver experience.

This feature enables users to manage and take action on various vulnerability-related approvals directly from the **Employee Service Center** \(ESC\), eliminating the need to navigate to**Vulnerability Response** &gt; **My Approvals**.

The following approval types are displayed within the Employee Service Center:

-   Request exceptions
-   False positives
-   Risk Reduction
-   Unassigned items
-   Extension requests

For Exception Rules:

-   Creation
-   Extension
-   Deletion \(Marked for deletion\)

These approvals are available under the **My Tasks** section for easier access and management. For more information related to employee center visit: [Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-center-landing-page.md)

## How approvers reach a request in the Employee Service Center

Approvers can reach a vulnerability approval in the Employee Service Center from any of three entry points:

-   **Email notification deep-link**

    Every approval-required notification includes a **Review request** link. Selecting the link opens the Employee Service Center directly to the approval form for that request. Authentication is preserved across the deep-link when the approver is already signed in to the ESC.

-   **__My Tasks__ card on the ESC home page**

    The **My Tasks** card surfaces the count of pending vulnerability approvals alongside other approval types. Selecting the card opens a filtered list scoped to the approver's assigned requests; selecting any row opens the request detail page.

-   **Mobile experience \(Now Mobile app\)**

    The same My Tasks list and detail pages are rendered for handheld devices through the Now Mobile app. Approve and reject actions, comments, and Now Assist recommendations are all available on mobile. Bulk approve and bulk reject are *not* supported on mobile and are limited to the desktop ESC.


## Information shown on the request detail page

The request detail page renders the same approval data as the Security Exposure Management Workspace, organized into four tabs designed for approvers who do not regularly log into the workspace:

-   **Approval Status** — current state, decision date \(if any\), the approver's level, and the requester's name.
-   **Request details** — the reason, justification, attached evidence, and the questionnaire response if one was completed.
-   **Impact summary** — impacted services, risk rating, and remediation status, surfaced for non-technical approvers who need a business-context view.
-   **Activity** — comments, work notes, and the audit trail.

The Now Assist recommendation panel, when available, appears in the right rail of the detail page alongside the same content as in the workspace view.

