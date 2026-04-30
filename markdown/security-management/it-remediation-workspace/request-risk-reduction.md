---
title: Request risk change in the IT Remediation Workspace
description: Starting from v20.0 of Vulnerability Response, you can request for the change in risk for a host vulnerable item or a remediation task in the IT Remediation Workspace.
locale: en-US
release: xanadu
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request risk change in the IT Remediation Workspace

Starting from v20.0 of Vulnerability Response, you can request for the change in risk for a host vulnerable item or a remediation task in the IT Remediation Workspace.

## Before you begin

Role required: sn\_vul.remediation\_owner

## About this task

Starting from v21.0 of Vulnerability Response:

-   You can request risk change for a remediation task if its vulnerability items are associated to a same Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) for which risk change is enabled.
-   You can request risk change for a remediation task with vulnerable items and also application remediation task with application vulnerable items associated to different CVEs if the risk change is enabled for CVEs. With the following message “Select relevant compensating controls for the vulnerabilities managed in the remediation task”

**Note:** The compensating controls feature is available for host vulnerabilities only.

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  On the List page, open a host vulnerable item or a remediation task.

3.  Select the three dots menu and select **Request Exception**.

4.  On the Request Exception pop-up, fill in the fields.

<table id="table_kxh_gh2_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reason

</td><td>

Reason for your exception request. Select Mitigating Control in Place for risk change request.To see how to add new reason choices, see [Define policy reason mapping](../../vulnerability-app-vuln-mgmt/task/define-policy-reason-mapping.md).

</td></tr><tr><td>

Request for Deferral

</td><td>

Differ the record. This field is selected by default.**Note:** This field appears only when the Mitigating Control in Place option is selected in the **Reason** field.

</td></tr><tr><td id="entry-risk-reduction">

Request for Risk Change

</td><td>

Enables you to request for the risk score change.**Note:** This check box appears only when the Mitigating Control in Place option is selected in the **Reason** field.

</td></tr><tr><td>

Current Risk Rating

</td><td>

Current severity of the risk.**Note:** This field appears only when the **Request for Risk Change** check box is selected.

</td></tr><tr><td>

Desired Risk Rating

</td><td>

New risk rating that you want to assign to the record.The highest risk score in this risk rating range is applied to the record when your request is approved.

**Note:** This field appears only when the **Request for Risk Change** check box is selected.

</td></tr><tr><td id="entry-select-controls">

Select Compensating Controls

</td><td>

Reason for your request to reduce the risk rating.

</td></tr><tr><td>

Until

</td><td>

Date on which the deferral or risk reduction request expires.When the exception request expires:

-   The record reverts to the Open state.
-   The compensating controls expire.
-   The calculated score will be in place of a reduced score.


</td></tr><tr><td>

Justification notes

</td><td>

Details that are related to the reason why this request is being made.

</td></tr></tbody>
</table>5.  Select **Request Exception**.

6.  On the Take Questionnaire modal, answer the questions to provide additional information about your request and select **Submit**.

    **Note:** The Take Questionnaire modal appears only when the questionnaire is enabled for exception management. For more information, see [Configure Exception Management for Vulnerability Response](../../vulnerability-response/task/configure-exception-management-settings.md).

    A message appears stating that your request is successfully submitted for approval. A notification is sent to the approver about your request.

    -   If you request for a deferral and risk change:
        -   Two state change approvals \(VCA\#\) are created for deferral and risk reduction.
        -   The state of the record changes to In Review.
    -   If you request for risk change only:
        -   A state change approval \(VCA\#\) is created.
        -   The state doesn't change.
    On approval or rejection of your request, you’ll receive a notification.

    For more information on how the **Until date for risk change** is updated for a remediation task and vulnerable item when a risk change request is approved, see [Impact of the compensating controls on risk score and expiration date](../concept/requesting-approving-risk-reduction.md).


## What to do next

You will receive a notification when your request is approved or rejected by the approver. For more information on the approval process, see [Approve or reject requests in the Vulnerability Manager Workspace](../../vulnerability-response/task/vr-ws-approve-requests.md).

**Related topics**  


[Understanding compensating controls for risk change](../concept/compensating-controls-overview.md)

[Disable or enable risk change for a CVE or TPE](disable-risk-reduction.md)

[Add a compensating control to the library](create-compensatory-control.md)

[Impact of the compensating controls on risk score and expiration date](../concept/requesting-approving-risk-reduction.md)

