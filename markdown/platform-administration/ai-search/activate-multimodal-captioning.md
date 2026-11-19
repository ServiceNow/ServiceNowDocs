---
title: Activate multimodal captioning for attachments from an indexed source
description: Generate searchable captions for images, tables, charts, and complex layouts in attachments from records in an indexed source table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/activate-multimodal-captioning.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 2
breadcrumb: [Indexed source attributes, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Activate multimodal captioning for attachments from an indexed source

Generate searchable captions for images, tables, charts, and complex layouts in attachments from records in an indexed source table.

## Before you begin

An administrator must have activated the plugin on your instance. For details on this procedure, see [Activate the Platform Multimodal Service plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/activate-platform-multimodal-service-plugin.md).

Role required: ais\_admin

## About this task

When indexing attachments for search, AI Search includes the attachment's text but ignores its images by default. For tables, charts, and complex layouts, indexing extracts text but doesn't necessarily preserve the context of that text.

To improve search recall, you can configure the to automatically generate descriptive captions for images, tables, charts, and complex layouts in attachments found on records from an indexed source table. With the service activated, you can find indexed source content attachments with these entity types by searching for terms that match the generated captions.

As an example, an attachment might include an image that yields the generated caption `woman in office`. Searches for `woman` or `office` can match the caption terms. Such searches return the attachment as a search result even if its text doesn't otherwise contain either of those terms.

**Note:**

Multimodal captioning runs as a separate process after text indexing is completed for the attachment in question. Records with attachments that contain images, tables, charts, or complex layouts won't show generated captions until multimodal captioning completes.

**Note:** Activating multimodal captioning for attachments found in an indexed source has no effect if the **index\_attachments** attribute is set to **false** for that indexed source. Make sure this attribute is set to **true** if you want to index attachments and generate captions for their content.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to activate multimodal captioning for.

    **Note:** Multimodal captioning is currently only supported for records from the Knowledge Table indexed source \(for the Knowledge \[kb\_knowledge\] table\).

3.  In the Advanced Configuration related list, check for an existing **index\_mms\_attachments** attribute.

    -   If an **index\_mms\_attachments** attribute already exists with value **false**, change its value to **true**. No further steps are needed.
    -   If an **index\_mms\_attachments** attribute exists with value **true**, multimodal captioning is already enabled for the indexed source. No further steps are needed.
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

To make the new indexed source attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/index-single-source-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/indexed-source-attributes-ais.md)

