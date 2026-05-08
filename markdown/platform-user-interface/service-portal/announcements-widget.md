---
title: Announcements widget
description: Users can view all active announcements. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Announcements widget

Users can view all active announcements. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

This widget lists the active announcements for a portal from the Announcement \[announcement\] table. To see the list of active announcements, navigate to **All** &gt; **Service Portal** &gt; **Announcements**. For information about creating announcements, see [Create an announcement](../task/create-announcement.md).

![](../image/announcement-widget.png "Announcements widget")

## Instance options

<table id="table_yj5_ld2_r1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select the type of announcements to display. Announcement types can be selected in the announcement record. Choices include:-   Banner
-   Widget

 If a type is not defined, the widget instance displays all active announcements.

</td></tr><tr><td>

Title

</td><td>

Widget header title.

</td></tr><tr><td>

Glyph

</td><td>

Glyph displayed to the left of the title.

</td></tr><tr><td>

Use Display Style

</td><td>

If selected, each announcement displays according to the style defined in the announcement record. Before selecting this option, consider how the widget will display if multiple announcements in the widget use different styles.

</td></tr><tr><td>

Paginate

</td><td>

Paginates multiple announcements.

</td></tr><tr><td>

Max Records

</td><td>

Number of announcements displayed per page.

</td></tr><tr><td>

View All Page

</td><td>

Select target for **View all** link. The **View all** link only displays when: -   There are more announcements than can be displayed on a single page. The **Max Records** field defines the number of records displayed per page.
-   A view all page is defined.

</td></tr><tr><td>

Who Can View Instances \| Who Cannot View Instances

</td><td>

Control who can and cannot view a widget instance with [user criteria](user-criteria.md). This option appears when user criteria for the Service Portal is activated.

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

