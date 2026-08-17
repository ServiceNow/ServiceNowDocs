---
title: Install ServiceNow Otto for AI Search
description: As an administrator, you can install the ServiceNow Otto for AI Search application \(sn\_ais\_assist\) from the AI Admin Hub module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/install-now-assist-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Install ServiceNow Otto for AI Search

As an administrator, you can install the ServiceNow® Otto for AI Search application \(sn\_ais\_assist\) from the AI Admin Hub module.

## Before you begin

Role required: admin

## About this task

The ServiceNow Otto for AI Search plugin is automatically installed as a dependency when you install a ServiceNow Otto plugin in ServiceNow Otto Admin. ServiceNow Otto for AI Search is included in Now Assist suites.

**Note:** When you upgrade to the latest version of ServiceNow Otto for AI Search, the system reindexes content from the Catalog Item Table and Knowledge Table indexed sources. While these reindexing tasks are ongoing, searches may not return answers from these sources. After reindexing completes, answers should appear normally.

## Procedure

1.  In ServiceNow Otto Admin, install one or more ServiceNow Otto plugins.

    To review the instructions for ServiceNow Otto feature plugin installation, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md). As part of the procedure, you may need to request a license for the plugin from the ServiceNow Store.

2.  Verify that ServiceNow Otto for AI Search is installed:

    1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

    2.  In the workflow list, select **Platform**.

    3.  Verify that the **Conversational experience** feature card displays, and that the **Knowledge base articles Genius Results** and **Actions** skills appear in the **All Conversational experience skills** listing.


## What to do next

With the plugin installed, search administrators can enable Genius Results in the following contexts.

-   Enable all available Genius Result configurations in individual AI Search portals. For details, see [Enable ServiceNow Otto for AI Search Genius Results in AI Search portals and mobile applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enable-now-assist-gr-ais-apps.md).
-   Enable Q&amp;A Genius Results in search profiles for AI Search applications. For steps, see [Enabling Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enabling-now-assist-qa-grs.md).
-   Enable Q&amp;A Genius Results in global search using the AI Search for Next Experience application. For steps, see [Enabling Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enabling-now-assist-qa-grs.md).

To learn more about configuration settings for the plugin, see [Configuring Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configuring-now-assist-ais.md).

-   **[Review available versions of ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/review-available-versions-na-ais.md)**  
View all versions of the ServiceNow Otto for AI Search application on the ServiceNow Store. Use this information to find the latest version of the application that's compatible with your instance's current ServiceNow AI Platform® family release.

**Parent Topic:**[ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/now-assist-ais.md)

