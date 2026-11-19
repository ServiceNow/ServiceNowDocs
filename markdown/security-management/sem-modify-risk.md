---
title: Modify the risk rating for a finding or remediation task
description: Change the risk rating for a host vulnerable item, application vulnerable item, container vulnerable item, or remediation task in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/sem-modify-risk.html
release: zurich
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Modify the risk rating for a finding or remediation task

Change the risk rating for a host vulnerable item, application vulnerable item, container vulnerable item, or remediation task in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   Host vulnerable items \(VITs\): sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner
-   Application vulnerable items \(AVITs\): sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion
-   Container vulnerable items \(CVITs\): sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner

## About this task

You can modify the risk rating for individual findings and remediation tasks \(VUL, AVUL, or CVUL\). This action isn't available for Configuration Compliance test results or test result groups. Only findings in the **Open**, **Under Investigation**, or **Awaiting Implementation** state are considered for risk change.

Risk modification is separate from requesting an exception. You don't need to complete a questionnaire, even if one is configured for exception requests. Associating a compensating control with the risk change is optional.

If you're a Vulnerability Admin, the risk rating updates immediately. If you're a Remediation Owner, your request requires approval before the risk rating updates.

**Note:** You can't change a finding's risk rating if its underlying vulnerability restricts risk changes. Resolve the restriction before proceeding. See [Disable or enable risk reduction for a CVE or TPE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-disable-risk-reduction.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **List**.

2.  Open the finding or remediation task whose risk rating you want to change.

3.  Select **Modify risk** from \[Omitted image "more-action-menu.png"\] Alt text: more optionmore option.

    **Note:** If you're a Remediation Owner, select **Request Risk Modification**.

4.  Complete the fields in the dialog.

    See [Modify risk and Request risk modification form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-modify-risk-form.md) for more information on the fields.

5.  Select **Apply**.


## Result

If you're a Vulnerability admin or an analyst, the risk rating updates immediately and a confirmation message appears.

If you're a Remediation Owner, a risk modification request is submitted for approval. The risk rating updates to your selected value only after the request is approved.

**Note:** The sn\_sec\_exception.modify\_risk\_approval\_required system property controls whether a Remediation Owner request requires approval. This property is set to true by default. If set to false, the change approval moves directly to **Approved** and the risk rating updates immediately for Remediation Owners too.

-   **[Modify risk and Request risk modification form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-modify-risk-form.md)**  
The following table shows the fields on the **Modify risk** and **Request risk modification** dialogs.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/using-unified-security-exposure-management.md)

**Related topics**  


[Request bulk exception in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-bulk-edit-request-exception.md)

[Add a compensating control to the library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-create-compensatory-control.md)

[Approve or reject requests in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-approve-requests.md)

