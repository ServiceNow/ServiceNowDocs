---
title: Request risk reduction for a vulnerable item or remediation task
description: Request a reduction in risk for a host vulnerable item or a remediation task in the IT Remediation Workspace.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request risk reduction for a vulnerable item or remediation task

Request a reduction in risk for a host vulnerable item or a remediation task in the IT Remediation Workspace.

## Before you begin

Role required: sn\_vul.remediation\_owner

## About this task

Starting from v21.0 of Vulnerability Response, you can request risk reduction only for the following items:

-   A remediation task only if all its vulnerable items are associated to the same Common Vulnerability Entry \(CVE\) regardless of whether its risk reduction is enabled for CVEs.
-   A third-party \(TPE\) for which risk reduction is enabled.

**Note:** The compensating controls feature is available for host vulnerabilities only.

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  Select the List icon \(![List icon](../../secops-analyst-workspace/image/listview-icon.png)\).

3.  On the List page, open a host vulnerable item or a remediation task.

4.  Select the More options icon and select **Request Exception**.

5.  On the Request Exception form, fill in the fields.

    For a description of the field values, see[Request exception form for risk reduction](../../vr-it-remediation-workspace/reference/itr-ws-request-exception-form-rr.md).

6.  Select **Request Exception**.

7.  If a Take Questionnaire modal is displayed, answer the questions to provide additional information about your request and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the questionnaire is enabled for exception management. For more information, see [Configure Exception Management for Vulnerability Response](../../vulnerability-response/task/configure-exception-management-settings.md).


## Result

A message appears stating that your request is successfully submitted for approval. A notification is sent to the approver about your request.

-   If your request is for a deferral and risk reduction:
    -   Two state change approvals \(VCA\#\) are created for deferral and risk reduction.
    -   The state of the record changes to In Review.
-   If your request is for risk reduction only:
    -   A state change approval \(VCA\#\) is created.
    -   The state doesn't change.

On approval or rejection of your request, you’ll receive a notification. For more information on the approval process, see [Approve or reject requests in the Vulnerability Manager Workspace](../../vulnerability-response/task/vr-ws-approve-requests.md).

For more information on how the **Until date for risk reduction** is updated for a remediation task and vulnerable item when a risk reduction request is approved, see [Impact of the compensating controls on risk score and expiration date](../concept/requesting-approving-risk-reduction.md).

**Related topics**  


[Understanding compensating controls for risk reduction](../concept/compensating-controls-overview.md)

[Disable or enable risk reduction for a CVE or TPE](disable-risk-reduction.md)

[Add a compensating control to the library](create-compensatory-control.md)

[Impact of the compensating controls on risk score and expiration date](../concept/requesting-approving-risk-reduction.md)

