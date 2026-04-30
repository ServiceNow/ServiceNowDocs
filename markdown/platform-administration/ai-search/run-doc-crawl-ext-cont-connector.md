---
title: Run a one-time full or partial document crawl for an external content connector
description: Retrieve document content and metadata from all or part of your external content connector's data source on demand. A document crawl sends retrieved content and metadata to AI Search for indexing, making them available to users of your AI Search applications.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 2
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Run a one-time full or partial document crawl for an external content connector

Retrieve document content and metadata from all or part of your external content connector's data source on demand. A document crawl sends retrieved content and metadata to AI Search for indexing, making them available to users of your AI Search applications.

## Before you begin

Role required: ais\_admin

## About this task

Create a one-time document crawl when you want to retrieve updated document content and metadata from a source system without configuring a scheduled crawl.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  Select the record for the external content connector that you want to run a one-time document crawl for.

3.  Select **Create crawls**, then select **Create one-time crawl**.

4.  In the Crawl settings dialog box, select one of the following document crawl types:

    -   To crawl your entire source system, starting at its root URL, select **Full document crawl**.
    -   To crawl a subset of your source system, starting from a point you specify and only retrieving documents located beneath that starting point, select **Partial document crawl**.
5.  If you selected **Partial document crawl** in step [4](run-doc-crawl-ext-cont-connector.md#select-ext-cont-doc-crawl-type), select **Refresh start points**, wait for the **Select start points** list to populate, then select the point where you want the partial crawl to start.

    **Note:** Refreshing the start point list requires the connector to retrieve data from the source system and may take a minute or two.

6.  Select **Start**.


## Result

The one-time document crawl task is added to the crawl queue and runs when the system has availability.

**Note:** To prevent excessive load on your instance, the External Content Connectors application only allows a maximum of five crawls to run simultaneously, no matter how many connectors you have created. Both content crawls and user permission crawls count against this limit. For best performance, run and schedule your external content connector crawls so that they don't overlap.

You can monitor the one-time crawl's state and results from the Connector list, or examine the external content connector's crawl history to see more details. For instructions for viewing an external content connector's crawl history, see [Review crawl history and analytics for an external content connector](review-crawl-ext-cont-connector.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

