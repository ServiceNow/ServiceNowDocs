---
title: Estimate document volume for Microsoft SharePoint Online
description: Estimate the total number of documents included in your Microsoft SharePoint Online source system and the document counts for individual sites. Use this information to determine crawl scope settings needed for your Microsoft SharePoint Online external content connector.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Estimate document volume for Microsoft SharePoint Online

Estimate the total number of documents included in your Microsoft SharePoint Online source system and the document counts for individual sites. Use this information to determine crawl scope settings needed for your Microsoft SharePoint Online external content connector.

## Before you begin

You need the following credentials and permissions for your organization's Microsoft 365 admin center instance:

-   Login credentials
-   Permission to configure and export the Microsoft SharePoint Online active site listing

For detailed information about access to reports in the Microsoft 365 admin center, see the [Microsoft 365 reports in the admin center](https://learn.microsoft.com/en-us/microsoft-365/admin/activity-reports/activity-reports) article on the Microsoft Learn site.

Role required: none

## About this task

Before configuring a Microsoft SharePoint Online external content connector, you may find it helpful to estimate the number of documents available in your Microsoft SharePoint Online source system and in its individual sites.

By estimating the count of available documents, you can determine whether you need to restrict the crawl scope for your Microsoft SharePoint Online external content connector to avoid exceeding the indexed-document limit.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Log in to the Microsoft 365 admin center at [https://admin.microsoft.com/](https://admin.microsoft.com/).

2.  Navigate to **Admin centers** &gt; **All admin centers**, then select **SharePoint** in the list of admin centers.

3.  Navigate to **Sites** &gt; **Active sites**.

4.  In the Active sites list, select the **Customize columns** header, ensure that the following columns are selected for display, then select **Apply**.

    -   Site name
    -   URL
    -   Storage used \(GB\)
    -   Files
5.  Export and analyze the document counts for active sites.

    1.  Select **Export**.

    2.  When prompted, save the active sites CSV list to a convenient location.

    3.  Open the exported active sites CSV list in a tool of your choice.

    4.  For each site entry in the active sites list, find the number of available documents in the Files field.

        Use the Site name and URL field values to identify your sites.

    5.  Find the total number of available documents in your Microsoft SharePoint Online source system by adding up the Files field values for all the sites in the active sites CSV list.


## What to do next

If your Microsoft SharePoint Online source system's total available document count exceeds the connector limit of ten million \(10,000,000\) documents, you will need to limit the crawl scope for the Microsoft SharePoint Online external content connector. Choose a set of sites whose total document count is less than the connector limit, and inform your AI Search administrator so they can configure the external content connector's crawl settings to include only those sites.

For details on configuring the Microsoft SharePoint Online connector's crawl settings, see [Configure crawl settings for the Microsoft SharePoint Online external content connector](configure-crawl-settings-spo-ext-cont-connector.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

