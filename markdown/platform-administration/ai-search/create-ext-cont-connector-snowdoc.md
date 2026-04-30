---
title: Create a ServiceNow product documentation external content connector
description: Create an external content connector to retrieve searchable content from the ServiceNow product documentation site.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-26"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Creating external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a ServiceNow product documentation external content connector

Create an external content connector to retrieve searchable content from the ServiceNow product documentation site.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **ServiceNow Product Documentation** tile, then select **Next**.

5.  On the Connector details page, fill in the required connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this ServiceNow product documentation external content connector.

</td></tr><tr><td>

Select source

</td><td>

ServiceNow AI Platform® family release to crawl product documentation for.

 Supported values:

-   **Automatically sync to current instance**: Crawl product documentation for the ServiceNow AI Platform family release used by your instance. As an example, if your instance has Yokohama Patch 3 installed, the connector crawls product documentation for the Yokohama family release.
-   **Manually select family version**: Specify a ServiceNow AI Platform family release that you want to crawl product documentation for.


</td></tr><tr><td>

Family version

</td><td>

ServiceNow AI Platform family release that you want to crawl product documentation for. This field appears only when **Manually select family version** is selected from **Family version**.

</td></tr></tbody>
</table>6.  Select **Save and validate**.

    **Note:** If validation fails, an error message appears. Double-check your connection settings to ensure they're correct.

7.  Define and save crawl settings for your new ServiceNow product documentation external content connector.

    You must save the crawl settings for this connector even if you don't make any changes to the default settings. To learn how to configure the connector's crawl settings, see [Configure crawl settings for the ServiceNow product documentation external content connector](configure-crawl-settings-snowdoc-ext-cont-connector.md).


## Result

Your new ServiceNow product documentation external content connector appears in the Connectors section.

## What to do next

You can optionally modify crawl settings for your new ServiceNow product documentation external content connector. Using these settings, you can limit the set of products you want the connector to crawl documentation for. To configure the crawl settings, see the task topic linked in step [7](create-ext-cont-connector-snowdoc.md#configure-crawl-settings).

If you want the connector to crawl everything in the source system, and don't want to apply file-extension inclusion or exclusion filters, you can skip definition of crawl settings and go straight on to run one-time crawls for your new connector. To learn about running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md). The connector automatically runs document crawls on a monthly schedule.

You can create search sources for the connector's indexed source and link them to your search profiles. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](../concept/search-sources-ais.md).

**Parent Topic:**[Creating external content connectors](creating-ext-cont-connectors.md)

