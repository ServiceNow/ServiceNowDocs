---
title: Action script for list context menus
description: The Action script field, on the Context Menu form, defines a script. The script runs when someone selects the context menu option.
locale: en-US
release: australia
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List context menus, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Action script for list context menus

The **Action script** field, on the Context Menu form, defines a script. The script runs when someone selects the context menu option.

This script is client-side and runs in the user's browser. The following JavaScript variables are available to the Action script when it is executed.

|Variable|Description|
|--------|-----------|
|g\_list|GlideList2 against which the script runs.|
|g\_fieldName|Name of the field against which the context menu runs.|
|g\_fieldLabel|Label of the field against which the context menu runs.|
|g\_sysId|The sys\_id of the row or form against which the script runs.|

The base system uses the following code in an action script to refresh the platform view.

```
g_list.refresh(1);
```

Another example is the use of these variables in a list header menu to sort a list by the selected field in descending order \(z to a\).

```
g_list.sortDescending(g_fieldName);
```

