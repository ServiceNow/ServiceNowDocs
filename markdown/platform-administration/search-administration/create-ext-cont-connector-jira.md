---
title: Create an Atlassian Jira Cloud external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Atlassian Jira Cloud source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/create-ext-cont-connector-jira.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Atlassian Jira Cloud external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an Atlassian Jira Cloud external content connector

Create an external content connector to retrieve searchable content and security principals from your Atlassian Jira Cloud source system.

## Before you begin

A source system administrator must have already configured your Atlassian Jira Cloud source system to allow access by the Atlassian Jira Cloud external content connector. For details on configuring these settings in the source system, see [Configure Atlassian Jira Cloud for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-src-sys-settings-jira-ext-cont-connector.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Jira Cloud** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Atlassian Jira Cloud external content connector.

</td></tr><tr><td>

URL

</td><td>

URL for your Atlassian Jira Cloud source system, in this format: `https://jira.example.com`.

</td></tr><tr><td>

API Key

</td><td>

API key from your Atlassian Administration console. If you're not sure how to find the API key in your Atlassian Administration console, ask your Atlassian administrator.

</td></tr><tr><td>

Client ID

</td><td>

Client identifier for the OAuth 2.0 Atlassian developer application that grants Confluence API access to your Atlassian Jira Cloud source system. If you're not sure how to find the Client ID for the OAuth 2.0 application in your Atlassian developer console, ask your Atlassian administrator.

</td></tr><tr><td>

Client Secret

</td><td>

OAuth 2.0 client secret for the OAuth 2.0 Atlassian developer application that grants Jira API access to your Atlassian Jira Cloud source system. If you're not sure how to find the Client Secret for the OAuth 2.0 application in your Atlassian developer console, ask your Atlassian administrator.

</td></tr></tbody>
</table>6.  Save and validate your connection settings.

    1.  Select **Validate Connection**.

        A pop-up window reports that the connector is requesting access to your Atlassian account.

    2.  In the **Use app on** field of the pop-up window, select the site that you specified the URL for in step [5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-jira.md), then select **Accept**.

        \[Omitted image "jira-cloud-requesting-access-account.png"\] Alt text: Pop-up window showing Atlassian account access request from connector.

    **Note:** If validation of your connection settings fails, the system shows an error message. Verify your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that must be corrected. Provide the information from this message to your source system administrator.

7.  After your connection settings are validated, select **Next**.

8.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for an Atlassian Jira Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-jira-ext-cont-connector.md).

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

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for an Atlassian Jira Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-jira-ext-cont-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you must link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

**Parent Topic:**[Atlassian Jira Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/atlassian-jira-cloud-external-content-connector.md)

