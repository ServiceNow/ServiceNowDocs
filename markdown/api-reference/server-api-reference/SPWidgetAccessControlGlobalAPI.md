---
title: SPWidgetAccessControl - Global
description: The SPWidgetAccessControl script include provides methods that allow administrators to check whether a provided table is granted public access to a widget and is securely accessed by an intended audience.Instantiates the SPWidgetAccessControl object.Returns information about whether a specified table has public access to a widget.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SPWidgetAccessControl- Global

The SPWidgetAccessControl script include provides methods that allow administrators to check whether a provided table is granted public access to a widget and is securely accessed by an intended audience.

For details and instructions about using the SPWidgetAccessControl API in your server script, see Configure widget security \(Restrict which tables public widgets can access for guest users\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SPWidgetAccessControl – SPWidgetAccessControl\(\)

Instantiates the SPWidgetAccessControl object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to initialize a new SPWidgetAccessControl object.

```
new global.SPWidgetAccessControl()
```

## SPWidgetAccessControl – hasPublicAccess\(String tableName, Object SPScriptable, String options, Object input\)

Returns information about whether a specified table has public access to a widget.

<table id="table_yjp_zpz_31b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Required. Name of the table to query. For example, enter `incident` to query the Incident \[Incident\] table.

</td></tr><tr><td>

SPScriptable

</td><td>

Scriptable Object

</td><td>

Required. Widget's SP Scriptable. Formatted as `$sp` in the request.```
SPScriptable:{
"widgetSysId":widget sys_id,
"request":request object
}
```

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. Widget/rectangle options passed in the widget.```
"options":{
"table":"incident", "maximum_entries": "10"
}

```

</td></tr><tr><td>

input

</td><td>

Object

</td><td>

Optional. Widget/rectangle input passed during runtime.```
"input":{
"table":"incident", 
"display_field":"name"
}
```

</td></tr></tbody>
</table><table id="table_zjp_zpz_31b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the widget access status of the specified table. Possible values:-   true: The provided table is granted security access on the widget.
-   false: The provided table is not granted security access on the widget.

Default: false

</td></tr></tbody>
</table>The following example shows confirmation that the Incident table has access to the Simple List Widget as shown in the configuration table, m2m\_sp\_public\_widget\_allow\_table.

```
options.table = "incident";
//$sp,options,input - which are available by default in any widget script
new global.SPWidgetAccessControl().hasPublicAccess(options.table, $sp, options, input);
```

Output:

```
true
```

