---
title: Set up your Microsoft Azure account
description: Complete the following setup tasks in your Microsoft Azure portal prior to installing the ServiceNow application for this integration. This account permits access to the Microsoft Exchange Online tenant for email message details.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
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

    2.  Select **Microsoft Entra ID**.

    3.  In the Overview pane that is displayed, select **App registrations**.

    4.  In the App registrations pane that is displayed, select **New registration**.

    5.  Fill in the Register an application form that is displayed.

        |Field|Description|
        |-----|-----------|
        |**Name**|Name for the application. In this example, `ServiceNow Exchange Online Integration` is entered.|
        |**Supported account types**|For this account, in Supported account types, select **Accounts in this organizational directory only \(your organization name\)**. This domain is used for the email searches.|
        |**Redirect URL \(optional\)**|If you enter a value for this field, it is not used by the integration.|

    6.  Select **Register**.

        An Application ID is created. This ID is similar to a user name. You enter this value on the configuration page in the **OAUTH Application ID** field during the configuration step in your ServiceNow AI Platform instance that is described in [Configure the Microsoft Exchange Online integration](msx_configure.md).

    7.  With the Application \(client\) ID displayed in the ServiceNow Exchange Online Integration pane, select **API permissions**.

        ![Application client ID highlighted in the ServiceNow Exchange Online Integration pane in the Microsoft Azure portal.](../image/ms_Azure_Portal_5.png)

    8.  In the ServiceNow Exchange Online Integration - API permissions pane that is displayed, select **Add a Permission**.

    9.  In the Request API permissions pane that is displayed, select **Microsoft Graph**.

    10. In the Request API permissions pane that is displayed, select **Application permissions**.

    11. In the Select Permissions field that is displayed, enter **Mail.ReadWrite** and select the **Mail.ReadWrite** check box.

    12. Select **Add Permissions**.

    13. In the ServiceNow Exchange Online Integration - API permissions pane that is displayed, click **Grant Admin Consent for &lt;your organization name&gt;**.

    14. To confirm the previous API selection \(Microsoft Graph API\) that you entered, click **Confirm**.

    15. In the ServiceNow Exchange Online Integration - Certificates &amp; Secrets pane, select **Certificates &amp; secrets** followed by **New Client secret** \(password\).

    16. In the form that is displayed on the ServiceNow Exchange Online Integration - Certificates &amp; Secrets pane, enter the name for the application in the `Description` field, click an option for expiration, and select **Add**.

        In the Certificates &amp; Secrets pane that is displayed, in the **Client secrets** section, under `Value`, the row is populated with the new client secret \(password\). Save this password in a secure location. After you leave this page, this password value is no longer visible. You enter this password in the **OAUTH Client Secret** field on the configuration page during the configuration step for the integration in your ServiceNow AI Platform instance. The configuration steps for the integration are described in [Configure the Microsoft Exchange Online integration](msx_configure.md).

        ![Secret value highlighted in Microsoft Azure portal.](../image/ms-azure-client-secret.png)

        You have successfully created an application ID for OAuth authentication in the Microsoft Azure portal.


## What to do next

You are ready to set up your ServiceNow AI Platform® instance for the integration.

**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Next topic:**[Install Microsoft Exchange Online application](install-and-configure-ms-exchange-online.md)

