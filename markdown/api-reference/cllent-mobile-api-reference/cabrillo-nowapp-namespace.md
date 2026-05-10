---
title: cabrillo.nowapp - Client
description: The name space for Cabrillo Now App functions. This enables you to interact with screens inside of ServiceNow AI Platform native mobile apps.Opens a mobile launcher native screen.Opens a mobile native screen.Opens a mobile native screen with a record context.Executes a native mobile function.Refresh the UI stack in the event a table update is made in the web view that may affect a previous screen.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.nowapp - Client

The name space for Cabrillo Now App functions. This enables you to interact with screens inside of ServiceNow AI Platform® native mobile apps.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.nowapp - openLauncherScreen\(String launcherScreenId\)

Opens a mobile launcher native screen.

|Name|Type|Description|
|----|----|-----------|
|launcherScreenId|String|Sys\_id of the launcher screen from the Applet launcher \[sys\_sg\_applet\_launcher\] table.|

<table id="table_qqc_55j_kxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the method is available on the native side.

 Valid values:

-   true: the method is available on the native side
-   false: the method is not available on the native side.

</td></tr></tbody>
</table>```
const launcherScreenId = 'a9e30c7dc61122760116894de7bcc7bd'; 
const result = cabrillo.nowapp.openLauncherScreen(launcherScreenId); 
If (result === false) {  
    console.log("method is not available")  
} 
```

Output:

```
true
```

## cabrillo.nowapp - openScreen\(String screenId\)

Opens a mobile native screen.

|Name|Type|Description|
|----|----|-----------|
|screenId|String|The sys\_id of the screen record to open from the Screen \[sys\_sg\_screen\] table.|

<table id="table_ysl_grj_kxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the method is available on the native side.

 Valid values:

-   true: the method is available on the native side
-   false: the method is not available on the native side.

</td></tr></tbody>
</table>```
const screenId = 'a9e30c7dc61122760116894de7bcc7bd'; 
cabrillo.nowapp.openScreen(screenId); 
If (result === false) {  
    console.log("method is not available")  
}
```

Output:

```
true
```

## cabrillo.nowapp - openScreenWithRecordContext\(String screenId, String table, String recordId\)

Opens a mobile native screen with a record context.

|Name|Type|Description|
|----|----|-----------|
|ScreenId|string|Sys\_id of the screen record to open from the Screen \[sys\_sg\_screen\] table.|
|table|string|The record table.|
|record|string|The record sys\_id.|

<table id="table_dvx_xsj_kxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the method is available on the native side.

 Valid values:

-   true: the method is available on the native side
-   false: the method is not available on the native side.

</td></tr></tbody>
</table>```
const screenId = 'a9e30c7dc61122760116894de7bcc7bd'; 
const recordId= '8e99daa3ff133100ba13757574847f2d'; 
const table= 'sys_users'; 
const result = cabrillo.nowapp.openScreenWithRecordContext(screenId, table, recordId); 
If (result === false) {  
    console.log("method is not available")  
} 
```

Output:

```
true
```

## cabrillo.nowapp - performFunction\(String functionId, String table, String recordId\)

Executes a native mobile function.

**Note:** Only Action functions are supported for the Vancouver release. For more information, see [Action functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-actions.md).

<table id="table_tjf_5vj_kxb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

functionId

</td><td>

string

</td><td>

Sys\_id of the target function from the Button \[sys\_sg\_button\] table.

</td></tr><tr><td>

table

</td><td>

string

</td><td>

The record table. Optional for Global Action items. For more information about mobile function, see [Action functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-actions.md).**Note:** Differences between Global and Record actions:

-   Record: Applies an action at the record level. For example, use this option to create a button that changes the state of a record. You can set the context to Record for actions on a particular field, a particular record, or swipe actions. If the action function includes a UI parameter with the Input source field set to Auto fill, you must specify the table in the Table field.
-   Global: Applies an action at the global, or list level. For example, use this option to add a button that creates a record. Do not use the Global setting for actions that are in the context of a record, or actions that include a UI parameter with the Input source field set to Auto fill.

</td></tr><tr><td>

recordId

</td><td>

string

</td><td>

The record sys\_id. Optional for Global Action Items. For more information about mobile function, see [Action functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-actions.md).

 **Note:** Differences between Global and Record action items:

-   Record: Applies an action at the record level. For example, use this option to create a button that changes the state of a record. You can set the context to Record for actions on a particular field, a particular record, or swipe actions. If the action function includes a UI parameter with the Input source field set to Auto fill, you must specify the table in the Table field.
-   Global: Applies an action at the global, or list level. For example, use this option to add a button that creates a record. Do not use the Global setting for actions that are in the context of a record, or actions that include a UI parameter with the Input source field set to Auto fill.

</td></tr></tbody>
</table><table id="table_ujf_5vj_kxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the method is available on the native side.

 Valid values:

-   true: the method is available on the native side
-   false: the method is not available on the native side.

</td></tr></tbody>
</table>```
const functionId= 'a9e30c7dc61122760116894de7bcc7bd'; 
const recordId= '8e99daa3ff133100ba13757574847f2d'; 
const table= 'sys_users'; 
const result = cabrillo.nowapp.performFunction(functionId, table, recordId); 
If (result === false) {  
    console.log("method is not available")  
} 
```

Output:

```
true
```

## cabrillo.nowapp - refresh\(\)

Refresh the UI stack in the event a table update is made in the web view that may affect a previous screen.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_k4s_wzj_kxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the method is available on the native side.

 Valid values:

-   true: the method is available on the native side
-   false: the method is not available on the native side.

</td></tr></tbody>
</table>```
const result = cabrillo.nowapp.refresh(); 
If (result === false) {  
    console.log("method is not available")  
```

Output:

```
true
```

