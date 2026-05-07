---
title: List of AI Search indexed source field settings
description: You can adjust indexing behavior for source record fields in an AI Search indexed source by configuring field setting attributes and values.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Field settings, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List of AI Search indexed source field settings

You can adjust indexing behavior for source record fields in an AI Search indexed source by configuring field setting attributes and values.

For more information on creating field settings, see [Create a field setting for an AI Search indexed source](../task/create-field-setting-ais.md).

<table id="table_m5b_r3j_smb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dot\_walk\_fields

</td><td>

Index reference and display values from fields on the selected reference field's source table for use in search source filters, facet filters, and EVAM search result configurations. AI Search automatically updates the indexed field values to reflect changes made to the referenced table's field values.

 For more information about search source filters, see [Search sources in AI Search](../concept/search-sources-ais.md). For details on facet filters, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md).

-   Field: Name of the reference field on your indexed source table. As an example, if your indexed source table contains a **company** reference field that references the Company \[core\_company\] table, and you want to index field values from that table's **name** and **city** fields, you'd set `company` as the field.
-   Type: string
-   Value: Comma-separated list of referenced table fields to index values from. As an example, if your indexed source table contains a **company** reference field that references the Company \[core\_company\] table, and you want to index field values from that table's **name** and **city** fields, you'd set `name,city` as the value.

**Note:** You can't search field values indexed with this field setting. To index field values from referenced tables for search, create a **searchable\_dot\_walk\_fields** field setting. You can create both **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings for the same reference field.

 If you change the value of this setting for an indexed source's field, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

index\_calculated\_field

</td><td>

Option to enable indexing of searchable content from calculated field values. If your indexed source contains a calculated field, set this field setting to **true** for that field to correctly index its values. With a field setting value of **false** or no value, AI Search ignores values from the calculated field when indexing content.

-   Field: Name of a calculated field from the indexed source table. \(If you specify a non-calculated field, the system rejects the field setting submission and displays a warning message.\)
-   Type: true \| false
-   Supported values:
    -   **true**: Apply special handling to correctly index calculated field values from the selected field.
    -   **false**: Don't apply special handling when indexing field values from the selected field. Calculated field values aren't indexed.

 If you change the value of this setting for an indexed source's field, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

map\_to

</td><td>

Map the selected field from the indexed source table to an AI Search index field. When indexing records from the source table, AI Search populates the specified index field with the value of the selected source field. For example, the base system's Knowledge Table indexed source maps the **kb\_knowledge.short\_description** source field to the **title** index field. When AI Search indexes a record from the Knowledge \[kb\_knowledge\] table, it populates the indexed record's searchable title with the value from the source record's **short\_description** field.

-   Field: Name of a field from the indexed source table.
-   Type: string
-   Value: Name of the AI Search field that you want to map the selected field's display values to. For details on AI Search index fields, see [AI Search index fields](index-fields-list-ais.md).

**Note:** You can only define one **map\_to** field setting for an indexed source field. If you try to define multiple **map\_to** settings for the same field, the system displays an error message.

 If you change the value of this setting for an indexed source's field, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

no\_text\_index

</td><td>

Option to disable indexing of searchable content from the selected field on records from the indexed source.-   Field: Name of a field from the indexed source table.
-   Type: true \| false
-   Supported values:
    -   **true**: Disable searchable content indexing for the selected field. Search and filters can't match the field's value. AI Search doesn't generate an index event when the field is updated.
    -   **false**: Enable searchable content indexing for the selected field. Search and filters can match the field's value. AI Search generates an index event when the field is updated, adding the affected record to its indexing queue.
-   Default value: **false**

 If you change the value of this setting for an indexed source's field, the new value immediately affects index event generation for updates to that field, but it doesn't affect searches or filters for previously indexed records until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

 **Warning:** Don't set this option to **true** for the sys\_updated\_on field on the Task \[task\] table, tables that extend Task, or any other tables that you've configured retention policies for. The retention policies for these tables rely on indexing of sys\_updated\_on field values. For more information on retention policies, see [Indexed source retention policies and filter conditions](../concept/retention-policies-conditions-ais.md).

For Customer Service and Support guidelines on setting the **no\_text\_index** option for different field types, see [KB0859922](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0859922) on the Now Support site.

</td></tr><tr><td>

not\_searchable

</td><td>

Option to disable search matching for content indexed from the selected field.-   Field: Name of a field from the indexed source table.
-   Type: true \| false
-   Supported values:
    -   **true**: Disable search matching for content indexed from the selected field. Search can't match the field's value. Filters \(such as those for content security, source facet buckets, and facets\) can still match the field's value.
    -   **false**: Enable search matching for content indexed from the selected field. Search and filters can match the field's value.
-   Default value: **false**

 If you change the value of this setting for an indexed source's field, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr><tr><td>

searchable\_dot\_walk\_fields

</td><td>

Index reference and display values from fields on the selected reference field's source table as searchable text. AI Search doesn't automatically update the indexed field values to reflect changes made to the referenced table's field values. To update the indexed field values, you must reindex the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

-   Field: Name of the reference field on your indexed source table. As an example, if your indexed source table contains a **company** reference field that references the Company \[core\_company\] table, and you want to index searchable text from that table's **name** and **city** fields, you'd set `company` as the field.
-   Type: string
-   Value: Comma-separated list of referenced table fields to index as searchable content. As an example, if your indexed source table contains a **company** reference field that references the Company \[core\_company\] table, and you want to index searchable text from that table's **name** and **city** fields, you'd set `name,city` as the value.

**Note:** You can't use field values indexed with this field setting in search source filters. To index field values from referenced tables for use in search source filters, create a **dot\_walk\_fields** field setting. You can create both **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings for the same reference field.

 If you change the value of this setting for an indexed source's field, the change doesn't take effect until you reindex content from the indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

</td></tr></tbody>
</table>**Note:** Field settings are records on the AI Search Configuration Attribute \[ais\_configuration\_attribute\] table that have Column as their **Applies To** field value. Records on this table that have Table as their **Applies To** field value are [Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md).

This example shows how the base system's Catalog Item Table indexed source maps **short\_description** field values from the Catalog Item \[sc\_cat\_item\] table to the AI Search index's **text** field for indexed records.

![AI Search Field Setting form showing source Catalog Item [sc_cat_item], attributemap_to, fieldshort_description, and valuetext.](../image/indexed-field-attr-example-map_to.png)

**Parent Topic:**[Field settings for AI Search](../concept/field-settings-ais.md)

