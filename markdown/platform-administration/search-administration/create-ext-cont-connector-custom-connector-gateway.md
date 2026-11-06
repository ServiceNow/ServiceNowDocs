---
title: Create a Custom Connector Gateway external content connector
description: Create a Custom Connector Gateway external content connector to index searchable content and security principals retrieved by your custom connector implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/create-ext-cont-connector-custom-connector-gateway.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-10-21"
reading_time_minutes: 7
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Custom Connector Gateway external content connector

Create a Custom Connector Gateway external content connector to index searchable content and security principals retrieved by your custom connector implementation.

## Before you begin

A custom connector must already be implemented. To learn more about implementing your own custom connector, see [Implementing a custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/implementing-custom-connector.md).

Your ServiceNow AI Platform® instance must have all the required plugins installed and must have the Hermes Messaging Service enabled. For details on configuring your instance to satisfy these prerequisites, see [Configure your ServiceNow AI Platform instance to support the Custom Connector Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-instance-custom-connector-gateway.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

The Custom Connector Gateway external content connector feeds content and security principals retrieved by your custom connector to AI Search for indexing. After you have set up the Custom Connector Gateway connector, you can configure your custom connector to push retrieved data to it using the Custom Connector Gateway API.

If you're creating two or more Custom Connector Gateway connectors in a single instance, consider the following points.

-   **Shared schema and indexed source**

    All Custom Connector Gateway connectors defined in your instance share the same schema and feed their content to the same indexed source. To distinguish individual connectors in your search applications' facet filters, you can create a separate search source for each connector. In each of these search sources, configure a filter condition based on the connector ID. To learn about search sources and their filter conditions, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/search-sources-ais.md).

-   **Per-connector user permission settings**

    Each Custom Connector Gateway connector has its own user permission settings. For details on configuring user permission settings, see [Configure user mapping settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md).

-   **Per-connector analytics, events, and index inspector**

    Each Custom Connector Gateway connector records its own analytics and events. The index inspector tool only shows indexed results for the specific connector you select. To learn about connector analytics and events and the index inspector tool, see [Reviewing external content connector crawl results and analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/reviewing-external-content-connector-results-and-analytics.md).


## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted to switch scope, select **Switch scope** and select the application scope specified in the prompt.

3.  In the Connectors section, select **Create**.

4.  On the Choose source page, select the **Custom Connector Gateway** tile, then select **Next**.

5.  On the Connection settings page, fill in the connection settings.

    |Connection setting|Description|
    |------------------|-----------|
    |Connector name|Unique name for this Custom Connector Gateway external content connector.|
    |I agree to the following disclaimer|Option acknowledging that you're responsible for the implementation, operation, and security of your custom connector.|

6.  Select **Validate connection**.

7.  On the Schema page, perform these steps to extend the default schema used for all Custom Connector Gateway connectors.

    1.  Select **Edit schema table**.

        The Dictionary Entries table list view appears.

    2.  Select **New**.

    3.  On the Dictionary Entry form, fill in the fields.

    4.  Select **Submit**.

        The new custom field appears in the Dictionary Entries table list view.

    5.  Return to the connector creation page and select **Next**.

    To use only fields from the default schema, skip this step \(by selecting **Skip**\). The default schema fields are displayed in the **Default columns** section of the Schema page. If metadata extracted by your custom connector matches one of the existing fields, map it to that field instead of creating a new field. This approach keeps naming consistent between connectors and avoids the overhead of extending the schema table.

    **Note:** All Custom Connector Gateway external content connectors on your instance share a single schema. When making changes to the Custom Connector Gateway schema for a new connector, check that those changes don't affect the behavior of your existing Custom Connector Gateway connectors.

8.  On the User mapping settings page, modify any default user mapping settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user mapping settings for this connector from the External Content Admin Home page. For details on this procedure and user mapping settings, see [Configure user mapping settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md).

9.  On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

    When you link a connector search source to a search profile in this step, the system automatically publishes the search profile to make the new link take effect.


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To feed content and security principals to AI Search for indexing, your custom connector must access the new connector via the Custom Connector Gateway API. To learn about the methods available in this API, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

To make content crawled by your new connector searchable in portals and search applications, you must link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

