---
title: Dynamic actions script for list context menus
description: The Dynamic actions script field, on the Context Menu form, defines a script. The script populates a list context menu with dynamic options, such as filters or views.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customize list context menus, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic actions script for list context menus

The **Dynamic actions script** field, on the Context Menu form, defines a script. The script populates a list context menu with dynamic options, such as filters or views.

The following JavaScript variables are available to the dynamic actions script when it is executed.

|Variable|Description|
|--------|-----------|
|g\_tableName|Name of the current table.|
|g\_listId|ID of the list for which the context menu is built.|
|g\_itemName|Name defined in the UI context menu record.|
|g\_itemOrder|Order defined in the UI context menu record. Use this variable to pass the value of the **Order** field to the dynamic actions script.|
|g\_contextMenu.addAction\(item\_id, label, script\_string, order\)|Add options to the context menu and select the order in which they appear.|

The following example displays a list title menu item that controls the number of records per page in the list view.

```
g_contextMenu.addAction('50', g_itemName, 'showRowsPerPage("50");', g_itemOrder);
```

**Note:** The action script for this item must define the showRowsPerPage function so that when selecting this menu item, that function is called with an argument of 50.

**Parent Topic:**[Customize list context menus](../task/t_CreateAContextMenu.md)

