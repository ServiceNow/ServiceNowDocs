---
title: Request release email from quarantine
description: Use this feature to release the email that is quarantined from the Microsoft Purview compliance portal.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Request release email from quarantine

Use this feature to release the email that is quarantined from the Microsoft Purview compliance portal.

## Before you begin

By default, the base system provides the **Request email release from quarantine** response option and **MSFT Quarantine Release Response Option Rule** to release the email from quarantine. This default record also has the **Quarantine Release Approval Rule** configured with it to leverage the approval functionality for this action. For more information, see [Create incident response option rules](../../data-loss-prevention/task/configure-end-user-action.md), [Configure response option for your DLP incidents](../../data-loss-prevention/task/configure-response-option-mapping.md), and [Create Approval Rules](../../data-loss-prevention/task/configure-approval-rules.md).

![Default MSFT Quarantine Release Response Option Rule](../../data-loss-prevention/image/dlp-default-incident-response-rule.png "MSFT Quarantine Release Response Option Rule")

![Default MSFT Response Option - Request email release from quarantine](../../data-loss-prevention/image/dlp-msft-default-response-option.png "Default MSFT Response Option")

**Prerequisites**:

1.  Exchange Online PowerShell module need to be installed on the MID server. For more information, see [Install and maintain the Exchange Online PowerShell](https://learn.microsoft.com/en-us/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exchange-online-powershell-module).
2.  The MID server needs to communicate with the Exchange server, which is also a cloud service. Therefore, the MID server requires continuous internet access.

**Note:** If you are using this response option then make sure the mid server is up and running with PowerShell capability. If a mid server is not up and running and doesn't have PowerShell capability then the end user will not be able to select **Request email release from quarantine** action from the DLP Users workspace. For more information, see [Create incident response option rules](../../data-loss-prevention/task/configure-end-user-action.md) and [Configure response option for your DLP incidents](../../data-loss-prevention/task/configure-response-option-mapping.md).

-   If you want a specific MID server from the list then you have to configure the MID app and make it visible in the list, and then at least one MID server which is configured should be up and running from the selected mid applications and should have the Power Shell capability.
-   For you to use the Release from quarantine option, you need API permissions. On the Microsoft API permissions page, verify **Office 365 Exchange Online** &gt; **Exchange.ManageAsApp** is listed and contains the following values:
    -   -   **Type**: **Application**.
-   **Admin consent required**: **Yes**.
-   **Status**: The current incorrect value is **Not granted for &lt;Organization&gt;** for the **Office 365 Exchange Online** &gt; **Exchange.ManageAsApp** entry and change the status value. For further steps on the API permissions, see [Assign API permissions to the application](https://learn.microsoft.com/en-us/powershell/exchange/app-only-auth-powershell-v2?view=exchange-ps#step-2-assign-api-permissions-to-the-application) on the Microsoft documentation site.

    **Note:** This step is required to connect to Exchange online using Service principle.

-   You should also need **Security Administrator** role in Service Principle,
    -   Search for **Microsoft Entra ID roles and Administrators** in Microsoft Azure portal, and add assignment to the registered app \(Service Principle\) and then follow the procedure explained on the Microsoft Documentation on how to [assign a role](https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/pim-how-to-add-role-to-user#assign-a-role).
-   This option is applicable only for Microsoft Exchange incidents which have the **Policy Action** option as **ExQuarantine** on the incident form view.

Role required: End user

The following procedure explains on how to submit this action from the DLP User Workspace.

## Procedure

1.  Navigate to **DLP** &gt; **DLP User Workspace**.

2.  Open any Microsoft Exchange DLP incident.

    Verify that the incident **Policy Action** is set to ExQuarantine.

3.  Click **Respond**.

4.  Select **Request release mail from Quarantine** option from the Response drop down list.

    ![Submit incident response for Microsoft Exchange](../../data-loss-prevention/image/dlp-respond-quarantined-email-release.png "Submit incident response - Request email release from quarantine option")

5.  Click **Submit**.

    **Note:** When an approval rule is configured for this action, the approval flow will be triggered first and after receiving all the approvals, the Request email release from quarantine flow will be triggered and the email will be released from quarantine. The state of the DLP Incident will be updated to **Released from Quarantine** after successful release.


**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

