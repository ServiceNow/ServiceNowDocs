---
title: Component properties for the Case list
description: Component properties enable you to configure the behavior of the Case list component instance on a third-party website.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Web Embeddables component properties, Web Embeddables reference, Reference, Customer Service Management]
---

# Component properties for the Case list

Component properties enable you to configure the behavior of the Case list component instance on a third-party website.

<table id="table_csm_base_entities"><thead><tr><th>

Component property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide header

</td><td>

Option to display header and its components. By default, it shows header.

</td></tr><tr><td>

Title

</td><td>

Required title of the Case list component.

</td></tr><tr><td>

Hide record count

</td><td>

Option switch to show or hide the total number of records on the case list. By default, it shows record count.

</td></tr><tr><td>

Hide search

</td><td>

Option switch to show or hide search button on the header. Use the Hide search option to search the case within the case list.By default, it shows search button.

</td></tr><tr><td>

Show filters

</td><td>

Option to show or hide filter button on the header. Use this option to customize the display of cases according to pre-defined filters.By default, it hides filter button.

</td></tr><tr><td>

Hide refresh

</td><td>

Option to show or hide the refresh button the header. Use this option to refresh the case list.By default, it shows a refresh button.

</td></tr><tr><td>

Hide last refreshed text

</td><td>

Option to show or hide a message on the header. Use this option to indicate when the last refresh occurred.By default, it shows last refreshed text.

</td></tr><tr><td>

Table

</td><td>

Table from which the cases or tasks shown on the Case list component. By default, this field is set to the Case \[sn\_customerservice\_case\] table.

**Note:** Case list component can show the records from any extended table of case or task table.

</td></tr><tr><td>

Query

</td><td>

Query to filter the case records. The default query shows all cases.

**Note:** If no query is provided, all case records are displayed in the Case list component. For more information, see [Generate an encoded query string through a filter](https://www.servicenow.com/docs/access?context=t_GenEncodQueryStringFilter&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

View

</td><td>

Display style for the cases inside the component, chosen from the predefined views.

</td></tr><tr><td>

Columns

</td><td>

Display columns from the case or task table. Select **Add** to add new columns to the case list table.

 Select \(![edit icon](../image/edit-new.png)\) to update and select \(![Remove icon](../../hs-risk-management/image/icon-remove.png)\) to remove column from the case list on the column cards.

**Note:**

-   If both the View and Columns attributes are provided, the fields specified in Columns will be displayed.
-   If the first column is the reference column, selecting on the case record shows the error in the Case View component.

</td></tr><tr><td>

Disable column resizing

</td><td>

Option to adjust the column width. By default, column resizing is enabled.

</td></tr><tr><td>

Records per page

</td><td>

Option to show or hide the number of records that appear by default on the case list. The default value is 20.

</td></tr><tr><td>

Hide errors

</td><td>

Option to show or hide error messages for the end user on the third-party website. By default, it shows errors.

</td></tr><tr><td>

Hide when empty

</td><td>

Option to show or hide the component when there are no cases to display. By default, it shows empty list when there are no cases.

**Note:** This property is honored when the component initially loads. If no matching records are found for searches or query filters afterward, an empty state is shown regardless of the attribute's value.

</td></tr></tbody>
</table>**Related topics**  


[Configure the Case list component instance](../task/configure-case-list-component-on-instance.md)

[Embed the Case list component instance on the third-party website](../task/embed-case-list-component-on-third-party-website.md)

[Event handler in the Case list component](we-case-list-event-handlers.md)

[Sample code for the Case list component](we-case-list-sample-code.md)

