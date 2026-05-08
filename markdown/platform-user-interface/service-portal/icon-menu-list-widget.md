---
title: Icon menu list widget
description: A simple list with a glyph icon next to each link. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Icon menu list widget

A simple list with a glyph icon next to each link. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

Configure the icon information using the Menu Items related list.

![Icon Menu list widget with icons for profile, group information, and credit card information](../image/WidgetIconMenuList.png "Icon Menu list widget")

1.  From the instance options for the icon menu list widget, under Related Lists, click **Menu Items**.
2.  Click **New**.
3.  Use the fields on the New Menu Items form to configure the icons for the icon menu list widget.

|Field|Description|
|-----|-----------|
|Label|Name or description of the icon|
|Parent Menu|The name of the menu that the icon appears in. This automatically populates with the name of the icon menu list widget that you created but you have the option to switch it to another menu.|
|Order|The order in which the icons appear in the icon menu list widget.|
|Parent menu Item|Nest menu items within a parent menu.|
|Page|The page within Service Portal that the icon links to. Select **Page** from the Type list to enable this option.|
|Type|Select the type of link you want the icon to have. You can link to pages within Service Portal, external URLs, KB articles, Service Catalog, or lists. Different fields will appear on the form depending on the option you select from the list.|
|Condition|Determines what conditions are required for menu items to show in the header. For more information on what conditions to use in the **Condition** field, see [Create a UI Action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=australia&pubname=australia-platform-administration&ft:locale=en-US) [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=australia&pubname=australia-platform-administration&ft:locale=en-US).|
|Glyph|Icon that you want to display in the icon menu list widget.|

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

