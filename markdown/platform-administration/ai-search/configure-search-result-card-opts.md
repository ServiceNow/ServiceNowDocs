---
title: Configure EVAM display settings for search results in AI Search applications
description: Customize display settings for Search Result EVAM \(Entity View Action Mapping\) cards in portal and non-portal AI Search applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure EVAM display settings for search results in AI Search applications

Customize display settings for Search Result EVAM \(Entity View Action Mapping\) cards in portal and non-portal AI Search applications.

## Before you begin

Role required: evam\_admin

## About this task

EVAM administrators can modify settings on Search Result EVAM cards to customize the appearance and layout of search results in AI Search applications.

String fields on Search Result EVAM cards can be populated with literal text or with values from AI Search indexed fields.

## Procedure

1.  Open the EVAM Definition record associated with your chosen AI Search application.

    -   For portal applications, navigate to **All** &gt; **Service Portal** &gt; **Portals**, select the search application's portal record from the list, then use the Preview this record icon ![](../image/icon-preview-this-record.png) to preview and open the portal record's linked Search Results Configuration record.
    -   For non-portal applications, navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**, select the search application's configuration record from the list, then use the Preview this record icon ![](../image/icon-preview-this-record.png) to preview and open the search application configuration record's linked EVAM Definition record.
2.  In the EVAM View Config Bundle M2Ms related list, select the record for the EVAM definition's config bundle.

3.  In the EVAM View Configs list, select the record for the specific Search Result category that you want to customize.

    The record name should include `Search Result`. Don't select a record with `Genius Result` in its name, as Genius Results have different display settings than standard search results do.

4.  Use the Preview this record icon ![](../image/icon-preview-this-record.png) to preview and open the EVAM View Config record's linked View Template record.

5.  In the Template field, edit the JSON for the Search Result card properties you want to customize.

    For details on available properties and their supported values, see [List of Search Result EVAM card properties](../reference/search-result-evam-card-opts.md).

6.  Select **Update**.


## Result

Changes made to Search Result EVAM card settings take effect immediately in AI Search applications.

-   **[List of Search Result EVAM card properties](../reference/search-result-evam-card-opts.md)**  
You can customize the appearance of standard search results in your AI Search application by changing these properties in the application's Search Result EVAM \(Entity View Action Mapping\) cards.

**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)

