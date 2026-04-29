---
title: Create a Microsoft SharePoint Online external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Microsoft SharePoint Online external content connector

Create an external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online source system.

## Before you begin

A source system administrator must have already configured your Microsoft SharePoint Online source system to allow access by the Microsoft SharePoint Online external content connector. For details on configuring these settings in the source system, see [Create a public/private key pair for the Microsoft SharePoint Online external content connector](gen-cert-spo-ext-cont-connector.md) and [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **SharePoint Online** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_bvk_jcd_t2c"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Microsoft SharePoint Online external content connector.

</td></tr><tr><td>

Application \(client\) ID

</td><td>

Application \(client\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft SharePoint Online source system. If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Application \(client\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Application \(client\) ID** value.

</td></tr><tr><td>

Directory \(tenant\) ID

</td><td>

Directory \(tenant\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft SharePoint Online source system. If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Directory \(tenant\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Directory \(tenant\) ID** value.

</td></tr><tr><td>

JKS Certificate

</td><td>

Java KeyStore \(JKS\) file containing a public/private key pair generated with the Java keytool utility. These keys must match the public key from the DER-encoded binary X.509 format certificate uploaded to the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data. If you don't have a copy of the JKS file, ask your security administrator for it. You can't download the JKS file from the OAuth 2.0 application's registration record in the Microsoft Entra portal.

</td></tr><tr><td>

JKS certificate password

</td><td>

Password for the Java KeyStore \(JKS\) file specified in **JKS Certificate**. If you don't have the password for the JKS file, ask your security administrator for it. You can't retrieve the JKS certificate password from the registration record for the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data.

</td></tr><tr><td>

JKS certificate thumbprint

</td><td>

Base64-encoded or hexadecimal SHA1 hash for the DER-encoded binary X.509 format public key certificate uploaded to the OAuth 2.0 application defined in the Microsoft Entra admin center that allows the Microsoft SharePoint Online external content connector to access your source system data. If you don't have this hash, ask your Microsoft Entra administrator for the SHA1 thumbprint hash for the application's DER-encoded binary X.509 format public key certificate, in either base64-encoded or hexadecimal format.

</td></tr><tr class="sub-head"><td colspan="2">

Settings for regulated markets

</td></tr><tr><td>

Configure settings for regulated markets

</td><td>

Option to display **Authority endpoint** and **Graph API endpoint** settings fields.

</td></tr><tr><td>

Authority endpoint

</td><td>

URL for the Microsoft authorization server that you use to log in to your source system \(Microsoft tenant\). This field appears only when **Configure settings for regulated markets** is selected.

 Default value: `https://login.microsoftonline.com/`

 Cloud service endpoint URLs include:

-   `https://login.microsoftonline.com/`: Endpoint URL for the Microsoft 365 cloud
-   `https://login.microsoftonline.us/`: Endpoint URL for the Microsoft 365 GCC and GCC High cloud and the Microsoft 365 DoD cloud
 If you don't know the authority endpoint URL to use, ask your Microsoft administrator for it.

**Important:** The authority endpoint URL must end with a trailing slash.

</td></tr><tr><td>

Graph API endpoint

</td><td>

Microsoft Graph API endpoint for your source system \(Microsoft tenant\). This field appears only when **Configure settings for regulated markets** is selected.

 Default value: `https://graph.microsoftonline.com/`

 Microsoft Graph API endpoint URLs include:

-   `https://graph.microsoftonline.com/`: Endpoint URL for the Microsoft Graph global service cloud
-   `https://graph.microsoftonline.us/`: Endpoint URL for the Microsoft Graph for US Government L4 cloud
-   `https://dod-graph.microsoftonline.us/`: Endpoint URL for Microsoft Graph for US Government L5 \(DOD\) cloud
 If you don't know the Microsoft Graph API endpoint URL to use, ask your Microsoft administrator for it.

**Important:** The Microsoft Graph API endpoint URL must end with a trailing slash.

</td></tr><tr><td>

Validate connection settings with test crawl

</td><td>

Option to run a short test crawl to verify whether your connection settings and source system permissions are correctly set.

 For more details on validating connection settings and source system permissions with a test crawl, see [Verify your connection settings and source system permissions for an external content connector](verify-connection-settings-ext-cont-connector.md).

**Important:** For connectors that support user permission crawls, all searchable content and metadata indexed by the validation test crawl is public until the connector completes its first user permission crawl. This means the test crawl's content will be visible to all users of portals and search applications that the connector is linked to.

</td></tr></tbody>
</table>    **Note:** The **Settings for regulated markets** connection settings aren't shown for Microsoft SharePoint Online connectors that you created in versions of External Content Connectors prior to version 4.0. Starting in External Content Connectors version 4.0, these connection settings are shown when you create a new Microsoft SharePoint Online external content connector.

6.  Save and validate your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection settings fails, the system shows an error message. Double-check your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that need to be corrected. Provide the information from this message to your source system administrator.

7.  Once your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a Microsoft SharePoint Online external content connector](configure-crawl-settings-spo-ext-cont-connector.md).

9.  On the User permission settings page, modify any default user permission settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user permission settings for this connector from the External Content Admin Home page. For details on this procedure and user permission settings, see [Configure user permission settings for an external content connector](configure-user-mapping-settings-external-content-connector.md).

10. On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

11. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

12. Select **Save**.


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content and security principals with your new connector, you need to configure and run content and user mapping crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a Microsoft SharePoint Online external content connector](configure-crawl-settings-spo-ext-cont-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

