---
title: Configure multi-content synthesized sources
description: Configure indexed sources so that AI Search includes content from multiple sources when generating responses. When you configure a source for synthesis, the large language model draws from that source alongside others to produce more complete, contextually relevant answers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/configure-multi-content-synthesis-sources.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure multi-content synthesized sources

Configure indexed sources so that AI Search includes content from multiple sources when generating responses. When you configure a source for synthesis, the large language model draws from that source alongside others to produce more complete, contextually relevant answers.

## Before you begin

This task assumes you have completed the Now Assist in AI Search setup and are ready to activate sources for AI-generated responses.

-   The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/install-now-assist-ais.md).

-   The source must be added to the search profile as a search source. For more information, see [Create a search source for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-search-source-ais.md).
-   The source must be configured as a hybrid source with semantic fields and semantic indexing configured. For more information, see [Manage hybrid search in search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enable-hybrid-search-aisac.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  Select **Application** &gt; **Service Portal** &gt; **Search Sources**.

3.  Select the Include in AI responses toggle next to the source you want to activate.

    Sources that aren't configured as hybrid sources with semantic indexing can't be activated for synthesis and won't display the toggle.

    Selecting the toggle triggers a confirmation dialog to complete the activation.

4.  Select **Submit**.


## Result

The toggle now shows as activated and results from this source are now included in AI-generated responses.

## What to do next

After activating sources, run a test search to confirm AI-generated responses include content from this source. If results from this source don't appear in AI-generated responses, verify that the source still shows as a hybrid source with semantic indexing active and rerun the steps. Configuration changes after initial setup can affect synthesis eligibility.

For more information about multi-content synthesized sources, see [Generate multi-content synthesized responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/generate_multicontent_sythesized-sources.md).

**Parent Topic:**[Using AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/using-ais-admin-console.md)

