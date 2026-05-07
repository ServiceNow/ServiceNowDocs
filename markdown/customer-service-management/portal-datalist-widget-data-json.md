---
title: Portal Data List widget JSON parameters
description: JSON parameters define aspects of the Portal Data list widget on the portal page.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [JSON parameter in Configurable Portal Widgets, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Data List widget JSON parameters

JSON parameters define aspects of the Portal Data list widget on the portal page.

**Note:** This information assumes that you’re familiar with the JSON code format.

<table id="table_csm_base_entities"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

categories

</td><td>

Each category displays a set of records from the Customer Case View Case \[sn\_customerservice\_case\] table that meets the filter criteria.For each category, you can choose from pre\_defined\_filters and run\_time\_filters predefined filter tabs, set the columns for the list view, and determine the fields to be shown in the card view.

</td></tr><tr><td>

ID

</td><td>

A unique identifier that enables the categories condition script to determine whether to show or hide categories on the widget.

</td></tr><tr><td>

label

</td><td>

Name of the category that appears on the navigation pane.If a label isn’t entered, the category doesn't appear.

</td></tr><tr><td>

table

</td><td>

The table from which the records are shown on the widget when a category is selected.By default, this field is set to the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

list\_view

</td><td>

The name of the view that defines the list of columns or fields to appear on the widget.For more information on these views, see [Create and delete views](https://www.servicenow.com/docs/access?context=create-delete-view&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

If no value is provided, all columns are shown.

</td></tr><tr><td>

card\_view\_primary\_column

</td><td>

A field from the defined table to be displayed in the first column of a card. For example, you can show the case number in the first column.

</td></tr><tr><td>

card\_view\_secondary\_column

</td><td>

A field from the defined table to be displayed in the second column of a card. For example, you can show short description of the case record.This parameter is optional.

</td></tr><tr><td>

card\_view\_additional\_columns":"column1\|column2\|column3\|column4

</td><td>

Field pairs from the defined table to be displayed as additional columns of a card.You can add a maximum of four additional columns.

This parameter is optional.

</td></tr><tr><td>

query":"active=true"

</td><td>

Query to filter the records that display under the category.If no value is provided, all records are displayed.

</td></tr><tr><td>

glyph":"glyph\_name"

</td><td>

The glyph to appear on the left of the category label in the navigation pane. The glyph name provided should be from the font-awesome library, which can be accessed at the following URL:

```
https://fontawesome.com/v4/icons/
```

The currently supported version of the font-awesome library is v4.7. If you use a glyph name from a different version, the image will not appear correctly.

**Note:** If both a glyph and an image are defined, the image is displayed.

This parameter is optional.

</td></tr><tr><td>

"image\_name":"file\_img"

</td><td>

An image to appear on the left of the category. The image name should be selected from the Images \[db\_image\] table.

**Note:** If both a glyph and an image are defined, the image is displayed.

This parameter is optional.

</td></tr><tr><td>

record\_view\_page

</td><td>

The Service Portal that displays the page with details of any record accessed in the widget.This parameter is optional.

By default, this field is set to the Case \(csm\_ticket\) page.

</td></tr><tr><td>

pre\_defined\_filters"filter\_name":"Value",

</td><td>

Display cases which are in New, Closed, Open, or Awaiting Info state in any selected category. These filters appear as tabs in the widget. Only Open and Closed case are included by default in the JSON code. The available values are:-   filter\_name: Name of the filter tab
-   Value: Name of the case state such as New, Closed, Open, or Awaiting Info.

This parameter is optional.

</td></tr><tr><td>

run\_time\_filters

</td><td>

Displays column and its fields from the defined table as runtime filters in a drop-down list. These runtime filters filter the case records displayed in the widget based on different fields from the defined table. For example, you can display Priority as a column and State, Contact, or Updated as fields. If the runtime filters values are not provided in the column and selection\_type parameters, the filter icon will not appear for the category.

This parameter is optional.

</td></tr><tr><td>

selection\_type

</td><td>

Display the type of selection. The available options are:-   Single select: Single selection for the filter column
-   Multi select: Multiple selection values for the filter columns

</td></tr><tr><td>

values"value":"4"

</td><td>

Values from the defined table for the column parameter. The available values are:-   Label: Name of a value
-   Value: Integer value of a field

</td></tr><tr><td>

"ranges":"label":"Last Month", "query":"&lt;Range condition&gt;",

</td><td>

Used to filter the records using a query defined in label and query parameters. For example, you can display case records that have been updated in the last month, last 3 months, or last 6 months.The range configuration is:

-   Label: Name of the filter option
-   Query: Query that defines a set of values grouped under a label

This parameter is optional.

</td></tr><tr><td>

```
"role_based_views":
{
"field_service_agent_view":"snc_field_technician",
"agent_case_view":["snc_customer_service_agent","snc_manager"]
}
```

</td><td>

Used to display data list according to the role of the logged in user. List the roles in an array to map multiple roles to the same view. All roles in that array share the same view.

For example, if you want both support agents and service managers to see the same case view, assign the same view \(such as `"agent_case_view"`\) to both roles within an array.

When a user has multiple roles the system uses the first matching view it finds.

This parameter is optional.

</td></tr><tr><td>

"guest\_view":"viewname

</td><td>

Used to display items for guest users or not logged in users. Map the view you want to display for the guest users.To make the items available to guest users, you must set these to public:

-   Portal Data List widget.
-   Page containing widget \(For example, Cases and Tasks\)
-   Page content instance

For details, see [Configure public access on the Portal Data List widget](../task/config-data-list-widget-inst-guest-access.md).

This parameter is optional.

</td></tr><tr><td>

"sort\_by":"&lt;column name&gt;"

</td><td>

Used for first‑load sorting of Data List.This parameter is optional.

</td></tr><tr><td>

"sort\_order":"&lt;asc/desc&gt;"

</td><td>

Order of sorting the data list. Default is ascending.This parameter is optional.

</td></tr></tbody>
</table>**Related topics**  


[Add and configure the Portal Data List widget](../task/config-data-list-widget-inst-optns.md)

