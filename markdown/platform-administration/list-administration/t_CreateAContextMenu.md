---
title: Customize list context menus
description: Customize the content and behavior of list context menus by creating or editing UI context menu records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/t\_CreateAContextMenu.html
release: brazil
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-11-09"
reading_time_minutes: 2
breadcrumb: [Administer, List administration, Forms, fields, and lists, Configure core features, ServiceNow AI Platform]
---

# Customize list context menus

Customize the content and behavior of list context menus by creating or editing UI context menu records.

## Before you begin

Role required: admin

## About this task

For example, you might add an option to the list column heading menu for a specific table. You might also change the roles required to access a global context menu option.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Context Menus**.

2.  Select **New**.

3.  On the Context Menu form, fill in the fields.

<table id="table_bp5_h2r_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table to which this context menu option is attached. The base system menu items are attached to the Global \[global\] table, which applies the context menu option to all lists for all tables. If you specify a particular table, the option is available only on context menus in lists from that table.

 **Note:** The list shows only tables and database views that are in the same scope as the context menu.

</td></tr><tr><td>

Menu

</td><td>

List context menu in which this option appears.

-   List title menus
-   Column headings
-   [List fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/r_Fields.md)


</td></tr><tr><td>

Type

</td><td>

Type of menu option to create:

-   **Action**: A menu option that performs an immediate action.
-   **Menu**: Parent menu that can display a submenu.
-   **Separator**: Line between groups of options on a menu. Menus do not display separator lines next to one another or at the bottom of a menu. If a condition that removes options for a role forces two separators together, one of the separators is removed from the view.
-   **Label**: An unlinked label for a menu or section of a menu.
-   **Dynamic actions**: Menu options dynamically created, such as the available views or user filters that can only be generated at the time the list is displayed.


</td></tr><tr><td>

Name

</td><td>

Label for the action as it appears in the menu.

</td></tr><tr><td>

Parent

</td><td>

If this action is part of a submenu, enter the name of the parent menu item. For example, in the base system, **Configure** is a parent.

</td></tr><tr><td>

Order

</td><td>

Order number for this item, menu, or separator to specify where in the menu it appears.

</td></tr><tr><td>

Active

</td><td>

Option to activate this context menu item. Only active items are shown in the context menu.

</td></tr><tr><td>

Run onShow script

</td><td>

Option to display the **onShow script** field.

</td></tr><tr><td>

Condition

</td><td>

Conditions under which this menu option appears. For example, define the role that has permission to see this item.

</td></tr><tr><td>

Action script

</td><td>

The action script runs when someone selects the context menu option. For more information, see [Action script for list context menus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/list-administration/r_ActionScript.md).

</td></tr><tr><td>

Dynamic actions script

</td><td>

The dynamic actions script populates the context menu with dynamic options, such as filters or views. For more information, see [Dynamic actions script for list context menus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/list-administration/r_DynamicActionsScript.md).

</td></tr><tr><td>

onShow script

</td><td>

The onShow script runs before the context menu is displayed, to determine which options appear in the context menu. For more information, see [onShow script for list context menus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/list-administration/r_OnShowScript.md).

</td></tr></tbody>
</table>4.  Select **Submit**.


