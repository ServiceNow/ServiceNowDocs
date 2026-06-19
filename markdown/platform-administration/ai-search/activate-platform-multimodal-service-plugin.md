---
title: Activate the Platform Multimodal Service plugin
description: Enable automatic generation of searchable descriptive captions for images, tables, charts, and other visual elements found in indexed attachments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/activate-platform-multimodal-service-plugin.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate the Platform Multimodal Service plugin

Enable automatic generation of searchable descriptive captions for images, tables, charts, and other visual elements found in indexed attachments.

## Before you begin

Role required: admin

## About this task

AI Search offers optional automatic multimodal generation of searchable descriptive captions for images, tables, charts, and other visual elements found in attachments that you index for search. These generated captions improve search recall, allowing you to find attachments using search keywords that match generated terms.

As an example, an attachment might include an image that yields the generated caption `man on bicycle`. Searches for `man` or `bicycle` can match the caption terms. Such searches return the attachment as a search result even if its text doesn't otherwise contain either of those terms.

To use the automatic multimodal caption generation feature, you must activate the Platform Multimodal Service \(com.glide.platform\_mm\_service\) plugin.

**Note:** Multimodal captioning is only supported for Knowledge \[kb\_knowledge\] table records from the Knowledge Table indexed source and for content retrieved by external content connectors.

The multimodal captioning feature has been validated and tested for English-language content. For content in other languages, it may function but has not been evaluated for caption quality or accuracy. Multimodal captioning for non-English content is not currently supported.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Platform Multimodal Service \(com.glide.platform\_mm\_service\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/find-components.md).


## What to do next

With the plugin activated, administrators have additional configuration options available, as follows:

-   AI Search administrators can activate multimodal captioning for individual AI Search indexed sources. For details on this procedure, see [Activate multimodal captioning for attachments from an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-multimodal-captioning.md).
-   Connector administrators can activate multimodal captioning in the crawl settings for an external content connector. To learn about configuring crawl settings for external content connectors, see [Configuring crawl settings for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-crawl-settings-ext-cont-connector.md).
-   AI Search administrators can select the VLM \(visual learning model\) provider and model used by the Platform Multimodal Service. For details on this process, see [Configure multimodal captioning for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-multimodal-captioning-for-ai-search.md).

.

**Parent Topic:**[Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md)

