---
title: Create a Google Drive external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-11"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Google Drive external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Google Drive external content connector

Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.

## Before you begin

A source system administrator must have already configured your Google Drive source system to allow access by the Google Drive external content connector. For details on configuring these settings in the source system, see [Configure Google Drive for external content indexing](cfg-gcloud-settings-gdrive-ext-cont-connector.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Google Drive** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Google Drive external content connector.

</td></tr><tr><td>

Workspace domain

</td><td>

Google Workspace domain for your source system, in this format: `https://workspace.example.com`. The Google Drive external content connector crawls eligible shared drives found in this domain.**Note:** The Google Drive external content connector only crawls eligible shared drives from your source system. It doesn't crawl user drives from your source system.

</td></tr><tr><td>

Service account email

</td><td>

Email address for a user account that has permission to access your Google Workspace domain’s user directory. The Google Drive external content connector uses this account to enumerate users and groups of the domain. As an example, you might enter `google.service.account@example.com`.

 If you don't know the email address to use, ask your Google administrator for it.

</td></tr><tr><td>

Service account JSON file

</td><td>

JSON-format private key file for the service account configured in Google Cloud for the Google Drive external content connector. If you don't have this JSON file, ask your Google administrator for it.

</td></tr></tbody>
</table>6.  Save your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection setting entries fails, the system shows an error message. Double-check your connection settings to ensure they're correct.

7.  Once your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for a Google Drive external content connector](configure-crawl-settings-gdrive-ext-cont-connector.md).

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

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a Google Drive external content connector](configure-crawl-settings-gdrive-ext-cont-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[Google Drive external content connector](../concept/google-drive-external-content-connector.md)

