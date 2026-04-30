---
title: ConnectActionResponse - Global
description: The ConnectActionResponse API provides a method to create a glide record.Create a GlideRecord in the specified table with the specified values.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ConnectActionResponse- Global

The ConnectActionResponse API provides a method to create a glide record.

The ConnectActionResponse methods are accessed through a global object \(response\) that is available only in Connect action scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ConnectActionResponse - newRecord\(String table, Object values, String view\)

Create a GlideRecord in the specified table with the specified values.

Opens a form in the UI based upon the table, which replaces the **Table** and **Document** fields in the Live Group Profile record for the associated conversation.

|Name|Type|Description|
|----|----|-----------|
|table|String|Name of the table where the record is to be added.|
|values|Object|An object of name value pairs where the names are field names in the table and the values are the field values.|
|view|String|The form view to load. This parameter is optional.|

|Type|Description|
|----|-----------|
|void| |

```
response.newRecord("incident", {
	short_description: conversation.document.short_description || "",
	caller_id: conversation.document.opened_by
});
```

