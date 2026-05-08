---
title: Indexing content from AI Search indexed sources
description: AI Search indexes records on indexed source tables to make their content searchable.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexing content from AI Search indexed sources

AI Search indexes records on indexed source tables to make their content searchable.

Once you define an indexed source, AI Search begins automatically indexing to reflect changes to records in the selected source table and its specified child tables. The results of all record create, update, and delete operations in these tables are reflected in the search index. AI Search doesn't index content from unmodified records in these tables until you perform a full table index.

## Indexing content from referenced tables

When an indexed source table includes a reference field that stores a reference to another table, AI Search defaults to indexing values for the reference field but not for other fields on the referenced table. For example, the User \[sys\_user\] table includes a **company** reference field that stores a reference to the Company \[core\_company\] table. When indexing records from the User table, AI Search indexes values for the **company** reference field, but doesn't index values for other Company table fields such as **city** or **website**.

To index additional fields from referenced tables, you can configure **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings for reference fields on your indexed source table.

-   To use field values from referenced tables in search source filters, facet filters, and EVAM search result configurations, create a **dot\_walk\_fields** field setting.
-   To make field values from referenced tables searchable, create a **searchable\_dot\_walk\_fields** field setting.

You can create both **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings for the same reference field.

For instructions on configuring **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings, see [Enable indexing of referenced table fields for an AI Search indexed source](../task/enable-ref-table-field-index-ais.md). For more information on field settings, see [Field settings for AI Search](field-settings-ais.md). To learn about search source filters, see [Search sources in AI Search](search-sources-ais.md). For details on facet filters, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md). To understand EVAM configurations, see Entity View Action Mapping.

## Indexing content from source record attachments

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

-   When indexing an encrypted attachment, AI Search extracts metadata such as file size and date, but doesn't extract searchable content.
-   The encrypted attachment's MIME type is detected as `application/octet-stream`.
-   No feedback for the encrypted attachment appears in ingestion log messages.

Attachment indexing is controlled by an indexed source's **index\_attachments** attribute. To verify that attachment indexing is enabled for an indexed source, see [Enable indexing of attachments for an AI Search indexed source](../task/enable-attachment-indexing-ais.md).

## Indexing content from source record tags

AI Search can index tags found on source table records. Search results display indexed tags based on the visibility of the result record instead of the visibility of the tag.

By default, indexing ignores tags from source records. You can enable indexing of tags for each indexed source. Choose whether you want to index all shared and globally visible tags or just globally visible tags.

For details on enabling tag indexing for an indexed source, see [Enable indexing of tags for an AI Search indexed source](../task/enable-tag-indexing-ais.md).

## Indexing content from the Task table and its child tables

When defining an indexed source that indexes records from the Task table or any of its child tables, you must specify a retention policy. For details on retention policies, see [Indexed source retention policies and filter conditions](retention-policies-conditions-ais.md).

## Reindexing content

You must perform a full table reindex for an indexed source under the following circumstances:

-   After you add, modify, or delete an indexed source attribute or a field setting for the indexed source.
-   If you want to update indexed values for fields on tables referenced by source table records. As an example, the **company** field on the User \[sys\_user\] table stores a reference to the Company \[core\_company\] table. If you configure indexing for values for fields on the referenced Company table, such as **city** or **website**, you must reindex the User table to update those indexed Company table field values. For details on configuring indexing of referenced table fields, see [Enable indexing of referenced table fields for an AI Search indexed source](../task/enable-ref-table-field-index-ais.md).

-   **[Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md)**  
Make content from an internal indexed source searchable by performing a full table index. This procedure indexes existing records from the source table and any child tables configured for indexing. You can manually reindex content from an internal indexed source by repeating this procedure.
-   **[Perform a full table index or reindex for multiple AI Search indexed sources](../task/index-multiple-sources-ais.md)**  
Make content from multiple internal indexed sources searchable by performing a full table index. This procedure indexes existing records from the source tables and any child tables configured for indexing. You can manually reindex content from internal indexed sources by repeating this procedure.

**Parent Topic:**[Indexed sources in AI Search](indexed-sources-ais.md)

