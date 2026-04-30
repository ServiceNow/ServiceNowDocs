---
title: Restrict the Microsoft SharePoint Online sites that External Content Q&amp;A Genius Results can search
description: Define a Microsoft Keyword Query Language \(KQL\) query to restrict the set of Microsoft SharePoint Online sites \(paths\) that External Content Q&amp;A Genius Results can search for documents. Only documents that satisfy your query are eligible for External Content Q&amp;A Genius Result answer generation.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Restrict the Microsoft SharePoint Online sites that External Content Q&amp;A Genius Results can search

Define a Microsoft Keyword Query Language \(KQL\) query to restrict the set of Microsoft SharePoint Online sites \(paths\) that External Content Q&amp;A Genius Results can search for documents. Only documents that satisfy your query are eligible for External Content Q&amp;A Genius Result answer generation.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

Role required: admin

## About this task

By default, External Content Q&amp;A Genius Results search for relevant documents in all sites \(paths\) in your Microsoft SharePoint Online source system. You can restrict the set of sites searched by specifying a Microsoft Keyword Query Language \(KQL\) property restriction query expression as the value for the **sn\_ais\_assist.sharepoint\_search.query\_filter** system property. Only documents from sites that satisfy your property restriction query are eligible for External Content Q&amp;A Genius Result retrieval and answer generation.

To learn more about KQL property restriction queries and the operators they support, see [https://learn.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference](https://learn.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search the list for the **sn\_ais\_assist.sharepoint\_search.query\_filter** system property record.

    -   If the system property record appears in the list, open it in form view by selecting it.
    -   If the system property record does not appear in the list, add it, setting its **Type** to `string`. To learn how to add a new system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).
3.  In the system property record's **Value** field, enter a valid KQL property restriction query expression.

    As an example, suppose your Microsoft SharePoint Online source system is `https://example.sharepoint.com`.

    -   To limit External Content Q&amp;A Genius Result searches to documents in your Marketing and Sales sites, you might enter `path:"https://example.sharepoint.com/teams/Marketing/" path:"https://example.sharepoint.com/teams/Sales/"` as your property restriction query expression.
    -   To prevent External Content Q&amp;A Genius Results from searching documents in your Engineering and QA sites, you might enter `NOT (path:"https://example.sharepoint.com/teams/Engineering/" path:"https://example.sharepoint.com/teams/QA/")` as your query expression.
    **Note:** You can use KQL Boolean and inclusion/exclusion operators to combine multiple property restriction expressions into a complex query expression.

4.  Select **Update**.


## Result

When searching for documents in your Microsoft SharePoint Online source system, External Content Q&amp;A Genius Results apply your property restriction KQL query as a filter. Only documents in sites that satisfy your query are eligible for retrieval and answer generation.

**Parent Topic:**[External Content Q&amp;A Genius Results](../concept/external-content-qna.md)

