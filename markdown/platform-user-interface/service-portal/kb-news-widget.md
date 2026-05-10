---
title: KB News widget
description: The KB News widget displays information from the Knowledge Base. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# KB News widget

The KB News widget displays information from the Knowledge Base. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

You can configure the KB News widget to display specific information by selecting a category from the KB category list.

**Note:** The KB News widget only displays the knowledge base articles a user has access to based on ACL rules.

![KB News widget with announcements about service interruptions](../image/WidgetKBNews.png "KB News widget")

## Instance options

![KB news widget instance options with four options listed](../image/IOKBNews.png "KB news widget instance options")

<table id="table_rjn_sx4_j1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the widget that appears in the widget header

</td></tr><tr><td>

Bootstrap color

</td><td>

Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.

</td></tr><tr><td>

Max number

</td><td>

The maximum number of news articles appearing in the widget. The default number is 5.**Note:** If a user does not have access to articles based on ACL rules, the widget can display fewer articles than the maximum number.

</td></tr><tr><td>

KB category

</td><td>

The knowledge base category determined by the kb\_category table. Only published articles display. For a news widget, select something like **Announcements** to show upcoming events.

</td></tr></tbody>
</table>**Parent Topic:**[Knowledge Management widgets](km-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

