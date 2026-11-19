---
title: Example 5: Delete a record in an external source
description: In this example, we create a script to delete an incident record from the external source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/remote-tables/remote-table-script-def-example5.html
release: zurich
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create script definitions, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 5: Delete a record in an external source

In this example, we create a script to delete an incident record from the external source.

For Remote Table API information, refer to:

-   [v\_query – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/v_queryAPI.md)
-   [v\_record - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/v_recordAPI.md)
-   [v\_table – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/v_tableAPI.md)

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

**Parent Topic:**[Create script definitions for a remote table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/remote-tables/create-remote-table-script.md)

