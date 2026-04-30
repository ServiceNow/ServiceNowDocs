---
title: Example 5: Delete a record in an external source
description: In this example, we create a script to delete an incident record from the external source.
locale: en-US
release: yokohama
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create script definitions for a remote table, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 5: Delete a record in an external source

In this example, we create a script to delete an incident record from the external source.

For Remote Table API information, refer to:

-   [v\_query – Scoped, Global](https://www.servicenow.com/docs/access?context=v_queryAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [v\_table – Scoped, Global](https://www.servicenow.com/docs/access?context=v_tableAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

```javascript
(function executeDelete(v_record) {

     var gr = new GlideRecord('incident');
     if (gr.get(v_record.sys_id)) {
         gr.deleteRecord();
     } else {
         v_record.setLastErrorMessage("Record not found");
     }
 })(v_record);
```

**Parent Topic:**[Create script definitions for a remote table](../task/create-remote-table-script.md)

