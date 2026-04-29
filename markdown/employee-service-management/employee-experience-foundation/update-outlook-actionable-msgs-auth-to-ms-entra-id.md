---
title: Update Outlook Actionable Messages authentication to Microsoft Entra ID
description: Microsoft will retire External Access Token \(EAT\) authentication for Outlook Actionable Messages on March 31, 2026. Microsoft Entra ID token authentication is required for Outlook Actionable Messages.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using ServiceNow for Microsoft Outlook, ServiceNow for Microsoft Outlook, Unified Employee Experience, Employee Service Management]
---

# Update Outlook Actionable Messages authentication to Microsoft Entra ID

Microsoft will retire External Access Token \(EAT\) authentication for Outlook Actionable Messages on March 31, 2026. Microsoft Entra ID token authentication is required for Outlook Actionable Messages.

## Before you begin

Role required: admin

## About this task

**Warning:** After Microsoft retired External Access Token \(EAT\) authentication for Outlook Actionable Messages on March 31, 2026, actionable messages that rely on EAT will stop working.

To ensure uninterrupted functionality with actionable message, you must migrate to Microsoft Entra ID token authentication and update the Outlook Actionable Messages app registration in your ServiceNow instance.

## Procedure

1.  Complete the Microsoft Entra ID setup for Actionable Messages.

    For more information, refer to [Enabling AAD token of Actionable Messages](https://learn.microsoft.com/en-us/outlook/actionable-messages/enable-entra-token-for-actionable-messages).

    **Important:** If you already have an AM provider with Microsoft, migrate and regenerate the AM provider ID. If you do not have one, generate a new provider ID.

2.  After completing the setup, copy the **App ID Uri** and the **Provider Id \(originator\)**.

    ![App ID URI on the Outlook Actionable App in Microsoft.](../images/outlookactionable-appiduri.png)

    ![Provider ID.](../images/outlookactionable-providerid.png)

3.  On your ServiceNow instance, update the **sn\_ms\_oam.outlookactionable.originator** System property value with the new **Provider Id \(originator\)** copied from Step 2.

4.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

5.  Select **Outlook Actionable**.

6.  On the form, in the **Client ID** field, update the ID with the **App ID Uri** that you copied in Step 2.

7.  In the **OAuth OIDC Provider Configuration** field, open the **Microsoft Office** record.

    On the Microsoft Office OIDC Provider Configuration form, do the following:

    ![Outlook actionable Application Registry form.](../images/outlookactionable-appregistry.png)

    1.  Update the **OIDC Metadata URL** to this format: `https://sts.windows.net/{tenant-id}/.well-known/openid-configuration`.

    2.  Set the **User Claim** field to **upn**.

        ![OIDC Provider form.](../images/outlookactionable-metadaturl.png)

    3.  Save the form.

8.  Save the form.


## Result

You are now migrated to Microsoft Entra ID token authentication and the Outlook Actionable Messages app registration is updated in your ServiceNow instance.

**Parent Topic:**[Using ServiceNow for Microsoft Outlook](../concept/using-sn-ms-outlook.md)

