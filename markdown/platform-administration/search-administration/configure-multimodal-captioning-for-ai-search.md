---
title: Configure multimodal captioning for AI Search
description: Use the AI Search Admin console to select the visual language model \(VLM\) provider and model for multimodal captioning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/configure-multimodal-captioning-for-ai-search.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure multimodal captioning for AI Search

Use the AI Search Admin console to select the visual language model \(VLM\) provider and model for multimodal captioning.

## Before you begin

-   The Platform Multimodal Service plugin \(`com.glide.platform_mm_service`\) must be installed on your instance. If the plugin is not installed, multimodal captioning options will not appear in the AI Search Admin console. For more information, see [Activate the Platform Multimodal Service plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-platform-multimodal-service-plugin.md).
-   Role required: ais\_admin


## About this task

When multimodal captioning is activated, attachments retrieved from supported sources are automatically analyzed and given descriptive captions, making visual content, such as images, discoverable through text-based search. You can specify the VLM provider and model to use when generating captions.

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  Select **System Properties**.

3.  In the Multimodal captioning section, select a **Provider** from the drop-down list.

    A provider is the VLM you want to use for captioning.

    **Note:** If your preferred provider is not listed, use the AI Control Tower \(AICT\) to configure approved third-party LLMs. For more information, see [Configure third-party LLMs using AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/configure-third-party-llms-using-ai-control-tower.md). NowLLM does not support this feature.

    The corresponding **Model** options appear.

4.  Select a **Model** from the drop-down list.

    A model is a specific version of AI offered by the provider.

5.  Select **Save**.


## Result

Changes to the provider and model take effect immediately for multimodal captioning.

## What to do next

AI Search administrators have additional configuration options available, as follows:

-   AI Search administrators can activate multimodal captioning for individual AI Search indexed sources. For details on this procedure, see [Activate multimodal captioning for attachments from an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-multimodal-captioning.md).
-   Connector administrators can activate multimodal captioning in the crawl settings for an external content connector. To learn about configuring crawl settings for external content connectors, see [Configuring crawl settings for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-crawl-settings-ext-cont-connector.md).

**Parent Topic:**[Using AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/using-ais-admin-console.md)

