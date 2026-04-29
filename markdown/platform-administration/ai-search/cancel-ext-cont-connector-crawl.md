---
title: Cancel a running external content connector crawl
description: Cancel a running crawl for an external content connector to prevent the connector from retrieving and feeding additional documents or access permissions to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Cancel a running external content connector crawl

Cancel a running crawl for an external content connector to prevent the connector from retrieving and feeding additional documents or access permissions to AI Search for indexing.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Search administrators can manually cancel external content connector crawls that are in the running state. When you cancel an external content connector's crawl, the connector stops retrieving documents or access permissions and feeding them to AI Search for indexing.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector whose crawl you want to cancel.

3.  In the connector editor, select the **Crawl history** tab.

4.  Select the crawl history record for the currently running crawl.

    The running crawl has state **In progress**.

5.  Select **Cancel**, then select **Yes, cancel** in the Cancel crawl dialog box.

    **Note:** Canceling a crawl may take a minute or two. During this time, the connector may continue to retrieve searchable content and security principals and feed them to AI Search.


## Result

The selected external content connector halts its crawl.

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

