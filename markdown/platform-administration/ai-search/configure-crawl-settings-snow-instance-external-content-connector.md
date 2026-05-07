---
title: Configure crawl settings for a ServiceNow instance external content connector
description: Specify the content types that you want your ServiceNow instance external content connector to retrieve when running content crawls.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow instance external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a ServiceNow instance external content connector

Specify the content types that you want your ServiceNow instance external content connector to retrieve when running content crawls.

## Before you begin

A connector admin must have already created the ServiceNow® instance external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a ServiceNow instance external content connector](create-ext-cont-connector-snow-instance.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the ServiceNow instance external content connector retrieves all KB articles from your ServiceNow AI Platform instance. You only need to perform this task if you want the connector to use inclusion or exclusion filters for the KB articles to retrieve when running content crawls.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need a connector to index more than 10,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the ServiceNow instance external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Short description filtering** options in the KB articles section.

    -   To crawl all KB articles from the source instance, select **Crawl all short descriptions**.
    -   To crawl only a specified set of KB articles from the source instance, select **Include only these short descriptions**, then use the **Add short description patterns to include** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the KB articles that you want to include in the crawl.

        As an example, you might enter `Beginner's [Gg]uide` to include all KB articles with short descriptions that contain the terms `Beginner's Guide` or `Beginner's guide`.

    -   To crawl all except a specified set of KB articles from the source instance, select **Exclude only these short descriptions**, then use the **Add short description patterns to exclude** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the KB articles that you want to exclude from the crawl.

        As an example, you might enter `(?i)\[Legacy\]` to exclude all KB articles with short descriptions that contain the terms `[Legacy]` or `[legacy]`.

    **Note:** To learn about Java regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

5.  Select **Save and validate**.


## Result

The ServiceNow instance external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your ServiceNow AI Platform instance using your modified crawl settings, create and run a one-time content crawl for your ServiceNow instance external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[ServiceNow instance external content connector](../concept/servicenow-instance-external-content-connector.md)

