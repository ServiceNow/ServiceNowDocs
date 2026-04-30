---
title: Facet form
description: The Facet form contains information about facets defined for search application configurations in AI Search. Use this form when creating or modifying a facet.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Facet form

The Facet form contains information about facets defined for search application configurations in AI Search. Use this form when creating or modifying a facet.

For details on creating or modifying a facet, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md).

<table id="ais-facet-form-fields-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the facet.

</td></tr><tr><td>

Label

</td><td>

Label to display for the facet in the search application.

</td></tr><tr><td>

Facet Field

</td><td>

Comma-separated list of field names from AI Search indexed source tables. The facet displays search result refinement filters for values from one or more specified fields that are present in the current search result set. When you select a refinement filter after searching, AI Search restricts the search result set to show only results that contain the specified field value.**Note:** When you save or update a facet, AI Search verifies each facet field. To pass verification, the field must exist on at least one record that exists in a search source used by the search application. If a field doesn't satisfy this condition, the system displays an error message.

 Supports the following formats:

 -   **Table-specific field list**

Enter a comma-separated list of qualified `[indexed_source_table_name].[field_name]` entries. AI Search displays search result refinement filters for values from the superset of the specified indexed source table fields.

For example, enter `kb_knowledge.author` to display search result refinement filters for **Author** field values from the Knowledge \[kb\_knowledge\] indexed source table. Or enter `kb_knowledge.author, sc_cat_item.owner, custom_table.author_field` to display search result refinement filters for values from all of the three specified indexed source table fields.

**Note:** All fields specified in a facet field list must be of the same type.

The `[indexed_source_table_name]` qualifier must be the name of a table specified in an indexed source. Don't specify indexed source child table names for this qualifier.

-   **Cross-table field**

Enter an unqualified `[field_name]` entry. AI Search displays search result refinement filters for values from the specified cross-table field.

For example, enter `language` to display search result refinement filters for **Language** field values from any indexed source table.

**Note:** This format only supports the `language` and `tags` cross-table fields.


 Special cases include:

-   **Faceting on parent table fields**

If you specify an indexed source parent table field as a facet field, AI Search includes values from the same field on child tables from the indexed source.

As an example, suppose you create an indexed source for a custom Parent \[u\_parent\] table, which is extended by a custom Child \[u\_child\] table. If you specify `u_parent.author` as a facet field, AI Search displays search result refinement filters for both `u_parent.author` and `u_child.author` field values.

-   **Faceting on child table fields**

You can specify a field that's unique to an indexed source child table as a facet.

Continuing the previous example, if your Child \[u\_child\] table includes an **Editor** field that's not present on the Parent \[u\_parent\] table, you can specify `u_parent.editor` as a facet to display search result refinement filters for **Editor** field values.

**Note:** Be sure to specify the parent table name as the qualifier, not the child table name.

-   **Faceting on dot-walk fields from referenced tables**

If your indexed source includes a **dot\_walk\_fields** field setting for a dot-walk referenced table field, you can specify that field in a facet field entry using dot-separated reference field qualifiers. Add these qualifiers between the indexed source table name and the referenced table field name.

For example, to facet knowledge article search results based on the Department field values for their authors, you can define `author.department` as a **dot\_walk\_fields** field setting for the indexed source for the Knowledge \[kb\_knowledge\] table and then specify `kb_knowledge.author.department` in your facet field entry. If you define `company.contact.department` as a **dot\_walk\_fields** field setting for the indexed source for the User \[sys\_user\] table, you can specify `sys_user.company.contact.department` in your facet field entry.

**Note:** Each dot-walk reference level imposes a performance impact on indexing. Avoid using multi-level references unless necessary.

To learn about **dot\_walk\_fields** field settings, see [Enable indexing of referenced table fields for an AI Search indexed source](../concept/field-settings-ais.md#).


 Facets work best when created from fields of the following types with relatively few unique values:

-   Choice
-   Reference
-   String
-   String \(Full UTF-8\)
-   True/False

</td></tr><tr><td>

Type

</td><td>

Type of the facet. The facet type determines how many field values you can select as facet refinement filters and the filter logic used by the facet. Supports the following values:

-   **Single Select**

In a Single Select facet, you can only select a single field value as a facet refinement filter.

When you select a field value from a Single Select, AI Search filters the search results list, displaying only results that contain your chosen field value.

A Single Select facet only allows you to select field values that are found in the current result set.

-   **Multi Select And**

In a Multi Select And facet, you can select multiple field values as facet refinement filters.

When you select a field value from a Multi Select And facet, AI Search filters the search results list, displaying only results that contain all of the field values you've selected from the facet.

A Multi Select And facet only allows you to select field values that are found in the current result set.

-   **Multi Select Or**

In a Multi Select Or facet, you can select multiple field values as facet refinement filters.

When you select a field value from a Multi Select Or facet, AI Search filters the search results list, displaying only results that contain any of the field values you've selected from the facet.

A Multi Select Or facet initially only allows you to select field values that are found in the current result set. All field values that are available when you make your first selection remain available for selection.

As an example, suppose you have a Multi Select Or facet for a custom **Color** field with blue, green, and red field values. If your search returns only green and red results, the **Color** facet only displays **green** and **red** field values. When you select the **red** field value, AI Search keeps the **green** field value available for selection because it was available before you made any **Color** selection.


**Warning:** Applying multiple filters from a Multi Select And or Multi Select Or facet makes your search query URL longer. Test your multi-select facet configurations to ensure that search query URLs with facet filters don't exceed the maximum URL length limit for your web browser. \(Different web browsers have different URL length limits.\)

</td></tr><tr><td>

Facet Value Limit

</td><td>

Maximum number of distinct field values to display for the facet.

</td></tr><tr><td>

Order

</td><td>

Order of appearance for the facet in the context of the search application configuration.

</td></tr><tr><td>

Active

</td><td>

Option to activate the facet for the application.

</td></tr><tr><td>

Sort by

</td><td>

Order in which to display the facet's buckets in the search results UI. Type: Choice list

 Default value: Count

 Supported values:

-   **Count**: Sort facet buckets by their search result counts, going from highest count to lowest.
-   **Value**: Sort facet buckets by their labels in alphabetical order.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

