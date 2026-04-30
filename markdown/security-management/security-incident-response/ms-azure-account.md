---
title: Set up your Microsoft Azure account
description: Complete the following setup tasks in your Microsoft Azure portal prior to installing the ServiceNow application for this integration. This account permits access to the Microsoft Exchange Online tenant for email message details.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your Microsoft Azure account

Complete the following setup tasks in your Microsoft Azure portal prior to installing the ServiceNow application for this integration. This account permits access to the Microsoft Exchange Online tenant for email message details.

## Before you begin

Role required: Microsoft Azure portal administrator

This account is required to access the Microsoft Exchange Online tenant to gather additional email message details and to delete email messages. This account is set up in the Microsoft Azure portal.

The images in the following tasks are privileged and proprietary and are used with permission from Microsoft. This content is subject to updates by Microsoft. To verify that you have access to the most current content, see the [Microsoft doc](https://docs.microsoft.com) website.

In the following images, `ServiceNow Inc.` is displayed for the account name in the examples for the Azure portal. In your Azure portal account, the company name for your account in the Azure portal is displayed.

## Procedure

1.  If you have not created an application ID for OAUTH authentication in the Microsoft Azure portal, follow these steps.

    1.  Log in to the Microsoft Azure portal using your Azure portal administrator credentials.

    2.  Enter **App registrations** in the **Search** box.

    3.  Select **New registration**.

    4.  Fill in the Register an application form that is displayed.

        |Field|Description|
        |-----|-----------|
        |**Name**|Name for the application. In this example, `ServiceNow Exchange Online Integration` is entered.|
        |**Supported account types**|For this account, in Supported account types, select **Accounts in this organizational directory only \(your organization name\)**. This domain is used for the email searches.|
        |**Redirect URL \(optional\)**|If you enter a value for this field, it is not used by the integration.|

    5.  Select **Register**.

        An Application ID is created. This ID is similar to a user name. You enter this value on the configuration page in the **OAUTH Application ID** field during the configuration step in your ServiceNow AI Platform instance that is described in [Configure the Microsoft Exchange Online integration](msx_configure.md).

    6.  Under **Manage** select, **Manifest**.

    7.  Find the **requiredResourceAccess** entry \(on or about line 52\).

    8.  Modify **resourceAppId**, **resourceAccess id**, and **resourceAccess type** values with the following code snippet:

        ![Code snippit.](../image/code-snippet.png)

    9.  Select **Save**.

    10. Under **Manage** select, **API permissions**.

    11. Select **Add a Permission**.

    12. In the Request API permissions pane that is displayed, select **Microsoft Graph**.

    13. In the Request API permissions pane that is displayed, select **Application permissions**.

    14. In the Select Permissions field that is displayed, enter **Threat** and select the **ThreatHunting.Read.All** check box.

    15. Select **Grant Admin Consent for &lt;Organization&gt;**.

    16. Select **Yes**.

        The **Status** value should now be **Granted for &lt;Organization&gt;**.![Grant admin consent.](../image/ms-exchange-admin-consent.png)


## What to do next

You are ready to set up your ServiceNow AI Platform® instance for the integration.

**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Next topic:**[Install Microsoft Exchange Online application](install-and-configure-ms-exchange-online.md)

