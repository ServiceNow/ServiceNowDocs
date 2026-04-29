---
title: Portal Case Cards widget instance options form
description: Instance options enable you to configure the Portal Case Cards widget on a portal page.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configurable Portal widgets instance options, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Case Cards widget instance options form

Instance options enable you to configure the Portal Case Cards widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case Table

</td><td>

Table from which the records shown as case cards on the widget are selected.By default, this field is set to the Cases \[sn\_customerservice\_case\] table and the extended table is Complaint Case \[sn\_complaint\_case\].

</td></tr><tr><td>

Query

</td><td>

Query to filter the case records.The default query shows cases that are awaiting information or are resolved.

**Note:** If no query is provided, all case records are displayed in the widget. For more information, see [Generate an encoded query string through a filter](https://www.servicenow.com/docs/access?context=t_GenEncodQueryStringFilter&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Sort by

</td><td>

Field in the Cases \[sn\_customerservice\_case\] table that determines the field by which cases are sorted when displayed on the widget. The default value is Last updated.

</td></tr><tr><td>

Sort Order

</td><td>

The order in which the cases appear on the widget.The available options are:

-   z to a
-   a to z

The default sort order is z to a.

**Note:** Currently, if you select None, the order is set to z to a.

</td></tr></tbody>
</table>|Instance option|Description|
|---------------|-----------|
|Title|Required title of a Portal Case cards widget. The default text is `Track case updates`.|
|Description|Subtitle that appears below the heading.|

<table id="table_y1f_rt5_2zb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max Cases to Display

</td><td>

Number of cases to appear by default on the widget. The default value is 10.

</td></tr><tr><td>

Card Title

</td><td>

Required title of the Case Cards widget.

</td></tr><tr><td>

State Highlight Color

</td><td>

Color of the background and text for the different states of a case in hex code format.

</td></tr><tr><td>

Card Display style

</td><td>

Display style for a case card inside the widget.The available options are:

-   Show case fields
-   Show latest activity
-   Title only

The default display style is Show the latest activity

**Note:** Currently, if you select None, the display style is set to Show latest activity.

</td></tr><tr><td>

Select Case Fields

</td><td>

Display case fields for a case card in the widget, which are chosen from a set of predefined set of fields in the Cases \[sn\_customerservice\_case\] table.You can show a maximum of three fields.

This field is available only when **Show case fields** is selected from **Card display style**.

</td></tr><tr><td>

Case View Page

</td><td>

The portal page that displays the details of a case record when the case card is accessed.By default, this field is set to the Case \(csm\_ticket\) page.

</td></tr><tr><td>

View All Page

</td><td>

Option to display all cases when **View all** is accessed on the widget.The **View all** option on the Portal Case Cards widget is displayed under the following conditions:

-   The number of cases resulting from the query provided in the **Query** field is more than the defined value in the **Max Cases to Display** field
-   A page has been selected from a set of predefined set of pages

</td></tr><tr><td>

Hide Empty Case Widget

</td><td>

Option to hide the widget when no records are available to display. If this option isn’t selected, an empty widget shows the text defined in the **Empty State Text** option.

</td></tr><tr><td>

Empty State Text

</td><td>

The text displayed in the widget when **Hide Empty Case Widget** isn’t selected and the widget has no records to display. The default text is `No updates right now`.

</td></tr></tbody>
</table>**Related topics**  


[Add and configure the Portal Case Cards widget](../task/portal-case-card-widget-inst-optns.md)

[Display the integer values of all case states](../task/integer-value-case-states.md)

