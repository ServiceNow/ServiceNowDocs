---
title: RecordToHTML - Global
description: The RecordToHTML script include is a utility class to turn a record into HTML.Creates an instance of a RecordToHTML class.Sets the specified field to the specified value.Converts a RecordToHTML object to a string.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RecordToHTML- Global

The RecordToHTML script include is a utility class to turn a record into HTML.

This script include is available to server-side scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RecordToHTML - RecordToHTML\(String table, String sys\_id, String pattern, Boolean link\)

Creates an instance of a RecordToHTML class.

<table id="table_zdx_h3v_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

String

</td><td>

Table name of the record.

</td></tr><tr><td>

sys\_id

</td><td>

String

</td><td>

Sys\_id of the record.

</td></tr><tr><td>

pattern

</td><td>

String

</td><td>

The pattern of the string to generate. The pattern can include $\{\} template literals to provide the content of existing field values. For example, the pattern "$\{number\}" provides the number for the selected record.

</td></tr><tr><td>

link

</td><td>

Boolean

</td><td>

Flag that indicates whether generate results as an HTML link.Valid values:

-   true: The record information is generated as a link in an HTML tag.
-   false: The record information is generated as text.

Default: False

</td></tr></tbody>
</table>The following example shows how to generate formatted incident record information in an HTML link.

```
var r2html = new RecordToHTML("incident", "e8e875b0c0a80164009dc852b4d677d5",
"incident: ${number}-${short_description}");
gs.print(r2html.toString());
```

Output:

```
<a href="incident.do?sys_id=e8e875b0c0a80164009dc852b4d677d5"><u>incident: INC0000005-CPU load high for over 10 minutes</u></a>

```

## RecordToHTML - setValue\(String fieldName, String value\)

Sets the specified field to the specified value.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field to change.|
|value|String|Value to set the field to.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to generate formatted incident record information including the user name as a string.

```
var r2html = new RecordToHTML("incident","e8e875b0c0a80164009dc852b4d677d5", "incident: ${number}-${short_description} (${user})", true);
r2html.setValue("user", gs.getUserName());
gs.print(r2html.toString());
```

Output:

```
incident: INC0000005-CPU load high for over 10 minutes (admin)
```

## RecordToHTML - toString\(\)

Converts a RecordToHTML object to a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|HTML output of the record in the pattern set using the RecordToHTML\(\) constructor.|

The following example shows how to convert a RecordToHTML object to a string and display the results.

```
var r2html = new RecordToHTML("incident","e8e875b0c0a80164009dc852b4d677d5", 
                          "incident: ${number}-${short_description}", true);
gs.print(r2html.toString());
```

Output:

```
<a href="incident.do?sys_id=e8e875b0c0a80164009dc852b4d677d5"><u>incident: INC0000005-CPU load high for over 10 minutes</u></a>
```

