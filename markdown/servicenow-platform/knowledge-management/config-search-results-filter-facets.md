---
title: Configure filter facet widget instance options
description: Configure widget instance options for the filter facet widgets on the Knowledge Management Service Portal search results page.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure filter facet widget instance options

Configure widget instance options for the filter facet widgets on the Knowledge Management Service Portal search results page.

## Before you begin

Role required: sp\_admin or admin

## About this task

The homepage uses several widgets to filter the items in the search results list. There are two types of facet widgets:

-   Simple field facets based on the Knowledge table fields
-   Advanced query facets based on custom queries of the Knowledge table

Use the widget instance options to customize these facet widgets:

-   Knowledge Field Facet \(for filtering by knowledge base, knowledge category, and author\)
-   Knowledge Tags Facet \(for filtering by tag\)
-   Knowledge Resource Facet \(for filtering by resource, such as articles\)
-   Knowledge Query Facet \(for filtering by rating, last modified, and number of views\)

    **Note:** Query facets are displayed when there's at least one knowledge field facet added to the page.


Use default Knowledge Language Widget to include language filters in the knowledge Search Result page. To add a custom language widget, you need to deactivate the Knowledge Language Widget on the Knowledge Search Result page.

## Procedure

1.  Navigate to the Knowledge Management Service Portal search results page.

2.  Control + right-click a filter facet widget.

3.  Click **Instance Options**.

4.  Configure the desired settings for the selected type of facet widget.

<table id="table_KM_SP_filter_facet_widgets"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the filter facet widget.

</td></tr><tr><td>

Glyph

</td><td>

Icon that appears to the left of the title.

</td></tr><tr><td>

Order

</td><td>

Order in which the filter facet widgets appear on the left side of the search results page. If empty, the filter facet widgets sort alphabetically.

</td></tr><tr><td>

Bootstrap color

</td><td>

Color of the filter facet widget header.

</td></tr><tr><td>

CSS

</td><td>

Custom configurations that determine the look and feel of the elements in the widget. For more information, see Service Portal SCSS Primer.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the **Source Field** used to provide the filter facet widget options. The default table is Knowledge \(kb\_knowledge\).

</td></tr><tr><td>

Source Field

</td><td>

Field in the **Source Table** that provides the filter facet widget options. Field types that can be used as a source field include string, glide list, integer, reference, and boolean.

</td></tr><tr><td>

Facet Identifier

</td><td>

Unique name for the custom query facet that can be used in script code.

</td></tr><tr><td>

Facet Template

</td><td>

Template that determines the type of facet interaction. Knowledge Field Facet widget templates:

-   **Single Select**: users can select only one filter from this widget.
-   **Multi Select**: users can select more than one filter from this widget.
-   **Dropdown Select**: users can select more than one filter from a drop-down menu.
 Knowledge Query Facet widget templates

-   **Simple Query**: shows a label for each facet value.
-   **Rating**: shows rating stars.


</td></tr><tr><td>

Custom Template

</td><td>

Custom template that determines facet interaction and value selection.

</td></tr><tr><td>

Facet Options

</td><td>

Custom query in JSON format for the label, ID, order, and query for each facet value. Includes the table, value \(encoded query\), and display value \(encoded query\).

</td></tr><tr><td>

Order by

</td><td>

Order of the filter options within the facet widget. The default order is **label**, which sorts the options in alphabetical order. For reference fields, you can also state an order from the reference field table.

</td></tr><tr><td>

Minimum results for showing filter search bar

</td><td>

Minimum number of results required to display a search bar at the top of the filter facet widget.

</td></tr><tr><td>

Minimum results for showing scroll bar

</td><td>

Minimum number of results required to display a scroll bar in the filter facet widget.

</td></tr><tr><td>

Maximum length for string field

</td><td>

Maximum field length. Only fields whose length is less than this value are allowed to be added as a filter facet.

</td></tr><tr><td>

Alternate URL Parameters

</td><td>

Names of the URL parameters used to initialize this filter facet, if used in the URL as a search parameter.

</td></tr><tr><td>

Fetch Maximum Values

</td><td>

Option to fetch filter values from all knowledge articles in the search results.

 Selecting the **Fetch Maximum Values** option might impact the load time for search results. If this option is disabled, the load time improves based on the **glide.knowman.search.facet\_depth** property value.

 If the **glide.knowman.search.apply\_acls**property is set to true, a filter value can appear in a filter facet even when there are no search results for that filter value. For example, a knowledge base without any articles might appear as a value in the knowledge base filter facet.

</td></tr><tr><td>

Show Empty Value

</td><td>

If enabled, shows an empty filter facet option that users can select to filter for articles that do not have this field set. For example, if an article does not have an assigned category, clicking the empty option lists all articles with no assigned category.

</td></tr><tr><td>

Show Only Facet Values Matching Results

</td><td>

Creates a dynamic filter facet widget that displays only those filter values that match the search results rather than showing all values. If you disable this instance option, the time needed to load the filter facet data is reduced.

</td></tr><tr><td>

Show category hierarchy \(valid for kb\_category only\)

</td><td>

If enabled, shows categories with their hierarchy list up to the fourth-level. When you enable this option, you can select only one category at a time. Any articles that are included in the subcategories beyond the fourth-level also appear in the fourth-level of category. The search results filtered on a selected parent category include articles within that category and all the associated child categories. **Note:**

-   If the number of knowledge articles returned in search results is greater than the search facet depth, all categories are displayed in this facet. Therefore, some categories shown in this facet might not be associated with any knowledge articles in the search results. By default, the facet depth is set to 300 and configured by an administrator in the **glide.knowman.search.facet\_depth** property.
-   To configure the knowledge Search Results page widgets by adding more filters. Specifically if filters on language need to be applied they should be using the OOB Knowledge Language Widget. The field facet widget can be configured using language field in instance options for similar behaviour but in that case OOB Knowledge Language Widget instance should be inactivated on the Knowledge Search Results page.


</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

**Related topics**  


[Knowledge Management properties](../reference/r_KnowledgeProperties.md#)

