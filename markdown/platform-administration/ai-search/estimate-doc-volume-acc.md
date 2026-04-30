---
title: Estimate document volume for Atlassian Confluence Cloud
description: Estimate the number of documents included in your Atlassian Confluence Cloud source system. Use this information to determine crawl scope settings needed for your Atlassian Confluence Cloud external content connector.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-02-26"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Estimating document volume for source systems, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Estimate document volume for Atlassian Confluence Cloud

Estimate the number of documents included in your Atlassian Confluence Cloud source system. Use this information to determine crawl scope settings needed for your Atlassian Confluence Cloud external content connector.

## Before you begin

You need the following credentials and permissions for your organization's Atlassian Confluence Cloud source system:

-   Login credentials for an administrator account
-   Permission to create reports

Role required: none

## About this task

Before configuring an Atlassian Confluence Cloud external content connector, you may find it helpful to estimate the number of documents available in your Atlassian Confluence Cloud source system.

By estimating the count of available documents, you can determine whether you need to restrict the crawl scope for your Atlassian Confluence Cloud external content connector to avoid exceeding the indexed-document limit.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Log in to your Atlassian Confluence Cloud administration console using administrator credentials.

    The URL for the Atlassian Confluence Cloud administration console is typically `https://<hostname>.atlassian.net/wiki/admin`, where `<hostname>` is your organization-specific hostname.

2.  In the administration page's menu, navigate to **Settings** &gt; **Data management** &gt; **Space reports**.

3.  Select **Create report** and wait for the new report's **Download** link to appear.

    The report may take a few minutes to generate.

4.  Select the **Download** action for the new report, then save the space report CSV file to a convenient location when prompted.

5.  Open the downloaded space report CSV file in a tool of your choice.

6.  For each space listed in the space report CSV file, find the number of available documents in the space by adding its listed Content Count and Attachments figures.

    As an example, if a space's entry in the space report CSV file shows Content Count 3571 and Attachments 258, the total number of available documents for that space is 3,829.

7.  Sum the available-document counts for all spaces to find the total number of available documents in your Atlassian Confluence Cloud source system.

    **Note:** The counts in the space report include all document and attachment types. Some of these may be types that aren't supported by the Atlassian Confluence Cloud external content connector, so the number of documents and attachments retrieved by the connector may be lower than the numbers in the report.


## What to do next

If your Atlassian Confluence Cloud source system's total available document count exceeds the connector limit of one million \(1,000,000\) documents, you will need to limit the crawl scope for the Atlassian Confluence Cloud external content connector. Choose a set of spaces whose total document count is less than the connector limit, and inform your AI Search administrator so they can configure the external content connector's crawl settings to include only those spaces.

For details on configuring the Atlassian Confluence Cloud connector's crawl settings, see [Configure crawl settings for the Atlassian Confluence Cloud external content connector](configure-crawl-settings-cc-ext-cont-connector.md).

**Parent Topic:**[Estimating document volume for source systems](../concept/estimating-doc-volume-src-sys.md)

