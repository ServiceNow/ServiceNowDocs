---
title: Activate automatic image captioning for attachments from an indexed source
description: Generate searchable captions for attachment images found on records in an indexed source table.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 2
breadcrumb: [Indexed source attributes, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate automatic image captioning for attachments from an indexed source

Generate searchable captions for attachment images found on records in an indexed source table.

## Before you begin

An administrator must have activated the Platform Multimodal Service plugin on your instance. For details on this procedure, see [Activate the Platform Multimodal Service plugin](activate-platform-multimodal-service-plugin.md).

Role required: ais\_admin

## About this task

When indexing attachments for search, AI Search includes the attachment's text but ignores its images by default. You can configure the multimodal caption service to automatically generate descriptive captions for images in attachments found on records from an indexed source table. With the service activated, you can find indexed source content with attachment images by searching for terms that match the generated image captions.

As an example, an attachment might include an image that yields the generated caption `woman on bicycle`. Searches for `woman` or `bicycle` can match the caption terms. Such searches return the attachment as a search result even if its text doesn't otherwise contain either of those terms.

Automatic image captioning runs as a separate process after text indexing is completed for the attachment in question. Records with attachments that contain images won't show generated captions until image captioning completes.

**Note:** Activating automatic image captioning for attachments found in an indexed source has no effect if the **index\_attachments** attribute is set to **false** for that indexed source. Make sure this attribute is set to **true** if you want to index attachments and generate image captions for them.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to activate automatic image captioning for.

3.  In the Advanced Configuration related list, check for an existing **index\_mms\_attachments** attribute.

    -   If an **index\_mms\_attachments** attribute already exists with value **false**, change its value to **true**. No further steps are needed.
    -   If an **index\_mms\_attachments** attribute exists with value **true**, automatic image captioning is already enabled for the indexed source. No further steps are needed.
    -   If no **index\_mms\_attachments** attribute exists, continue with the following steps.
4.  In the Advanced Configuration related list, select **New**.

5.  On the Indexed Source Attribute form, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Attribute|index\_mms\_attachments|
    |Value|true|

6.  Select **Submit**.


## Result

The new **index\_mms\_attachments** indexed source attribute appears in the Advanced Configuration related list.

## What to do next

To make the new indexed source attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md)

