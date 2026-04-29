---
title: Review crawl history for an external content connector
description: View crawl history records for an external content connector. Drill into a crawl history record to see metrics and alerts for the crawl in question.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Review, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review crawl history for an external content connector

View crawl history records for an external content connector. Drill into a crawl history record to see metrics and alerts for the crawl in question.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

The crawl history page for an external content connector shows a crawl history record for each crawl run by the connector.

You can select an individual crawl history record to examine a crawl in more detail, viewing counts of items found, discovered, and updated as well as performance data and a list of any alerts encountered during the crawl.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector that you want to review crawl history for.

3.  In the connector editor, select the **Crawl history** tab.

    The Crawl history section shows a record for each crawl run for the connector in the last 30 days.

4.  To view more detailed metrics and alert messages for a specific crawl, select the crawl history record for that crawl.

    On the Crawl details page, the About this crawl header section reports the crawl's status, its scope \(full or partial\), its cadence \(whether it was scheduled or a one-time crawl\), its start and end times and duration, and the ID of the user who started it.For a partial crawl, this section also shows a link with the label of the chosen start point. Selecting this link displays the record for the start point, showing its ID as well as its label.

    The Statistics tab shows details about items encountered during the crawl.

    -   For content crawls, this tab shows document statistics and crawl speed in documents per second. For explanations of these document statistics, see [Statistics for external content connector content crawls](../reference/document-statistics-external-content-connectors.md).
    -   For user permission crawls, this tab shows permission statistics and crawl speed in users per second. For explanations of these permission statistics, see [Statistics for external content connector user permission crawls](../reference/permission-statistics-external-content-connectors.md).
5.  To view entries for any alerts encountered during the crawl, navigate to the Alerts tab.

    Alerts include informational, debugging, warning, and error events logged by the connector during its crawl.

    Each alert entry includes a type and a scope. The alert type indicates the importance of the recorded event, as follows.

    -   **Debugging**

        A debugging alert provides detailed insights into the connector's behavior during a crawl.

    -   **Informational**

        An informational alert indicates the successful operation of connector functionality during a crawl.

    -   **Warning**

        A warning alert indicates that the connector encountered an unusual behavior or potentially problematic issue during a crawl.

    -   **Error**

        An error alert indicates that the connector encountered a problem that disrupted its functionality during a crawl.

    The alert scope indicates what the recorded event affected.

    -   **Single**

        The event affected a single content item retrieved by the connector crawl.

    -   **Multiple**

        The event affected multiple content items retrieved by the connector crawl.

    -   **All**

        The event affected all content items retrieved by the connector crawl.

    -   **Crawl**

        The event affected the crawl job for the connector crawl.

6.  To view details for an alert, select the **View Details** link for that alert entry.


**Parent Topic:**[Reviewing external content connector crawl results and analytics](../concept/reviewing-external-content-connector-results-and-analytics.md)

