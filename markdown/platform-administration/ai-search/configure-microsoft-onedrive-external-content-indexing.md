---
title: Configure Microsoft OneDrive for external content indexing
description: Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft OneDrive external content connector to access your Microsoft OneDrive source system.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft OneDrive external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Microsoft OneDrive for external content indexing

Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft OneDrive external content connector to access your Microsoft OneDrive source system.

## Before you begin

You need the following credentials and permissions for your organization in the Microsoft Entra admin center:

-   Login credentials
-   Permission to register an application
-   Permission to add API permissions to an application
-   Permission to grant admin consent for an application's API permissions
-   Permission to upload certificates for an application

You must have created a public/private key pair for the Microsoft OneDrive external content connector and extracted the public key certificate in DER-encoded binary X.509 format. For details on creating the public/private key pair and extracting the public key certificate, see [Create a public/private key pair for the Microsoft OneDrive external content connector](gen-cert-msod-ext-cont-connector.md).

Role required: none

## About this task

The Microsoft OneDrive external content connector retrieves content from your Microsoft OneDrive source system using the Microsoft Graph API.

To enable the connector to access your Microsoft OneDrive source system via this API, you must configure an OAuth 2.0 application in the Microsoft Entra admin center. Your connector admin can use settings copied from this Microsoft Entra application to configure the Microsoft OneDrive external content connector for proper connection to your Microsoft OneDrive source system.

## Procedure

1.  Register a new application in the Microsoft Entra admin center.

    1.  Log in to the Microsoft Entra admin center at [https://entra.microsoft.com/](https://entra.microsoft.com/).

        **Note:** If your Microsoft OneDrive tenant is in the Microsoft 365 GCC or GCC High cloud or the Microsoft 365 DoD cloud, log in at [https://entra.microsoft.us/](https://entra.microsoft.us/) instead.

    2.  Select **Applications** &gt; **App registrations**.

    3.  On the App registrations page, select **New registration**.

        ![App registrations page in Microsoft Entra admin center with New registration link.](../image/ms-entra-home-app-registrations.png)

    4.  On the Register an application form, fill in the following fields:

        |Field|Instructions|
        |-----|------------|
        |Name|Enter a unique name for your OAuth 2.0 application. For example, you might enter `Microsoft OneDrive external content connector`.|
        |Supported account types|Select **Accounts in this organizational directory only \(&lt;instance-name&gt; only - Single tenant\)**, where `<instance-name>` is the name of your Microsoft Entra instance.|
        |Redirect URI \(optional\)|Leave this field empty.|

        ![Register an application dialog box in Microsoft Entra admin center.](../image/ms-onedrive-entra-register-application.png)

    5.  Select **Register**.

        The new application's Overview page appears.

2.  Record the values of the **Application \(client\) ID** and **Directory \(tenant\) ID** properties in a secure location.

    ![Application's overview page in Microsoft Entra admin center showing application/client and directory/tenant ID values.](../image/ms-onedrive-entra-app-overview.png)

    **Important:** Your connector admin needs the application's tenant and client IDs to configure a Microsoft OneDrive external content connector.

3.  Add the API permissions required by the Microsoft OneDrive external content connector.

    1.  In the application menu, select **Manage** &gt; **API permissions**.

        ![Application's API permissions list in Microsoft Entra admin center with Add a permission link.](../image/ms-onedrive-entra-api-permissions-before.png)

    2.  Select **Add a permission**, then select **Microsoft Graph**, then select **Application permissions**.

        ![Request API permissions dialog box in Microsoft Entra admin center showing Microsoft Graph tile](../image/ms-entra-request-api-permissions-ms-graph.png)

    3.  For each of the following permissions, enter the permission name into the **Select permissions** search field, then locate and select the option for the permission.

        -   Files.Read.All
        -   Group.Read.All or GroupMember.Read.All

            **Note:** Selecting the Group.Read.All permission improves the connector's crawl speed, but it also gives the connector read access to group chats in your Microsoft OneDrive source system. If you don't want the connector to have read access to your group chats, select the GroupMember.Read.All permission instead.

        -   User.Read.All
    4.  Select **Add permissions**.

        The new Microsoft Graph permissions appear in the application's Configured permissions list.

    ![Application's API permissions list in Microsoft Entra admin center showing added permissions needing admin consent.](../image/ms-onedrive-entra-api-permissions-grant-consent.png)

4.  Grant admin consent for the added API permissions.

    1.  Select **Grant admin consent for &lt;instance-name&gt;**, where `<instance-name>` is the name of your Microsoft Entra instance.

    2.  In the Grant admin consent confirmation dialog box, select **Yes**.

        ![Application's API permissions list in Microsoft Entra admin center showing added permissions with admin consent granted.](../image/ms-onedrive-entra-api-permissions-after.png)

    The status for the added API permissions changes to `Granted for <instance-name>`, where `<instance-name>` is the name of your Microsoft Entra instance.

5.  Upload your DER-encoded binary X.509 format public key certificate for the Microsoft OneDrive external content connector.

    1.  In the Microsoft Entra application menu, select **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **Certificates**, then select **Upload certificate**.

        ![Application's Certificates & secrets page in Microsoft Entra admin center showing Upload certificate link.](../image/ms-onedrive-entra-certificates-secrets-before.png)

    3.  Select **Select a file** and locate your DER-encoded binary X.509 format public key certificate file, then enter a description for it.

        ![Upload certificate dialog box in Microsoft Entra admin center.](../image/ms-onedrive-entra-upload-certificate.png)

    4.  Select **Add**.

        The DER-encoded binary X.509 format public key certificate appears in the Certificates list.

        **Note:** You can drag the column separators in the Certificates list to view the entire thumbprint SHA1 hash value.

    5.  Copy the certificate's **Thumbprint** SHA1 hash, shown in hexadecimal format, and record it in a secure location.

        ![Application's Certificates & secrets page in Microsoft Entra admin center showing thumbprint SHA1 hash value for uploaded certificate.](../image/ms-onedrive-entra-certificates-secrets-after.png)

        **Important:** Your connector admin needs the DER-encoded binary X.509 format public key certificate's SHA1 thumbprint hash to configure the Microsoft OneDrive external content connector.

    6.  Retain copies of the generated public/private key files and the key password in a secure location.

        **Note:** You can't download the public key certificate or its password from the Microsoft Entra admin center.


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 application's tenant ID and client ID that you recorded in step [2](configure-microsoft-onedrive-external-content-indexing.md#client-tenant-ids-step).
-   The DER-encoded binary X.509 format public key certificate's SHA1 thumbprint hash in hexadecimal format that you recorded in step [5.e](configure-microsoft-onedrive-external-content-indexing.md#certificate-thumbprint-step).

Your connector admin needs these items to configure a Microsoft OneDrive external content connector to retrieve searchable content and security principals from your Microsoft OneDrive instance.

For details on creating and configuring a Microsoft OneDrive external content connector, see [Create a Microsoft OneDrive external content connector](create-ext-cont-connector-microsoft-onedrive.md).

**Parent Topic:**[Microsoft OneDrive external content connector](../concept/microsoft-onedrive-external-content-connector.md)

