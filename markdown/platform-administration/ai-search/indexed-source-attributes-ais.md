---
title: Indexed source attributes for AI Search
description: An indexed source attribute defines indexing behavior for all records from an indexed source.Define an indexed source attribute to configure the AI Search content indexing behavior for all records on a source table.Configure an indexed source attribute to enable indexing of content from tags found on records from an indexed source.Configure an indexed source attribute to enable indexing of content from attachments found on records from an indexed source.You can adjust indexing behavior for an AI Search indexed source by configuring indexed source attributes and values.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed source attributes for AI Search

An indexed source attribute defines indexing behavior for all records from an indexed source.

Examples of how you might use indexed source attributes include the following.

-   Define a filter to limit the set of records indexed from the source table
-   Modify default indexing behavior for attachments or tags found on source table records
-   Specify whether to index translated fields from source table records

An indexed source's attributes appear in its Advanced Configuration related list.

**Parent Topic:**[Indexed sources in AI Search](indexed-sources-ais.md)

## Create an indexed source attribute in AI Search

Define an indexed source attribute to configure the AI Search content indexing behavior for all records on a source table.

### Before you begin

Role required: ais\_admin

### About this task

For details on available indexed source attributes and values, see [List of AI Search indexed source attributes](indexed-source-attributes-ais.md#).

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to define an attribute for.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, fill in the fields.

    For a description of the field values, see [Indexed Source Attribute form](../reference/indexed-source-attribute-form-ais.md).

5.  Select **Submit**.


### Result

The new indexed source attribute appears in the Advanced Configuration related list.

### What to do next

To make the new indexed source attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

## Enable indexing of tags for an AI Search indexed source

Configure an indexed source attribute to enable indexing of content from tags found on records from an indexed source.

### Before you begin

Role required: ais\_admin

### About this task

By default, AI Search indexing ignores tags from source records. You can enable indexing of tags for all records from an indexed source. Choose whether you want to index all shared and globally visible tags or only globally visible tags. Private tags are never indexed.

For more general instructions on defining indexed source attributes, see [Create an indexed source attribute in AI Search](indexed-source-attributes-ais.md#).

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to enable tag indexing for.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, fill in the fields.

    1.  In the **Attribute** field, enter `index_tags`.

    2.  In the **Value** field, enter one of the following options:

    |Option|Description|
    |------|-----------|
    |everyone\_only|Only tags shared with everyone are indexed.|
    |all\_shared|All shared tags \(**Everyone**, **Groups and Users**\) are indexed.|

    For a description of the field values, see [Indexed Source Attribute form](../reference/indexed-source-attribute-form-ais.md).

5.  Select **Submit**.


### Result

The new **index\_tags** indexed source attribute appears in the Advanced Configuration related list.

### What to do next

To make the new **index\_tags** attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

## Enable indexing of attachments for an AI Search indexed source

Configure an indexed source attribute to enable indexing of content from attachments found on records from an indexed source.

### Before you begin

Role required: ais\_admin

### About this task

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

The following procedure explains how to make sure this attribute is set to **true** for an indexed source. For more general instructions on defining indexed source attributes, see [Create an indexed source attribute in AI Search](indexed-source-attributes-ais.md#).

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to verify or change attachment indexing for.

3.  In the Advanced Configuration related list, check for an **index\_attachments** attribute with value **false**.

    **Note:** If no **index\_attachments** attribute exists in the related list, or the attribute exists with value **true**, attachment indexing is already enabled for the indexed source. No further steps are required.

4.  Open the **index\_attachments** attribute and change its value from **false** to **true**.


### Result

Attachment indexing is enabled for the indexed source.

### What to do next

If you changed the **index\_attachments** attribute's value from **false** to **true**, reindex content for the indexed source. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

## List of AI Search indexed source attributes

You can adjust indexing behavior for an AI Search indexed source by configuring indexed source attributes and values.

For instructions on defining AI Search indexed source attributes, see [Create an indexed source attribute in AI Search](indexed-source-attributes-ais.md#).

<table id="table_m5b_r3j_smb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

Specify a filter condition that applies on the indexed source table and all of its child tables configured for indexing. Indexing ignores source records that don't pass this filter condition. If you change the value of this attribute for an indexed source, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

index\_attachments

</td><td>

Control indexing behavior for attachments from indexed records. Supported values:

-   **true**: Enable indexing of attachments for records on this table.
-   **false**: Disable indexing of attachments for records on this table.

Default value: **true**

If you change the value of this attribute for an indexed source, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

index\_tags

</td><td>

Control indexing behavior for tags from indexed records. Supported values:

-   **all\_shared**: Index shared tags and globally visible tags.
-   **everyone\_only**: Only index globally visible tags.
-   **none**: Disable indexing of tags.

 Default value: **none**

**Note:** Search results display indexed tags based on the visibility of the result record instead of the visibility of the tag.

 If you change the value of this attribute for an indexed source, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

index\_translated\_fields

</td><td>

Control indexing behavior for translated fields from indexed records. Supported values:

-   **true**: Enable indexing of translated fields for this table.
-   **false**: Disable indexing of translated fields for this table.

 Default value: **false**

**Note:** For tables with manually mapped records, such as kb\_knowledge, indexing ignores this attribute and honors the manual mapping.

 If you change the value of this attribute for an indexed source, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

index\_translated\_reference\_fields

</td><td>

Control indexing behavior for translated reference fields from indexed records. Supported values:

-   **true**: Enable indexing of translated reference fields for this table.
-   **false**: Disable indexing of translated reference fields for this table.

 Default value: **true**

 If you change the value of this attribute for an indexed source, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

user\_read\_takes\_precedence\_over\_group\_deny

</td><td>

Control precedence of external user read access permissions and external group deny access permissions for external document search results from the indexed source. Supported values:

-   **true**: External user read access permissions take precedence over external group deny access permissions for external document search results from the indexed source.
-   **false**: External group deny access permissions take precedence over external user read access permissions for external document search results from the indexed source.

 Default value: **true** on indexed sources for external content schema tables. Not set on indexed sources for internal tables.

**Note:** This attribute only applies to indexed sources for external content schema tables. If you apply this attribute to an indexed source for an internal table, it has no effect.

</td></tr></tbody>
</table>**Note:** Indexed source attributes are records on the AI Search Configuration Attribute \[ais\_configuration\_attribute\] table that have Table as their **Applies To** field value. Records on this table that have Column as their **Applies To** field value are [Field settings for AI Search](field-settings-ais.md#).

