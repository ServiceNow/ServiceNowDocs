---
title: Script Debugger API
description: The Script Debugger API provides endpoints to debug lines of server-side JavaScript code, such as business rules and script includes.Retrieve a list of breakpoints or logpoints in a server-side script, such as a business rule or script include.Add, update, or remove breakpoints or logpoints in a server-side script, such as a business rule or script include. Process several breakpoints or logpoints at a time.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Script Debugger API

The Script Debugger API provides endpoints to debug lines of server-side JavaScript code, such as business rules and script includes.

For more information about the Script Debugger, see [Script Debugger and Session Log](../../../script/debugging/concept/script-debugger.md).

This API is available by default.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Script Debugger - GET /js/debugpoints/script/\{tableName\}/\{sysId\}/\{fieldName\}

Retrieve a list of breakpoints or logpoints in a server-side script, such as a business rule or script include.

### URL format

Default URL: `/api/now/js/debugpoints/script/{tableName}/{sysId}/{fieldName}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

Name of the table that contains the server-side script, such as sys\_script or sys\_script\_include.Data type: String

</td></tr><tr><td>

sysId

</td><td>

Sys\_id for the server-side script.Data type: String

</td></tr><tr><td>

fieldName

</td><td>

Name of the field that contains the server-side script content.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|403|User Not Authorized. The user who executed the request does not have permission to access breakpoint or log point information for the specified record.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

canWrite

</td><td>

Flag indicating whether the currently logged in user can set or modify breakpoints for the script.Possible values:

-   true: You can set or modify breakpoints.
-   false: You cannot set or modify breakpoints.

 Data type: Boolean

</td></tr><tr><td>

debugpoints

</td><td>

List of all the breakpoints and logpoints in the script.```
"debugpoints": {
  "breakpoint": {Object}
  "logpoint": {Object}
}
```

 Data type: Object

</td></tr><tr><td>

debugpoints.breakpoint

</td><td>

List of all the breakpoints in the script, presented as key-value pairs. The key is the line number for the breakpoint. The value is an object containing the breakpoint's sys\_id and text.```
"breakpoint": {
  <line_number>: {Object}
}
```

 Data type: Object

</td></tr><tr><td>

debugpoints.breakpoint.&lt;line\_number&gt;

</td><td>

Line number for the breakpoint.```
<line_number>: {
  "evaluationString": "String"
  "sysId": "String"
}
```

 Data type: Object

</td></tr><tr><td>

debugpoints.breakpoint.&lt;line\_number&gt;.evaluationString

</td><td>

Text of the breakpoint. If the breakpoint is conditional, the evaluationString contains the condition text. If the breakpoint is not conditional, the evaluationString is an empty string. Data type: String

</td></tr><tr><td>

debugpoints.breakpoint.&lt;line\_number&gt;.sysId

</td><td>

Sys\_id of the breakpoint.Data type: String

</td></tr><tr><td>

debugpoints.logpoint

</td><td>

List of all the logpoints in the script, presented as key-value pairs. The key is the line number for the logpoint. The value is an object containing the logpoint's sys\_id and text.```
"logpoint": {
  <line_number>: {Object}
}
```

 Data type: Object

</td></tr><tr><td>

debugpoints.logpoint.&lt;line\_number&gt;

</td><td>

Line number for the logpoint.```
<line_number>: {
  "evaluationString": "String"
  "sysId": "String"
}
```

 Data type: Object

</td></tr><tr><td>

debugpoints.logpoint.&lt;line\_number&gt;.evaluationString

</td><td>

Text of the logpoint. Contains the message being logged.Data type: String

</td></tr><tr><td>

debugpoints.logpoint.&lt;line\_number&gt;.sysId

</td><td>

Sys\_id of the logpoint.Data type: String

</td></tr><tr><td>

key

</td><td>

Object providing details about the script being debugged. ```
"key": {
  "scriptField": "String"
  "scriptId": "String"
  "scriptType": "String"
  "value": "String"
}
```

 Data type: Object

</td></tr><tr><td>

key.scriptField

</td><td>

Name of the field that contains the script.Data type: String

</td></tr><tr><td>

key.scriptId

</td><td>

Sys\_id of the script.Data type: String

</td></tr><tr><td>

key.scriptType

</td><td>

Name of the table that contains the script.Data type: String

</td></tr><tr><td>

key.value

</td><td>

The path parameters used to make the request. Listed in the following order.-   tableName
-   sysId
-   fieldName

 Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the script.Data type: String

</td></tr><tr><td>

script

</td><td>

Text displaying the script's code.Data type: String

</td></tr></tbody>
</table>### Example cURL request

### cURL request

Retrieves a list of logpoints and breakpoints for a server-side script. This script has a logpoint on line 2, a breakpoint on line 11, and a conditional breakpoint on line 18.

```
curl "https://instance.servicenow.com/api/now/js/debugpoints/script/sys_script_include/d65f78c40a0a0b6900196656f35913d3/script" \
--request GET \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "canWrite": true,
    "debugpoints": {
      "LOGPOINT": {
        "2": {
          "evaluationString": "A log message",
          "sysId": "ba28b0fa739310101c233096fbf6a75e"
        }
      },
      "BREAKPOINT": {
        "11": {
          "evaluationString": "",
          "sysId": "dc5f5bf341256010f877587fbdf5ec1d"
        },
        "18": {
          "evaluationString": "a == true",
          "sysId": "3d4f5bf341256010f877587bdf5ecf6"
        }
      }
    },
    "script": "// script code",
    "name": "AbstractAjaxProcessor",
    "key": {
      "scriptType": "sys_script_include",
      "scriptId": "d65f78c40a0a0b6900196656f35913d3",
      "scriptField": "script",
      "value": "sys_script_include.d65f78c40a0a0b6900196656f35913d3.script"
    }
  }
}
```

## Script Debugger - POST js/debugpoints/process

Add, update, or remove breakpoints or logpoints in a server-side script, such as a business rule or script include. Process several breakpoints or logpoints at a time.

### URL format

Default URL: `/api/now/js/debugpoints/process`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fetchAll

</td><td>

When true, returns a list of all the breakpoints or logpoints added or updated by the user.Data type: Boolean

 Default: false

</td></tr><tr><td>

fetchAllFilter

</td><td>

Returns a filtered list of all the breakpoints or logpoints added or updated by the user.

 Valid values:

-   debugpointType. Set to either breakpoint or logpoint.
-   scriptId. Set to the sys\_id of the script in which to search for debug points.
-   scope. Set to the name of the scope in which to search for debug points.

 Use the caret \(^\) symbol as a separator for multiple properties. For example, `fetchAllFilter=debugpointType=logpoint^scope=MyApp`

 Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

debugpointType

</td><td>

Required. Type of debug point to add, delete, or update.

 Valid values:

-   breakpoint
-   logpoint

 Data type: String

</td></tr><tr><td>

evaluationString

</td><td>

Text for a logpoint or conditional breakpoint.

 For a logpoint, the **evaluationString** is the log message.

 For a conditional breakpoint, the **evaluationString** is the condition. For example, if you're looping through a list of user IDs and you want the debugger to pause only when the user ID is 38493, you can add a conditional breakpoint inside the loop with `userID == 38493` as the condition. The debugger will only pause at this breakpoint when the condition is true.

 If the breakpoint is not a conditional breakpoint, the **evaluationString** is an empty string.

 Data type: String

</td></tr><tr><td>

fieldName

</td><td>

Required. Name of the field that contains the server-side script content.Data type: String

</td></tr><tr><td>

lineNumber

</td><td>

Line number in the server-side script specifying where to add, delete, or update the breakpoint or logpoint.Data type: Number

</td></tr><tr><td>

operation

</td><td>

Required. Operation to perform for the breakpoint or logpoint.Valid values:

-   add
-   delete
-   update

 Data type: String

</td></tr><tr><td>

scriptId

</td><td>

Required. Sys\_id for the server-side script.Data type: String

</td></tr><tr><td>

tableName

</td><td>

Required. Name of the table that contains the server-side script, such as sys\_script or sys\_script\_include.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requestedDebugpoints

</td><td>

List of the requested breakpoints and logpoints. Presented as an array of objects.```
"requestedDebugpoints": [
  {
    "scriptId": "String",
    "evaluationString": "String",
    "operation": "String",
    "tableName": "String",
    "fieldName": "String",
    "status": "String",
    "lineNumber": Number,
    "debugpointType": "String"
  }
]
```

 Data type: Array

</td></tr><tr><td>

requestedDebugpoints.ScriptId

</td><td>

Sys\_id for the server-side script.Data type: String

</td></tr><tr><td>

requestedDebugpoints.evaluationString

</td><td>

Text added for a logpoint or conditional breakpoint. For a logpoint, the **evaluationString** is the log message. For a conditional breakpoint, the **evaluationString** is the condition. Data type: String

</td></tr><tr><td>

requestedDebugpoints.operation

</td><td>

Operation performed for the breakpoint or logpoint.

 Possible values:

-   add
-   delete
-   update

 Data type: String

</td></tr><tr><td>

requestedDebugpoints.tableName

</td><td>

Name of the table that contains the server-side script, such as sys\_script or sys\_script\_include.Data type: String

</td></tr><tr><td>

requestedDebugpoints.fieldName

</td><td>

Name of the field that contains the server-side script content.Data type: String

</td></tr><tr><td>

requestedDebugpoints.status

</td><td>

Result of the instruction to add, delete, or update a specific breakpoint or logpoint.

 Possible values:

-   failure
-   ignored
-   success

 A request to add, delete, or update a debug point is ignored in the following situations:

-   It requests to delete a breakpoint or logpoint that doesn't exist.
-   It requests to add a breakpoint or logpoint identical to one that already exists.

 Data type: String

</td></tr><tr><td>

requestedDebugpoints.lineNumber

</td><td>

Line number in the server-side script specifying where the breakpoint or logpoint was added, deleted, or updated.Data type: Number

</td></tr><tr><td>

requestedDebugpoints.debugpointType

</td><td>

Type of debug point added, deleted, or updated.

 Possible values:

-   breakpoint
-   logpoint

 Data type: String

</td></tr><tr><td>

status

</td><td>

Result of the overall action. The status code for the HTTP call.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example adds a conditional breakpoint at line 12 in the script.

```
curl "https://instance.servicenow.com/api/now/js/debugpoints/process" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data “[
{
\"tableName\": \"sys_script_include\",
\"scriptId\": \"d65f78c40a0a0b6900196656f35913d3\",
\"fieldname\": \"script\",
\"lineNumber\": 12,
\"evaluationString\": \"a == false\",
\"debugpointType\": \"breakpoint\",
\"operation\": \"add\"
}
]” \
--user 'username':'password'
```

```
{
  "result": {
    "requestedDebugpoints": [
      {
        "scriptId": "d65f78c40a0a0b6900196656f35913d3",
        "evaluationString": "a == false",
        "operation": "add",
        "tableName": "sys_script_include",
        "fieldName": "script",
        "status": "success",
        "lineNumber": 12,
        "debugpointType": "breakpoint"
      }
    ],
    "status": 200
  }
}

```

