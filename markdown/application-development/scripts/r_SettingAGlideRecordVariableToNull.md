---
title: Setting a GlideRecord variable to 'NULL'
description: GlideRecord variables \(including current\) are initially null in the database. Setting these back to an empty string, a space, or the JavaScript null value will not result in a return to this initial state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/scripts/r\_SettingAGlideRecordVariableToNull.html
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Setting a GlideRecord variable to 'NULL'

GlideRecord variables \(including current\) are initially null in the database. Setting these back to an empty string, a space, or the JavaScript null value will not result in a return to this initial state.

**Note:** This functionality requires a knowledge of JavaScript.

To set it back to the initial state, simply set the value to 'NULL'. Note that the update\(\) function does not run on the current object but rather on the record. The object displays the initial value until it is called again from the record.

**Note:** Functionality described here requires the **Admin** role.

## Example 1

```
var grIncident = new GlideRecord('incident');
grIncident.addNotNullQuery("assigned_to");
grIncident.query();
if (grIncident.next()) {
  gs.log(“The incident record that is going to be updated is “ + grIncident.number);
  gs.log("Previous Value of 'Assigned To' field: " + grIncident.assigned_to);
  grIncident.assigned_to = "NULL";
  grIncident.update();
  gs.log("Current Value of 'Assigned To' field: " + grIncident.assigned_to);
}
```

## Example 2 \(Business Rule\)

```
current.u_affected_value = 'NULL';
current.update();
```

**Parent Topic:**[Server-side scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/scripts/c_ServerScripting.md)

