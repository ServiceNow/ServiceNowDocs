---
title: Enable Now Assist Genius Results in AI Search portals and mobile applications
description: Specify the Now Assist Genius Result types you want to make available in each of your AI Search portals and mobile applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable Now Assist Genius Results in AI Search portals and mobile applications

Specify the Now Assist Genius Result types you want to make available in each of your AI Search portals and mobile applications.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

Role required: ais\_admin

## About this task

Now Assist in AI Search provides multiple AI-powered Genius Result configurations. As a search administrator, you can enable individual Now Assist Genius Result configurations in AI Search portal and mobile applications.

To learn more about how Genius Results work, see [Genius Results](../concept/genius-results-ais.md). For details on the Now Assist Genius Result configurations, see [Now Assist Q&amp;A Genius Results](../concept/now-assist-qna-genius-results.md) and [Now Assist Actions Genius Results](../concept/now-assist-catalog-ordering-gr.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Now Assist in AI Search Setup**.

    The Set up Now Assist in AI Search panel displays a list of search profiles associated with AI Search portals and mobile applications and a Prerequisites section for each Now Assist Genius Result configuration.

2.  If a Now Assist Genius Result enablement option isn't selectable, follow the guidance in its Prerequisites entry to make it selectable.

    **Note:** After following the Prerequisites guidance, you may need to refresh the Set up Now Assist in AI Search panel to make the Now Assist Genius Result enablement option selectable.

3.  In each search profile row, select the options for the individual Now Assist Genius Results you want to enable for the associated AI Search portal or mobile application.

    As an example, to enable Now Assist Q&amp;A Genius Results in Service Portal, select the **Now Assist Q&amp;A** option in the **Service Portal Default Search Profile** row.

    **Note:** You can disable a Now Assist Genius Result for an AI Search portal or mobile application by clearing its option.

4.  Select **Apply Changes**.


## Result

AI Search enables your selected Now Assist Genius Result configurations for all users of the specified AI Search portals and mobile applications.

**Parent Topic:**[Configuring Now Assist in AI Search](../concept/configuring-now-assist-ais.md)

