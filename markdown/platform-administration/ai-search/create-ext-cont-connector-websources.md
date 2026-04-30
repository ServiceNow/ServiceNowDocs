---
title: Create a predefined web sources external content connector
description: Create an external content connector to retrieve searchable content from pages and subdomains in a predefined public web source system.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 2
breadcrumb: [Creating external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a predefined web sources external content connector

Create an external content connector to retrieve searchable content from pages and subdomains in a predefined public web source system.

## Before you begin

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Predefined web sources** tile, then select **Next**.

5.  On the Connector details page, select the predefined web source that you want to retrieve searchable content from.

6.  Select **Save and validate**.

    **Note:** If validation fails, an error message appears. Double-check your connection settings to ensure they're correct.


## Result

Your new predefined web sources external content connector appears in the Connectors section.

## What to do next

You can optionally define crawl settings for your new predefined web sources external content connector. Using these settings, you can limit the set of pages and subdomains you want the connector to crawl. To learn how to configure the connector's crawl settings, see [Configure crawl settings for the predefined web sources external content connector](configure-crawl-settings-websources-ext-cont-connector.md).

If you want the connector to crawl everything in the source system, and don't want to apply file-extension inclusion or exclusion filters, you can skip definition of crawl settings and go straight on to run one-time crawls for your new connector. To learn about running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md). The connector automatically runs document crawls on a monthly schedule.

You can create search sources for the connector's indexed source and link them to your search profiles. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](../concept/search-sources-ais.md).

**Parent Topic:**[Creating external content connectors](creating-ext-cont-connectors.md)

