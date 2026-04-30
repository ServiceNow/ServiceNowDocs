---
title: Create a Webcrawler external content connector
description: Create an external content connector to retrieve searchable content from pages and subdomains in a public web source system. Select from a list of predefined web sources or specify your own web source.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Webcrawler external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Webcrawler external content connector

Create an external content connector to retrieve searchable content from pages and subdomains in a public web source system. Select from a list of predefined web sources or specify your own web source.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Follow this procedure to create a new Webcrawler connector to retrieve searchable content and metadata from URLs found in a predefined or custom web source.

By default, you can configure up to three Webcrawler connectors for custom web sources. If you need to retrieve items from more than three custom web sources, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the Webcrawler connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Webcrawler** tile, then select **Next**.

5.  On the Connection settings page, specify the web source that you want to retrieve searchable content from.

    -   To retrieve searchable content from a web source in the list of predefined web sources, select the **Predefined web source** tile, then select your desired web source from the list.
    -   To retrieve searchable content from a public web source not included in the list, select the **Custom web source** tile. Enter a name for the connector and the URL for your selected web source, then select the legal disclaimer option.
6.  Save and validate your connection settings by selecting **Validate Connection**.

    **Note:** If validation of your connection settings fails, the system shows an error message. Double-check your connection settings to ensure they're correct. If permissions required by the connector are missing or incorrectly configured in the source system, a warning message appears showing the permissions that need to be corrected. Provide the information from this message to your source system administrator.

7.  On the Crawl settings page, modify any default crawl settings that you want to override for this connector, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the crawl settings for this connector from the External Content Admin Home page. For details on this procedure and the available crawl settings, see [Configure crawl settings for an Atlassian Confluence Cloud external content connector](configure-crawl-settings-cc-ext-cont-connector.md).

8.  On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

9.  On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

The Webcrawler external content connector automatically schedules monthly content crawls to retrieve searchable content from your source system. You can't schedule content crawls for the Webcrawler connector, but you can run one-time content crawls to retrieve updated content ahead of schedule.

You can modify your new connector's crawl settings and create one-time content crawls for it from the External Content Admin Home page even if you skipped these steps during connector creation.

-   To learn how to configure your new connector's crawl settings, see [Configure crawl settings for a Webcrawler external content connector](configure-crawl-settings-webcrawler-external-content-connector.md).
-   For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you need to link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](../concept/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](connect-external-content-connector-search-profile.md).

**Parent Topic:**[Webcrawler external content connector](../concept/webcrawler-external-content-connector.md)

