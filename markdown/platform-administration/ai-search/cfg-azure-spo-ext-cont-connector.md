---
title: Configure Microsoft SharePoint Online for external content indexing
description: Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft SharePoint Online external content connector to access your Microsoft SharePoint Online source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Microsoft SharePoint Online for external content indexing

Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft SharePoint Online external content connector to access your Microsoft SharePoint Online source system.

## Before you begin

You need the following credentials and permissions for your organization in the Microsoft Entra admin center:

-   Login credentials
-   Permission to register an application
-   Permission to add API permissions to an application
-   Permission to grant admin consent for an application's API permissions
-   Permission to upload certificates for an application

You must have created a public/private key pair for the Microsoft SharePoint Online external content connector and extracted the public key certificate in DER-encoded binary X.509 format. For details on creating the public/private key pair and extracting the public key certificate, see [Create a public/private key pair for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/gen-cert-spo-ext-cont-connector.md).

Role required: none

## About this task

The Microsoft SharePoint Online external content connector retrieves content from your Microsoft SharePoint Online source system using Microsoft Graph and the Microsoft SharePoint REST APIs.

To enable the connector to access your Microsoft SharePoint Online source system via these APIs, you must configure an OAuth 2.0 application in the Microsoft Entra admin center. Your connector administrator can use settings copied from this Microsoft Entra application to configure the Microsoft SharePoint Online external content connector for proper connection to your Microsoft SharePoint Online source system.

## Procedure

1.  Register a new application in the Microsoft Entra admin center.

    1.  Log in to the Microsoft Entra admin center at [https://entra.microsoft.com/](https://entra.microsoft.com/).

        **Note:** If your Microsoft SharePoint Online tenant is in the Microsoft 365 GCC or GCC High cloud or the Microsoft 365 DoD cloud, log in at [https://entra.microsoft.us/](https://entra.microsoft.us/) instead.

    2.  Select **Applications** &gt; **App registrations**.

    3.  On the App registrations page, select **New registration**.

        \[Omitted image "ms-entra-home-app-registrations.png"\] Alt text: App registrations page in Microsoft Entra admin center with New registration link.

    4.  On the Register an application form, fill in the following fields:

        |Field|Instructions|
        |-----|------------|
        |Name|Enter a unique name for your OAuth 2.0 application. For example, you might enter `Microsoft SharePoint Online external content connector`.|
        |Supported account types|Select **Accounts in this organizational directory only \(&lt;instance-name&gt; only - Single tenant\)**, where `<instance-name>` is the name of your Microsoft Entra instance.|
        |Redirect URI \(optional\)|Leave this field empty.|

        \[Omitted image "ms-sharepoint-online-entra-register-application.png"\] Alt text: Register an application dialog box in Microsoft Entra admin center.

    5.  Select **Register**.

        The new application's Overview page appears.

2.  Record the values of the **Application \(client\) ID** and **Directory \(tenant\) ID** properties in a secure location.

    \[Omitted image "ms-sharepoint-online-entra-app-overview.png"\] Alt text: Application's overview page in Microsoft Entra admin center showing application/client and directory/tenant ID values.

    **Important:** Your connector administrator needs the application's tenant and client IDs to configure a Microsoft SharePoint Online external content connector.

3.  Add the API permissions required by the Microsoft SharePoint Online external content connector.

    1.  In the application menu, select **Manage** &gt; **API permissions**.

        \[Omitted image "ms-sharepoint-online-entra-api-permissions-before.png"\] Alt text: Application's API permissions list in Microsoft Entra admin center with Add a permission link.

    2.  Select **Add a permission**, then select **Microsoft Graph**, then select **Application permissions**.

        \[Omitted image "ms-entra-request-api-permissions-ms-graph.png"\] Alt text: Request API permissions dialog box in Microsoft Entra admin center showing Microsoft Graph tile

    3.  For each of the following permissions, enter the permission name into the **Select permissions** search field, then locate and select the option for the permission.

<table id="table_wls_w2k_cjc"><thead><tr><th>

Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GroupMember.Read.All

</td><td>

This permission allows the connector to read group memberships from Microsoft Entra ID.

</td></tr><tr><td>

Sites.Read.All

</td><td>

This permission enables the connector to perform automatic site discovery for crawl configuration and one-time crawls.**Note:** If you plan to specify the sites to crawl manually, don't select this permission. For more information on specifying sites for the connector to crawl, see [Configure crawl settings for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-crawl-settings-spo-ext-cont-connector.md). To learn more about one-time crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-user-mapping-crawl-external-content-connector.md).

</td></tr><tr><td>

User.Read.All

</td><td>

This permission allows the connector to read users from Microsoft Entra ID. User information includes user type and account enablement status.

</td></tr></tbody>
</table>    4.  Select **Add permissions**.

        The new Microsoft Graph permissions appear in the application's Configured permissions list.

    5.  Select **Add a permission**, then select **SharePoint**, then select **Application permissions**.

        \[Omitted image "ms-entra-request-api-permissions-sharepoint.png"\] Alt text: Request API permissions dialog box in Microsoft Entra admin center showing SharePoint tile.

    6.  In the **Select permissions** search field, enter either `Sites.FullControl.All` or `Sites.Selected`, then locate and select the option for the specified permission.

        **Note:** The connector only needs one of these two permissions. Don't select both permissions.

<table id="table_ldc_qnn_djc"><thead><tr><th>

Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sites.FullControl.All

</td><td>

This permission allows the connector to access content and user permissions from all sites and site collections in your Microsoft SharePoint Online tenant.Select this permission if your organization allows it. When you select this permission, no additional configuration is needed.

</td></tr><tr><td>

Sites.Selected

</td><td>

This permission allows the connector to access content and user permissions from individual sites and site collections in your Microsoft SharePoint Online tenant. An administrator must grant FullControl permissions to your registered Microsoft Entra OAuth 2.0 app for each site or site collection that you want the connector to access content from.Select this permission if your organization doesn't permit you to grant Sites.FullControl.All permission to a registered application.

To learn how to grant FullControl permissions for individual sites and site collections to your registered Microsoft Entra OAuth 2.0 app, see [Configure site and site collection access for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-site-collection-access-spo-external-content-connector.md).

</td></tr></tbody>
</table>    7.  Select **Add permissions**.

        The new SharePoint permission appears in the application's Configured permissions list.

    \[Omitted image "ms-sharepoint-online-entra-api-permissions-grant-consent.png"\] Alt text: Application's API permissions list in Microsoft Entra admin center showing Microsoft Graph API permissions and Sites.FullControl.All SharePoint API permission added.

    **Tip:** The SharePoint section of your application's API permissions list will show the entry for the SharePoint API permission that you selected in step [3.f](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.md). The images in this procedure show the Sites.FullControl.All permission, but your application may show the Sites.Selected permission instead.

4.  Grant admin consent for the added API permissions.

    1.  Select **Grant admin consent for &lt;instance-name&gt;**, where `<instance-name>` is the name of your Microsoft Entra instance.

    2.  In the Grant admin consent confirmation dialog box, select **Yes**.

        \[Omitted image "ms-sharepoint-online-entra-api-permissions-after.png"\] Alt text: Application's API permissions list in Microsoft Entra admin center showing admin consent granted for added Microsoft Graph API permissions and Sites.FullControl.All SharePoint API permission.

    The status for the added API permissions changes to `Granted for <instance-name>`, where `<instance-name>` is the name of your Microsoft Entra instance.

5.  Upload your DER-encoded binary X.509 format public key certificate for the Microsoft SharePoint Online external content connector.

    1.  In the Microsoft Entra application menu, select **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **Certificates**, then select **Upload certificate**.

        \[Omitted image "ms-sharepoint-online-entra-certificates-secrets-before.png"\] Alt text: Application's Certificates &amp; secrets page in Microsoft Entra admin center showing Upload certificate link.

    3.  Select **Select a file** and locate your DER-encoded binary X.509 format public key certificate file, then enter a description for it.

        \[Omitted image "ms-sharepoint-online-entra-upload-certificate.png"\] Alt text: Upload certificate dialog box in Microsoft Entra admin center.

    4.  Select **Add**.

        The DER-encoded binary X.509 format public key certificate appears in the Certificates list.

        **Note:** You can drag the column separators in the Certificates list to view the entire thumbprint SHA1 hash value.

    5.  Copy the certificate's **Thumbprint** SHA1 hash, shown in hexadecimal format, and record it in a secure location.

        \[Omitted image "ms-sharepoint-online-entra-certificates-secrets-after.png"\] Alt text: Application's Certificates &amp; secrets page in Microsoft Entra admin center showing thumbprint SHA1 hash value for uploaded certificate.

        **Important:** Your connector administrator needs the DER-encoded binary X.509 format public key certificate's SHA1 thumbprint hash to configure the Microsoft SharePoint Online external content connector.

    6.  Retain copies of the generated public/private key files and the key password in a secure location.

        **Note:** You can't download the public key certificate or its password from the Microsoft Entra admin center.


## What to do next

If you granted Sites.Selected permission instead of Sites.FullControl.All permission in step [3.f](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.md), configure SharePoint API permissions for the site collections you want the Microsoft SharePoint Online connector to be able to crawl. For details on this procedure, see [Configure site and site collection access for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-site-collection-access-spo-external-content-connector.md).

Provide the following items to your connector administrator:

-   The OAuth 2.0 application's tenant ID and client ID that you recorded in step [2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.md).
-   The DER-encoded binary X.509 format public key certificate's SHA1 thumbprint hash in hexadecimal format that you recorded in step [5.e](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.md).

Your connector administrator needs these items to configure a Microsoft SharePoint Online external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online instance.

For details on creating and configuring a Microsoft SharePoint Online external content connector, see [Create a Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-mspo.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/microsoft-sharepoint-online-external-content-connector.md)

