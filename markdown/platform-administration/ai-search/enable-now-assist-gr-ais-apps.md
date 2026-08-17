---
title: Enable ServiceNow Otto for AI Search Genius Results in AI Search portals and mobile applications
description: Specify the ServiceNow Otto for AI Search Genius Result types you want to make available in each of your AI Search portals and mobile applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/enable-now-assist-gr-ais-apps.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-07-25"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow Otto for AI Search, ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable ServiceNow Otto for AI Search Genius Results in AI Search portals and mobile applications

Specify the ServiceNow Otto for AI Search Genius Result types you want to make available in each of your AI Search portals and mobile applications.

## Before you begin

The ServiceNow Otto for AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/install-now-assist-ais.md).

Role required: ais\_admin

## About this task

ServiceNow Otto for AI Search provides multiple AI-powered Genius Result configurations. As a search administrator, you can enable individual Genius Result configurations in AI Search portal and mobile applications.

To learn more about how Genius Results work, see [Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/genius-results-ais.md). For details on the Genius Result configurations, see [Knowledge base articles Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md) and [Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-catalog-ordering-gr.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **ServiceNow Otto for AI Search in Setup**.

    The Set up ServiceNow Otto for AI Search panel displays a list of search profiles associated with AI Search portals and mobile applications and a Prerequisites section for each Genius Result configuration.

2.  If a Genius Result enablement option isn't selectable, follow the guidance in its Prerequisites entry to make it selectable.

    **Note:** After following the Prerequisites guidance, you may need to refresh the Set up panel to make the Genius Result enablement option selectable.

3.  In each search profile row, select the options for the individual Genius Results you want to enable for the associated AI Search portal or mobile application.

    As an example, to enable Knowledge base articles Genius Results in Service Portal, select the **Knowledge base articles** option in the **Service Portal Default Search Profile** row.

    **Note:** You can disable a Genius Result for an AI Search portal or mobile application by clearing its option.

4.  Select **Apply Changes**.


## Result

AI Search enables your selected Genius Result configurations for all users of the specified AI Search portals and mobile applications.

**Parent Topic:**[Configuring ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-now-assist-ais.md)

