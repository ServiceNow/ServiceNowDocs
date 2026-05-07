---
title: List of AI Search indexed source attributes
description: You can adjust indexing behavior for an AI Search indexed source by configuring indexed source attributes and values.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-04-24"
reading_time_minutes: 5
breadcrumb: [Indexed source attributes, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List of AI Search indexed source attributes

You can adjust indexing behavior for an AI Search indexed source by configuring indexed source attributes and values.

For instructions on defining AI Search indexed source attributes, see [Create an indexed source attribute in AI Search](../task/create-indexed-source-attr-ais.md).

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

index\_mms\_attachments

</td><td>

Control automatic captioning behavior for images in attachments for records on this table. To learn more about automatic image captioning, see [Activate automatic image captioning for attachments from an indexed source](../task/activate-automatic-image-captioning.md).Supported values:

-   **true**: Enable automatic captioning for images in attachments for records on this table.
-   **false**: Disable automatic captioning for images in attachments for records on this table.

Default value: **true**

This attribute has no effect if **index\_attachments** is set to **false** for the indexed source.

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
</table>**Note:** Indexed source attributes are records on the AI Search Configuration Attribute \[ais\_configuration\_attribute\] table that have Table as their **Applies To** field value. Records on this table that have Column as their **Applies To** field value are [Field settings for AI Search](../concept/field-settings-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md)

