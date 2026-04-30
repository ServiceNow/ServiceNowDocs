---
title: Create a Microsoft Viva Engage external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Microsoft Viva Engage source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-11"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft Viva Engage external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Create a Microsoft Viva Engage external content connector

Create an external content connector to retrieve searchable content and security principals from your Microsoft Viva Engage source system.

## Before you begin

A source system administrator must have already configured your Microsoft Viva Engage source system to allow access by the Microsoft Viva Engage external content connector. For details on configuring these settings in the source system, see [Configure Microsoft Viva Engage for external content indexing](configure-microsoft-viva-engage-external-content-indexing.md).

You need login credentials for a Microsoft Entra service user account that can grant the Microsoft Viva Engage connector access to your Microsoft Viva Engage tenant.

**Note:** In order for the connector to retrieve searchable content and metadata from a private community in your Microsoft Viva Engage source system, one of these conditions must be true:

-   The service user account is a member of the private community
-   The service user account has the Global Administrator Microsoft Entra role
-   The service user account has the Groups Administrator Microsoft Entra role

To learn more about administrator roles in Microsoft Viva Engage, see the [https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference) resource.

Ensure that you're logged out of all your Microsoft accounts.

**Important:** If you're logged in to a Microsoft account when creating the connector, the connector runs using that account instead of prompting you for your Microsoft Entra service user account credentials. Using a non-service user account may prevent Microsoft Viva Engage content from being searchable in AI Search applications.

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Viva Engage** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Microsoft Viva Engage external content connector.

</td></tr><tr><td>

Authority URL

</td><td>

Authority URL used to log in to your Microsoft Viva Engage source system. The authority URL typically consists of your Microsoft cloud service endpoint URL, possibly followed by organization-specific parameters. Cloud service endpoint URLs include:

-   `https://login.microsoftonline.com/` \(for the Microsoft 365 cloud\)
-   `https://login.microsoftonline.us/` \(for the Microsoft 365 GCC or GCC High cloud or the Microsoft 365 DoD cloud\)
 If you don't know the authority URL to use, ask your Microsoft Viva Engage administrator for it.

</td></tr><tr><td>

Tenant ID

</td><td>

Directory \(tenant\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft Viva Engage instance. If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Directory \(tenant\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Directory \(tenant\) ID** value.

</td></tr><tr><td>

Client ID

</td><td>

Application \(client\) ID for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft Viva Engage instance. If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Overview** and copy this ID from the **Application \(client\) ID** field in the Essentials section.

 If you can't access the OAuth 2.0 application's registration record in the Microsoft Entra admin center, ask your Microsoft Entra administrator for the application's **Application \(client\) ID** value.

</td></tr><tr><td>

Client Secret

</td><td>

Value of the client secret for the OAuth 2.0 application defined in the Microsoft Entra admin center that grants access to your Microsoft Viva Engage instance. If you have access to the OAuth 2.0 application's registration record in the Microsoft Entra admin center, you can navigate to **Manage** &gt; **Certificates &amp; secrets** and copy this value from the appropriate client secret's **Value** field in the Client secrets section.

 If you can't access the OAuth 2.0 application's client secret value in the Microsoft Entra admin center, ask your Microsoft Entra administrator for it.

</td></tr></tbody>
</table>6.  Save and validate your connection settings.

    1.  Select **Validate Connection**.

        ![Microsoft login pop-up window.](../image/ms-sign-in-prompt.png)

        A pop-up window prompts you to sign in with a Microsoft account.

        **Important:** If you don't see the pop-up window, make sure you're signed out of all your Microsoft accounts, then repeat the connector creation procedure.

    2.  Sign in using your Microsoft Entra service user account credentials.

        The connector runs its crawls using permissions from this service user account.

    **Note:** If validation of your connection settings fails, the system shows an error message. Double-check your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that need to be corrected. Provide the information from this message to your source system administrator.

7.  Once your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a Microsoft Viva Engage external content connector](configure-crawl-settings-microsoft-viva-engage-external-content-connector.md).

9.  On the User permission settings page, modify any default user permission settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user permission settings for this connector from the External Content Admin Home page. For details on this procedure and user permission settings, see [Configure user permission settings for an external content connector](configure-user-mapping-settings-external-content-connector.md).

10. On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

11. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content and security principals with your new connector, you need to configure and run content and user mapping crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a Microsoft Viva Engage external content connector](configure-crawl-settings-microsoft-viva-engage-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[Microsoft Viva Engage external content connector](../concept/microsoft-viva-engage-external-content-connector.md)

