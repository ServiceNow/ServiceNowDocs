---
title: Sort Option form
description: The Sort Option form contains information about search result sort options defined in your AI Search application configurations. Use this form when creating or modifying a search result sort option for a search application configuration.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Sort Option form

The Sort Option form contains information about search result sort options defined in your AI Search application configurations. Use this form when creating or modifying a search result sort option for a search application configuration.

For details on creating or editing search result sort options, see [Search result sort options in AI Search application configurations](../concept/sort-options-srch-app-cfg-ais.md#).

<table id="table_f2c_t4r_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label displayed for the search result sort option in the search application's sort menu.

</td></tr><tr><td>

Sort Field

</td><td>

Name of a source table field or common index field that the sort option uses to sort search results. The sort field can be a date, number, or string field.

**Note:** If you specify a sort field of an unsupported type, an error message appears when you attempt to save the sort option.

 Supports the following formats:

-   **Qualified `[indexed_source_table_name].[field_name]` entry**

Sort search results on their values from the specified table's field.

For example, enter `kb_knowledge.author` to sort search results by their Author field values.

**Note:** The parent search application configuration's linked search profile must include a search source derived from the specified indexed source table. If this condition isn't met, an error message appears when you attempt to save the sort option.

-   **Unqualified common index field name**

Sort search results on their values from the specified common AI Search index field.

For example, enter `title` to sort search results based on their titles, or `language` to sort search results based on their language.


 The `[indexed_source_table_name]` qualifier must be the name of a table specified in an indexed source. Don't specify indexed source child table names for this qualifier.

 Special cases include:

-   **Sorting on parent table fields**

If you specify an indexed source parent table's field in a sort option, AI Search includes values from the same field on child tables from the indexed source.

For example, suppose you create an indexed source for custom table Parent \[u\_parent\] which is extended by custom table Child \[u\_child\], and then specify `u_parent.author` as the field for a sort option. When a user applies the sort option, AI Search uses both `u_parent.author` and `u_child.author` field values to sort the search result list.

-   **Sorting on child table fields**

You can specify a field that's unique to an indexed source's child table as a sort option field.

Continuing the previous example, if your Child \[u\_child\] table includes an **Editor** field that's not present on the Parent \[u\_parent\] table, you can define `u_parent.editor` as a sort option field to sort search result s using this field's values.

**Note:** Be sure to specify the parent table's name as the qualifier, not the child table's name.


</td></tr><tr><td>

Application

</td><td>

Application scope for the search result sort option. This field is automatically set.

</td></tr><tr><td>

Ascending

</td><td>

Option to make the search result sort option display results in ascending order \(a to z\). Clear this option to make the search result sort option display results in descending order \(z to a\).

</td></tr><tr><td>

Active

</td><td>

Option to activate the search result sort option for use in the search application.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

