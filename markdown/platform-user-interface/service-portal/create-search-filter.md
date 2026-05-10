---
title: Add facets to a simple search source
description: Enable end users to refine search results for a simple search source. You can create facets for a table search source that return results based on field values or query conditions.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add facets to a simple search source

Enable end users to refine search results for a simple search source. You can create facets for a table search source that return results based on field values or query conditions.

## Before you begin

Role required: admin or sp\_admin

In new instances, search facets are enabled by default. If upgrading from a previous release, enable search facets by activating a record in the Page Route Maps \[sp\_page\_route\_map\] table. See [Enable search facets](enable-facets.md). Create facet items and mapped queries with no more than 30 filter items. To verify, test each search source with a variety of keywords as a user with low permissions.

**Note:** Only set search facets for indexed fields. Fields that are not indexed may take longer to return results and are not optimized for a fast search experience. Learn more: [Configure a table for indexing and searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-single-table-for-indexing.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Search Sources**.

2.  Open or create a simple search source.

    Simple search sources do not use a data fetch script. Rather, they define a table as the source of searchable data. To learn more about search sources, see [Configuring search in a portal](../concept/search-service-portal.md).

3.  Select the **Facets** related list.

4.  Click **New**.

    The Facet form displays.

5.  Complete the fields.

<table id="table_xgn_dhj_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the facet header.

</td></tr><tr><td>

Application

</td><td>

Application scope of the search source. This value is read-only.

</td></tr><tr><td>

Selection type

</td><td>

Type of user selection allowed:-   **Single**: Only one filter value can be selected at a time. For example, if a facet is created for the **Assigned to** field, the end user can select **Fred Luddy** or **Beth Anglin**, but not both at the same time. Before filtering for a new value, the user must first clear the current value.
-   **Multiple**: Multiple filter values can be selected at the same time. For example, if a facet is created for the **Assigned to** field, the end user can select both **Fred Luddy** and **Beth Anglin**. Because multi choice results in an OR query, records assigned to either Fred Luddy or Beth Anglin display.


</td></tr><tr><td>

Active

</td><td>

Whether the filter option displays in search results.

</td></tr><tr><td>

Use mapped facet filters

</td><td>

Maps a facet to a query condition, such as **\[Updated\]\[After\]\[Last week\]**. When selected, the **Fields** and **Sort** fields are removed from the form. After saving, define filters in the Facet Filters related list.

</td></tr><tr><td>

Order

</td><td>

Defines the display order when multiple facets are defined. If some facets do not have an order value defined, facets with an order defined display first. Facets without an order defined are displayed alphabetically.

</td></tr><tr><td>

Table

</td><td>

Table that the query is created for. This value is read-only and defined by the table used in the search source.

</td></tr><tr><td>

Field

</td><td>

Field that end users can filter search results by. For example, if **Active** is selected, the user can filter search results by true or false.

 Only fields of the following types are supported: True/False, Choice, Decimal, Floating Point Number, Integer, IP Address, Long, Reference, String, String \(Full UTF-8\), and URL.

</td></tr><tr><td>

Sort

</td><td>

Determines the order in which filter options display. -   **Ascending**: Sorts filter options from A to Z when alphabetical, and from lowest to highest when numerical. This is the default option.
-   **Descending**: Sorts filter options from Z to A when alphabetical, and from highest to lowest when numerical.


</td></tr></tbody>
</table>6.  Save the record.

    If **Use mapped facet filters** is selected, the **Facet Filters** related list appears in the facet form.

7.  If **Use mapped facet filters** is selected, define facet filters.

    Map facet filters map a query condition to a facet label. When the end user selects the label from the facet list, the defined query executes.

    1.  In the **Facet Filters** related list, click **New**.

        The Mapped Facet Form appears.

    2.  Define the facet filter fields.

<table id="table_gps_yjj_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the facet filter option.

</td></tr><tr><td>

Order

</td><td>

Defines the display order when multiple facet filters are defined. If some facet filters do not have an order value defined, facets filters with an order defined display first. Facet filters without an order defined are displayed alphabetically.

</td></tr><tr><td>

Application

</td><td>

The application scope of the search source. This value is read-only.

</td></tr><tr><td>

Facet

</td><td>

The search facet that uses the mapped query. This value is read-only.

</td></tr><tr><td>

Table

</td><td>

The table defined in the search facet. This value is read-only.

</td></tr><tr><td>

Mapped query

</td><td>

A query condition that users can set to filter search results. For example, **\[Updated\]\[On\]\[Today\]**.

</td></tr></tbody>
</table>    3.  Click **Submit**.

        Users can filter search results based on the query defined.


**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

