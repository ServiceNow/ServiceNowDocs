---
title: Navigation handler
description: A navigation handler is a scripted view rule and runs each time data from the specified table is requested in the form view.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View management, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Navigation handler

A navigation handler is a scripted view rule and runs each time data from the specified table is requested in the form view.

## Create a navigation handler

The Navigation Handler \[sys\_navigator\] table contains the navigation handlers on your instance. Access this table by entering `sys_navigator.list` in the filter navigator. Navigation handler records contain a **Table** field to specify which table the navigation handler applies to, and a **Script** field containing the scripted view rule.

The following script comes from navigation handler included with the HR plugin. The script forces records from the table in the **Table** field to use ESS view for users with no roles, and default view for all other users.

```
var now_GR = new GlideRecord(hr.TABLE_CASE);  
if (gr.get(g_uri.get('sys_id'))) {  
     if (!gs.getUser().hasRoles())   
          g_uri.set('sysparm_view', 'ess');  
     else  
          g_uri.set('sysparm_view', '');  
}  
  
  
answer =  g_uri.toString('hr_case.do'); 
```

## Run navigation handlers before or after view rules

Use the **glide.ui.view\_rule.check\_after\_nav\_handler** system property to control the order in which view rules and navigation handlers are applied. Set the property value to **True** to process view rules after navigation handlers. If the system property does not exist in your instance, the navigation handler always takes precedence.

The system property only overrides the navigation handler if the navigation handler scripted function does not return an answer. In the example script above, the property has no effect. This is because this navigation handler always returns an answer due to the `answer` line being outside of the `if` statement.

To force the navigation handler script in the preceding example to honor view rules, take the following steps:

1.  Create the **glide.ui.view\_rule.check\_after\_nav\_handler** system property.
2.  Set the value of the property to `true`.
3.  Update the navigation handler script to only return an `answer` when the view must be changed or forced.

This example is a modified version of the previous script. In this case, the `answer` line only occurs when the user has no roles. If the user has roles, `answer` is never reached, and view rules on the same table, if any, are applied.

```
var now_GR = new GlideRecord(hr.TABLE_CASE);  
if (gr.get(g_url.get('sys_id'))) {  
     if (!gs.getUser().hasRoles()) {  
          g_url.set('sysparm_view'),'ess');  
          answer = g_url.toString('hr_case.do');  
     }  
} 
```

**Parent Topic:**[View management](view-management-overview.md)

