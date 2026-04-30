---
title: Create an Atlassian Jira Cloud external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Atlassian Jira Cloud source system.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-25"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Creating external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an Atlassian Jira Cloud external content connector

Create an external content connector to retrieve searchable content and security principals from your Atlassian Jira Cloud source system.

## Before you begin

A source system administrator must have already configured your Atlassian Jira Cloud source system to allow access by the Atlassian Jira Cloud external content connector. For details on configuring these settings in the source system, see [Configure Atlassian Jira Cloud for external content indexing](cfg-src-sys-settings-jira-ext-cont-connector.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Jira Cloud** tile, then select **Next**.

5.  On the Connector details page, fill in the required connection settings.

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

Instance ID

</td><td>

Instance ID \(cloud ID\) for your Atlassian Jira Cloud source system.

 If you're not sure how to find the instance ID for your Atlassian Jira Cloud source system, contact your Atlassian administrator.

</td></tr><tr><td>

API Key

</td><td>

API key from your Atlassian Administration console.

 If you're not sure how to find the API key in your Atlassian Administration console, contact your Atlassian administrator.

</td></tr><tr><td>

Client ID

</td><td>

Client identifier for the OAuth 2.0 Atlassian developer application that grants Confluence API access to your Atlassian Jira Cloud source system.

 If you're not sure how to find the Client ID for the OAuth 2.0 application in your Atlassian developer console, contact your Atlassian administrator.

</td></tr><tr><td>

Client Secret

</td><td>

OAuth 2.0 client secret for the OAuth 2.0 Atlassian developer application that grants Jira API access to your Atlassian Jira Cloud source system.

 If you're not sure how to find the Client Secret for the OAuth 2.0 application in your Atlassian developer console, contact your Atlassian administrator.

</td></tr></tbody>
</table>6.  Select **Save and validate**.

    **Note:** If validation fails, an error message appears. Double-check your connection settings to ensure they're correct.


## Result

Your new Atlassian Jira Cloud external content connector appears in the Connectors section.

## What to do next

You can optionally define crawl settings for your new Atlassian Jira Cloud external content connector. Using these settings, you can limit the set of projects you want the connector to crawl, or define the file extensions for documents you want the connector's crawls to include or exclude. To learn how to configure the connector's crawl settings, see [Configure crawl settings for the Atlassian Jira Cloud external content connector](configure-crawl-settings-jira-ext-cont-connector.md).

If you want the connector to crawl everything in the source system, and don't want to apply file-extension inclusion or exclusion filters, you can skip definition of crawl settings and go straight on to define a crawl schedule for your new connector or run one-time crawls for it. For details on defining a crawl schedule, see [Define a crawl schedule for an external content connector](define-schedule-ext-cont-connector.md). To learn about running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md) and [Run a one-time user mapping crawl for an external content connector](run-umap-crawl-ext-cont-connector.md).

You can create search sources for the connector's indexed source and link them to your search profiles. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](../concept/search-sources-ais.md).

**Parent Topic:**[Creating external content connectors](creating-ext-cont-connectors.md)

