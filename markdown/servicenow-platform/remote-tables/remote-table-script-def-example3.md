---
title: Example 3: Insert a record in an external source
description: In this example, we create a script to insert an incident record into the external source.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create script definitions, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Example 3: Insert a record in an external source

In this example, we create a script to insert an incident record into the external source.

For Remote Table API information, refer to:

-   [v\_query – Scoped, Global](https://www.servicenow.com/docs/access?context=v_queryAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [v\_table – Scoped, Global](https://www.servicenow.com/docs/access?context=v_tableAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

```javascript
(function executeInsert(v_record) {
	var gr = new GlideRecord("incident");
	gr.setNewGuidValue(v_record.sys_id);

	delete v_record["sys_id"];
	gr.number = v_record.u_number;
	gr.short_description = v_record.u_short_description;
	if (!gr.insert()) {
		v_record.setLastErrorMessage("Error on insert: " + gr.getLastErrorMessage());
	}
})(v_record);
```

**Parent Topic:**[Create script definitions for a remote table](../task/create-remote-table-script.md)

