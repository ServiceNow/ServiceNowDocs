---
title: Example 4: Update a record in an external source
description: In this example, we create a script to update an incident record in the external source.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create script definitions, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 4: Update a record in an external source

In this example, we create a script to update an incident record in the external source.

**Note:** If multiple users update the same record at the same time, the value on the remote system is from the last update call executed.

For Remote Table API information, refer to:

-   [v\_query – Scoped, Global](https://www.servicenow.com/docs/access?context=v_queryAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [v\_table – Scoped, Global](https://www.servicenow.com/docs/access?context=v_tableAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

v\_changed\_fields is a map of changed field names and values.

```javascript
(function executeUpdate(v_record, v_changed_fields) {

	var gr = new GlideRecord('incident');
	if (gr.get(v_changed_fields.sys_id)) {
		Object.keys(v_changed_fields).map(function(k) {
				switch (k){
				case "u_number" :
					gr.number = v_changed_fields.u_number;
					break;
				case "u_short_description" :
					gr.short_description = v_changed_fields.u_short_description;
					break;
			}
		});
	gr.update();
} else {
	v_record.setLastErrorMessage("Missing record to update, " + v_changed_fields.sys_id);
}

})(v_record, v_changed_fields);
```

**Parent Topic:**[Create script definitions for a remote table](../task/create-remote-table-script.md)

