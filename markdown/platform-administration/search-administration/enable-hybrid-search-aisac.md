---
title: Manage hybrid search in search applications
description: Control hybrid search settings in AI Search applications to optimize search performance. Activate hybrid search to create context-aware results that provide both search precision and contextual relevance. Deactivating hybrid search generates results that rely solely on keyword-based queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/enable-hybrid-search-aisac.html
release: brazil
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Manage hybrid search in search applications

Control hybrid search settings in AI Search applications to optimize search performance. Activate hybrid search to create context-aware results that provide both search precision and contextual relevance. Deactivating hybrid search generates results that rely solely on keyword-based queries.

## Before you begin

-   Starting with ServiceNow Otto for AI Search version 15.0.
-   Must have at least one indexed source with semantic fields and semantic indexing configured.

Role required: ais-admin

## About this task

Hybrid search helps users find relevant content more easily, even when they don't use the exact words in the content. For most experiences, it improves the relevance of results, especially when users search with questions or descriptive phrases. If users typically search for exact values, such as record numbers, IDs, or codes, keyword search may provide more predictable results. For more information, see [Hybrid search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/hybrid-search-ais.md).

Upgrading an existing installation doesn't change current hybrid search settings. Users with the admin role can activate or deactivate hybrid search for individual SACs after installation.

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  From **Applications**, select the search application.

3.  Manage the hybrid search mode.

    -   Enable the **Hybrid search** toggle to switch on the hybrid search mode.
    -   Disable the **Hybrid search** toggle to switch off the hybrid search mode.

## Result

Hybrid search mode is updated for the selected application.

## What to do next

**Parent Topic:**[Using AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/search-administration/using-ais-admin-console.md)

