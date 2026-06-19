---
title: Activate the Platform Multimodal Service plugin
description: Enable automatic generation of searchable captions for images, tables, charts, and complex layouts found in indexed attachments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/activate-platform-multimodal-service-plugin.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 1
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer]
---

# Activate the Platform Multimodal Service plugin

Enable automatic generation of searchable captions for images, tables, charts, and complex layouts found in indexed attachments.

## Before you begin

Role required: admin

## About this task

AI Search offers optional automatic multimodal generation of descriptive captions for images, tables, charts, and complex layouts found in attachments that you index for search. These generated captions improve search recall, allowing you to search for attachments using keywords that match generated terms.

As an example, an attachment might include an image that yields the generated caption `man on bicycle`. Searches for `man` or `bicycle` can match the caption terms. Such searches return the attachment as a search result even if its text doesn't otherwise contain either of those terms.

To use the automatic multimodal caption generation feature, you must activate the plugin.

**Note:**

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/find-components.md).


## What to do next

With the plugin activated, AI Search administrators can activate multimodal captioning for individual AI Search indexed sources. For details on this procedure, see [Activate multimodal captioning for attachments from an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/activate-multimodal-captioning.md).

**Parent Topic:**[Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configuring-ais.md)

