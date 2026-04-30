---
title: Connect an external content connector to a search profile
description: Make results from an external content connector searchable in your portals and search applications by connecting its search sources to your existing search profiles.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-09-15"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Connect an external content connector to a search profile

Make results from an external content connector searchable in your portals and search applications by connecting its search sources to your existing search profiles.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin or admin

## About this task

To make results from an external content connector searchable in a portal or search application, you need to link one of its search sources to the search profile used by that portal or search application. As an example, linking a connector's search source to the **Now Assist in VA** search profile makes filtered content from that connector available in Now Assist in Virtual Agent conversations.

Each external content connector type feeds its crawled results to a unique indexed source. By default, the system creates a search source for each connector type which has no filters and includes all documents from the connector's indexed source. You can define additional search sources for the indexed source with filter sets applied to limit which documents are searchable. To learn more about search sources and filters, see [Search sources in AI Search](../concept/search-sources-ais.md).

Linking an external content connector's search source to a search profile makes crawled content that satisfies the search source's filters searchable in all portals and search applications that use the specified search profile. For more details on search profiles, see [Search profiles in AI Search](../concept/defining-search-profiles-ais.md).

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector with results that you want to make searchable using one or more search profiles.

3.  In the connector editor's Settings tab, select **Manage index**.

4.  In the Connected search profiles section, repeat these steps for each search profile you want to link the selected external content connector to.

    1.  Use the **Select search source** field to select a search source derived from the connector's indexed source.

    2.  Use the **Connect to search profile** field to select the search profile you want to link the selected search source to.

    3.  Select **Add**.

        A new connection entry appears showing your search source and search profile selections.

5.  Select **Save**.


## Result

For each connection you created, content from the selected external content connector search source becomes searchable in portals and search applications that use the selected search profile.

**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

