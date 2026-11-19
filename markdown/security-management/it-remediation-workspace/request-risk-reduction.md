---
title: Request a risk modification for a vulnerable item or remediation task
description: Request a risk modification for a host vulnerable item or a remediation task in the IT Remediation Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/it-remediation-workspace/request-risk-reduction.html
release: zurich
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 3
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request a risk modification for a vulnerable item or remediation task

Request a risk modification for a host vulnerable item or a remediation task in the IT Remediation Workspace.

## Before you begin

Role required: sn\_vul.remediation\_owner

## About this task

Starting from v21.0 of Vulnerability Response, you can request risk reduction only for the following items:

-   A remediation task only if all its vulnerable items are associated to the same Common Vulnerability Entry \(CVE\) regardless of whether its risk reduction is enabled for CVEs.
-   A third-party \(TPE\) for which risk reduction is enabled.

**Note:** The compensating controls feature is available for host vulnerabilities only.

A remediation task can include vulnerable items associated with more than one CVE or TPE. If risk change is restricted for some of those CVEs or TPEs, you can still request risk reduction for the eligible vulnerable items. The **Request risk modification** form shows how many of the selected items are eligible for risk change. If none of the selected items are eligible, the form states that risk change is restricted and the request can't proceed.

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  Select the List icon \(\[Omitted image "listview-icon.png"\] Alt text: List icon\).

3.  On the List page, open a host vulnerable item or a remediation task.

4.  Select the More options icon and select **Request risk modification**.

5.  On the **Request risk modification** form, fill in the fields.

    For a description of the field values, see [Modify risk and Request risk modification form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-modify-risk-form.md).

6.  Select **Submit request**.

    **Note:** No questionnaire is required, even if a questionnaire is configured for exception requests. If you previously relied on a questionnaire configured for exception requests on the **Mitigating Control in Place** reason to gather this information for risk modification, that questionnaire no longer appears for new risk modification requests. In case you must modify your questionnaire, refer to KB2713229.


## Result

A message appears stating that your request is successfully submitted for approval. A notification is sent to the approver about your request. A state change approval \(VCA\#\) record is created. The state of the record doesn't change until the request is approved.

On approval or rejection of your request, you'll receive a notification. For more information on the approval process, see [Approve or reject requests in the Vulnerability Manager Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/vr-ws-approve-requests.md).

For more information on how the **Until date for risk reduction** is updated for a remediation task and vulnerable item when a risk reduction request is approved, see [Impact of the compensating controls on risk score and expiration date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/requesting-approving-risk-reduction.md).

**Related topics**  


[Understanding compensating controls for risk reduction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/compensating-controls-overview.md)

[Restrict or enable risk change for a CVE or TPE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/disable-risk-reduction.md)

[Add a compensating control to the library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/create-compensatory-control.md)

[Impact of the compensating controls on risk score and expiration date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-manager-workspace/requesting-approving-risk-reduction.md)

