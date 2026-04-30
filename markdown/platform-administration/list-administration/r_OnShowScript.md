---
title: onShow script for list context menus
description: The onShow script field defines a script that runs before the context menu is displayed to determine which options appear in the context menu.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List context menus, Administer, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# onShow script for list context menus

The **onShow script** field defines a script that runs before the context menu is displayed to determine which options appear in the context menu.

Use this script to change the menu items on the list header menu based on the current field column. The following JavaScript variables are available to the onShow script when it is executed:

|Variable|Description|
|--------|-----------|
|g\_menu|Context menu to be displayed.|
|g\_item|Current context menu item.|
|g\_list|GlideList2 against which the script runs.|
|g\_fieldName|Name of the field against which the context menu runs.|
|g\_fieldLabel|Label of the field against which the context menu runs.|
|g\_sysId|The sys\_id of the row or form against which the script runs.|

An example of an onShow script is one that determines when to enable or disable the **Ungroup** option in a list column heading menu based on whether the list is grouped or not.

```
if (g_list.getGroupBy()) {
   // list is grouped so enable to Ungroup menu item
   g_menu.setEnabled(g_item);
} else {
   // list is not grouped, so disable the Ungroup menu item
   g_menu.setDisabled(g_item);
}
```

