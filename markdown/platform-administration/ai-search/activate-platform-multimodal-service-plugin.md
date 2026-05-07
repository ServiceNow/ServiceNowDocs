---
title: Activate the Platform Multimodal Service plugin
description: Enable automatic generation of searchable captions for images found in indexed attachments.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate the Platform Multimodal Service plugin

Enable automatic generation of searchable captions for images found in indexed attachments.

## Before you begin

Role required: admin

## About this task

AI Search offers optional automatic generation of descriptive captions for images found in attachments that you index for search. These generated captions improve search recall, allowing you to search for attachments using keywords that match generated terms.

To use the automatic caption generation feature, you must activate the Platform Multimodal Service \(com.glide.platform\_mm\_service\) plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Platform Multimodal Service \(com.glide.platform\_mm\_service\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

With the plugin activated, AI Search administrators can activate automatic image captioning for individual AI Search indexed sources. For details on this procedure, see [Activate automatic image captioning for attachments from an indexed source](activate-automatic-image-captioning.md).

**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)

