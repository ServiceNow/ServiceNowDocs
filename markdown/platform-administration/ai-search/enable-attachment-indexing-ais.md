---
title: Enable indexing of attachments for an AI Search indexed source
description: Configure an indexed source attribute to enable indexing of content from attachments found on records from an indexed source.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indexed source attributes, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable indexing of attachments for an AI Search indexed source

Configure an indexed source attribute to enable indexing of content from attachments found on records from an indexed source.

## Before you begin

Role required: ais\_admin

## About this task

By default, AI Search indexes searchable content and metadata \(such as file size and date\) for attachments found on source table records. Indexing supports the following attachment file formats:

-   Active Server Page Extended \(`.aspx`\)
-   Hypertext Markup Language \(`.html`, `.htm`\)
-   Microsoft Excel \(`.xls`, `.xlsx`\)
-   Microsoft PowerPoint \(`.pot`, `.potx`, `.ppt`, `.pptm`, `.pptx`\)
-   Microsoft Word \(`.doc`, `.docx`, `.dot`, `.dotx`\)
-   Plain Text \(`.txt`\)
-   Portable Document Format \(`.pdf`\) with searchable text

**Note:** The maximum file size for binary files is 25 MB. Keyword indexing processes up to the first 1MB of text. Use semantic search to index data containing between 1MB and 25 MB of text.

AI Search provides limited support for encrypted record attachments:

-   When indexing an encrypted attachment, AI Search extracts metadata such as the attachment file's size and date, but it doesn't extract searchable content.
-   The encrypted attachment's MIME type is detected as `application/octet-stream`.
-   No feedback for the encrypted attachment appears in ingestion log messages.

Attachment indexing is controlled by an indexed source's **index\_attachments** attribute:

-   true \(default value\): Attachments are indexed for records from the indexed source.
-   false: Attachments aren't indexed for records from the indexed source.

The following procedure explains how to make sure this attribute is set to **true** for an indexed source. For more general instructions on defining indexed source attributes, see [Create an indexed source attribute in AI Search](create-indexed-source-attr-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to verify or change attachment indexing for.

3.  In the Advanced Configuration related list, check for an **index\_attachments** attribute with value **false**.

    **Note:** If no **index\_attachments** attribute exists in the related list, or the attribute exists with value **true**, attachment indexing is already enabled for the indexed source. No further steps are required.

4.  Open the **index\_attachments** attribute and change its value from **false** to **true**.


## Result

Attachment indexing is enabled for the indexed source.

## What to do next

If you changed the **index\_attachments** attribute's value from **false** to **true**, reindex content for the indexed source. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md)

