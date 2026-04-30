---
title: Create a Google Drive external content connector
description: Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.
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

# Create a Google Drive external content connector

Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.

## Before you begin

A source system administrator must have already configured your Google Drive source system to allow access by the Google Drive external content connector. For details on configuring these settings in the source system, see [Configure Google Drive for external content indexing](cfg-gcloud-settings-gdrive-ext-cont-connector.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You need to be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **Google Drive** tile, then select **Next**.

5.  On the Connector details page, fill in the required connection settings.

<table id="table_uvz_jrv_sdc"><thead><tr><th>

Connection setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector name

</td><td>

Unique name for this Google Drive external content connector.

</td></tr><tr><td>

Workspace domain

</td><td>

Google Workspace domain for your source system, in this format: `https://workspace.example.com`. The Google Drive external content connector crawls shared drives found in this domain.**Note:** The Google Drive external content connector only crawls shared drives from your source system. It doesn't crawl user drives from your source system.

</td></tr><tr><td>

Service account email

</td><td>

Email address for a user account that has permission to access your Google Workspace domain’s user directory. The Google Drive external content connector uses this account to enumerate users and groups of the domain.

 As an example, you might enter `google.service.account@example.com`.

 If you don't know the email address to use, ask your Google administrator for it.

</td></tr><tr><td>

Service account JSON file

</td><td>

JSON-format private key file for the service account configured in Google Cloud for the Google Drive external content connector.

 If you don't have this JSON file, ask your Google administrator for it.

</td></tr></tbody>
</table>6.  Select **Save and validate**.

    **Note:** If validation fails, an error message appears. Double-check your connection settings to ensure they're correct.


## Result

Your new Google Drive external content connector appears in the Connectors section.

## What to do next

You can optionally define crawl settings for your new Google Drive external content connector. Using these settings, you can limit the set of shared drives you want the connector to crawl, or define the file extensions for documents you want the connector's crawls to include or exclude. To learn how to configure the connector's crawl settings, see [Configure crawl settings for the Google Drive external content connector](configure-crawl-settings-gdrive-ext-cont-connector.md).

If you want the connector to crawl everything in the source system, and don't want to apply file-extension inclusion or exclusion filters, you can skip definition of crawl settings and go straight on to define a crawl schedule for your new connector or run one-time crawls for it. For details on defining a crawl schedule, see [Define a crawl schedule for an external content connector](define-schedule-ext-cont-connector.md). To learn about running one-time crawls, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md) and [Run a one-time user mapping crawl for an external content connector](run-umap-crawl-ext-cont-connector.md).

You can create search sources for the connector's indexed source and link them to your search profiles. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources and linking them to search profiles, see [Search sources in AI Search](../concept/search-sources-ais.md).

**Parent Topic:**[Creating external content connectors](creating-ext-cont-connectors.md)

