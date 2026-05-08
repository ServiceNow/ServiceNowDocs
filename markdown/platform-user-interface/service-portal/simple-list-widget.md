---
title: Simple List widget
description: The Simple List widget can be used to display any list in the system within Service Portal. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Simple List widget

The Simple List widget can be used to display any list in the system within Service Portal. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Simple List widget](../image/WidgetSimpleList.png "Simple List widget")

## Instance options

<table id="table_lgf_x32_k1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The platform table that the simple list is formed from.

</td></tr><tr><td>

Filter

</td><td>

Conditions that are applied to the list. To edit the filter, in the widget instance options context menu, select **Open in platform**. Use the Table &amp; Filter tab to apply conditions to the simple list. For more information, see [Create a filter in List](../../../use/using-lists/task/t_CreatingFilters.md).

</td></tr><tr><td>

Display field

</td><td>

Main field that displays as the "title" of the list item.

</td></tr><tr><td>

Secondary fields

</td><td>

Fields from the list item that display in addition to the main display field.

</td></tr><tr><td>

List page

</td><td>

The page that opens when a user selects **View all** in the widget footer. Select a page that correlates with the items that display in the list.

</td></tr><tr><td>

Enforce field-level Read ACLs on Filter query terms \(may alter the query for unprivileged users\)

</td><td>

Enforce read ACL rules for fields included in filter conditions applied to the list.**Note:** When the **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** system property is set to true, read ACLs are enforced for Simple List filter conditions always.

</td></tr><tr><td>

Link to this page

</td><td>

Portal page to link to from a list item.

</td></tr><tr><td>

Show even when empty

</td><td>

Widgets are designed to hide on a page when no results meet the criteria. Select this option to make the simple list widget display on a page even when empty.

</td></tr><tr><td>

View

</td><td>

The view option for when a list item links to a form. The **Link to this page** field must be set to a form page for this option to work.

</td></tr><tr><td>

Disable record watcher

</td><td>

Turn off automatically updating the list based on changes to the filtered records.

</td></tr><tr><td>

Glyph

</td><td>

Icon that displays next to the widget name in the header

</td></tr><tr><td>

Bootstrap color

</td><td>

Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.

</td></tr><tr><td>

Bootstrap size

</td><td>

Size of the widget

</td></tr><tr><td>

Maximum entries

</td><td>

Maximum allowed number of entries that appear in the list at one time.

</td></tr><tr><td>

List body height

</td><td>

Actual length of the widget in pixels or EMs. A long list with a small body height includes a scroll bar option.

</td></tr><tr><td>

Image field

</td><td>

Displays an image in the list. Select a field type that includes an image. For example, Photo.

</td></tr><tr><td>

Rounded images

</td><td>

Makes any images selected in the Image field round in the list.

</td></tr><tr><td>

Hide footer

</td><td>

Show or hide the widget footer

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

