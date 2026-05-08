---
title: Filters
description: A filter restricts what records appear in a list by providing a set of conditions each record must meet to be included in the list.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Filters

A filter restricts what records appear in a list by providing a set of conditions each record must meet to be included in the list.

A condition consists of the following parts.

-   Field: Each field contains data from a particular column in the table. Selecting a reference field enables you to dot-walk to data from other tables.
-   Operator: Each field type has its own set of valid operators. The operator determines if a value is needed.
-   Value: Each field has its own set of valid values determined by the field type. Reference fields have access to auto-complete, and choice lists provide a list of options.
-   Grouping: Each condition line is grouped with either an AND or OR connector. The filter requires all condition lines linked with an AND connector to be met. The filter separately evaluates each condition line linked with an OR connector.

List v3 provides the Related Lists Conditions section that enables you to include a condition based on a related table.

**Note:** If you open a list for a table you have create permissions for, apply a filter for a field, and click **New** in the list header. The same field is automatically populated with the value you set in the filter on the new record.

Create filters on a list using the condition builder.

## Related list conditions in List v3

By default, all lists enables you to filter on the current table data, which includes dot-walking to fields in referenced tables. In v3 lists, another type of condition, Related Lists Conditions, is available in the condition builder. For more information, see [Add related list conditions](../../using-lists-v3/task/create-related-list-query.md).

## Pin a filter in List v2

To make the condition builder appear every time you open the list, click the pin/unpin filter icon \(![Pin icon for Core UI](../image/Icon-Pin_UI15.png)\). This functionality is not supported in List v3.

-   **[Create a filter in List](../task/t_CreatingFilters.md)**  
You can create a filter to restrict what records appear in a list by providing a set of conditions. When you run the filter, only records that meet the specified conditions are listed.
-   **[Add related list conditions](../../using-lists-v3/task/create-related-list-query.md)**  
Related list conditions allow you to include a relationship with another table in the filter. Related list conditions are supported in both List v3 and the Report interface.
-   **[OR conditions](c_UsingORConditions.md)**  
The condition builder uses two different types of OR conditions: top-level and dependent.
-   **[Filter on multiple string values](../task/t_FilteringOnMultipleStringValues.md)**  
For a string field, you can create a filter that searches for multiple values by creating a comma-delimited list.
-   **[Dynamic operators](../reference/r_UsingTheDynamicOperator.md)**  
The dynamic operator, **is \(dynamic\)**, lists predefined dynamic filter options where the condition value is computed from a value in a reference field.

**Parent Topic:**[Filters and breadcrumbs](c_UsingFiltersAndBreadcrumbs.md)

**Related topics**  


[Dot-walking to data in related tables](../../navigation/concept/c_DotWalking.md)

[bundle-platadm.r_FieldTypes]

[Operators available for filters and queries](../../common-ui-elements/reference/r_OpAvailableFiltersQueries.md)

