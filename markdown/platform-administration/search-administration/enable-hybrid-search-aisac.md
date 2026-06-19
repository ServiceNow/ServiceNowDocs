---
title: Manage hybrid search in search applications
description: Control hybrid search settings in AI Search applications to optimize search performance. Enable hybrid search to create context-aware results that combine keyword matching with semantic understanding. Disabling it generates results that rely solely on keyword-based queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/enable-hybrid-search-aisac.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Manage hybrid search in search applications

Control hybrid search settings in AI Search applications to optimize search performance. Enable hybrid search to create context-aware results that combine keyword matching with semantic understanding. Disabling it generates results that rely solely on keyword-based queries.

## Before you begin

-   Beginning with Now Assist in AI Search version 15.0.
-   Must have at least one indexed source with semantic fields and semantic indexing configured.

Role required: admin

## About this task

Hybrid search combines traditional keyword-based search with AI-powered semantic understanding. When hybrid search mode is on, it processes keywords and comprehends the meaning and context of your query, which delivers more accurate and comprehensive results. For more information, see [Hybrid search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/hybrid-search-ais.md).

Beginning with Now Assist in AI Search version 17.0, hybrid search is automatically activated for all search application configurations \(SACs\) when you install Now Assist in AI Search for the first time. Upgrading an existing installation does not change current hybrid search settings. Users with the admin role can deactivate hybrid search for individual SACs after installation.

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the search application for which you want to enable hybrid search.

3.  In the menu, select **Search Application Configuration**.

4.  In the Hybrid search section, select **Manage hybrid search**.

5.  Manage the hybrid search mode.

    -   Enable the **Hybrid search** toggle to switch on the hybrid search mode.
    -   Disable the **Hybrid search** toggle to switch off the hybrid search mode.

## Result

Hybrid search mode is updated for the selected application.

**Parent Topic:**[Using AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/using-ais-admin-console.md)

