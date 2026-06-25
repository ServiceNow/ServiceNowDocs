---
title: Create a Notion external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Notion source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/create-ext-cont-connector-notion.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Notion external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Notion external content connector

Create an external content connector to retrieve searchable content and security principals from your Notion source system.

## Before you begin

A source system administrator must have already configured your Notion source system to allow access by the Notion external content connector. For details on configuring these settings in the source system, see [Configure Notion for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-notion-external-content-indexing.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Notion** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Notion external content connector.

</td></tr><tr><td>

Authentication token

</td><td>

Secret for the internal integration created to allow the connector to access your Notion workspace. If you don't have the internal integration secret, ask your Notion administrator for it.

</td></tr></tbody>
</table>6.  Save your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection setting entries fails, the system shows an error message. Verify your connection settings to ensure they're correct.

7.  After your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a Notion external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-notion-external-content-connector.md).

9.  On the User permission settings page, modify any default user permission settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user permission settings for this connector from the External Content Admin Home page. For details on this procedure and user permission settings, see [Configure user permission settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md).

10. On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

11. On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

    When you link a connector search source to a search profile in this step, the system automatically publishes the search profile to make the new link take effect.


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content and security principals with your new connector, you must configure and run content and user mapping crawls for it. You can modify your new connector's crawl settings and create crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a Notion external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-notion-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md).

**Important:** The Notion external content connector doesn't retrieve per-user permissions when running content crawls. All content indexed by the connector is searchable by all mapped users who have access to your configured AI Search experience.

To make content crawled by your new connector searchable in portals and search applications, you must link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

**Parent Topic:**[Notion external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/notion-external-content-connector.md)

