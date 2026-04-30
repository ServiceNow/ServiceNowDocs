---
title: Review crawl history and analytics for an external content connector
description: View crawl history records and analytics for an external content connector. Drill into a crawl history record to see detailed metrics and errors from the crawl in question.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-09-24"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review crawl history and analytics for an external content connector

View crawl history records and analytics for an external content connector. Drill into a crawl history record to see detailed metrics and errors from the crawl in question.

## Before you begin

Role required: ais\_admin

## About this task

The crawl history page for an external content connector shows crawl history records for individual crawls, along with analytics summarizing crawl results from the last 30 days and the connector's total count of external documents fed to AI Search for indexing.

You can select an individual crawl history record to examine a crawl in more detail, with counts of items found, discovered, and updated as well as performance data and lists of errors encountered during the crawl. Additionally, you can view crawl-related messages in the system log or cancel a crawl that's currently running.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector whose crawl history and analytics you want to review.

3.  In the connector editor, select the **Crawl history** tab.

    The Crawl history section shows a record for each crawl run for the connector in the last 30 days. The Analytics section summarizes crawl results from the last 30 days and shows the total count of external documents fed to AI Search for indexing.

4.  To view more detailed metrics and error messages for a specific crawl, select the crawl history record for that crawl.

    The Crawl details page reports the crawl's start and end times, its type, who started it, its status and duration, its processed item and error counts, and its performance data. The Job errors, Item errors, and Misc errors sections show details for any errors encountered during the crawl. A crawl with status **In progress** is currently running.

5.  To cancel a running crawl, select **Cancel** on the Crawl details page, then select **Yes, cancel** in the Cancel crawl dialog box.

    **Note:** Canceling a crawl may take a minute or two. During this time, the connector may continue to retrieve searchable content and security principals and feed them to AI Search.


**Parent Topic:**[Reviewing external content connector crawl results and analytics](../concept/reviewing-external-content-connector-results-and-analytics.md)

