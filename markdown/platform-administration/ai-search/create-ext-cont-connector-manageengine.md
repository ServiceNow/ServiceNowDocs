---
title: Create a ManageEngine external content connector
description: Create an external content connector to retrieve searchable content from your ManageEngine source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-11"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ManageEngine external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Create a ManageEngine external content connector

Create an external content connector to retrieve searchable content from your ManageEngine source system.

## Before you begin

A source system administrator must have already configured your ManageEngine source system to allow access by the ManageEngine external content connector. For details on configuring these settings in the source system, see [Configure ManageEngine for external content indexing](configure-manageengine-external-content-indexing.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **ManageEngine** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this ManageEngine external content connector.

</td></tr><tr><td>

Portal URL

</td><td>

URL for your ManageEngine instance. This is typically `https://<organization>.manageengine.com`, where `<organization>` is the name of your organization.If you don't have the portal URL, ask your ManageEngine administrator for it.

</td></tr><tr><td>

Client ID

</td><td>

Client ID for the server-based OAuth 2.0 client application that grants the connector access to your ManageEngine instance.If you don't have the client ID for this application, ask your ManageEngine administrator for it.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret for the server-based OAuth 2.0 client application that grants the connector access to your ManageEngine instance.If you don't have the client secret for this application, ask your ManageEngine administrator for it.

</td></tr></tbody>
</table>6.  Save and validate your connection settings.

    1.  Select **Validate Connection**.

        A Zoho Accounts window reports that the server-based OAuth 2.0 client application is requesting access to information from your ManageEngine instance.

    2.  In the Zoho Accounts window, select the option to allow the OAuth 2.0 client application to access your Zoho account information, then select **Accept**.

        You're redirected to the connector creation page for connection setting validation.

    **Note:** If validation of your connection settings fails, the system shows an error message. Double-check your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that need to be corrected. Provide the information from this message to your source system administrator.

7.  Once your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a ManageEngine external content connector](configure-crawl-settings-manageengine-external-content-connector.md).

9.  On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

10. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content with your new connector, you need to configure and run content crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a ManageEngine external content connector](configure-crawl-settings-manageengine-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[ManageEngine external content connector](../concept/manageengine-external-content-connector.md)

