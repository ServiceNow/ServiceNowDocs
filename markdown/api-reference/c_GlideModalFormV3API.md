---
title: GlideModalForm - Client
description: The GlideModalForm API provides methods to display a form in a GlideModal.Creates an instance of the GlideModalForm class.Sets the specified form field to the specified value.Sets the object's sys\_id preference.Sets the function to be called when the form has been successfully submitted and processed by the server.Sets the function to be called after the form has been loaded.Shows the modal form.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideModalForm- Client

The GlideModalForm API provides methods to display a form in a GlideModal.

General usage of the GlideModalForm class involves creating the object, setting any preferences, and then rendering the GlideModalForm.

```
var dialog = new GlideModalForm('dialog title', 'table_name_or_form_name', [callback on completion of submit])
  dialog.setPreference('name', 'value');
  dialog.render();
```

Specify the query parameters that are passed to the form using the setPreference\(\) method. Any name/value pair that you specify with setPreference\(\) is sent along with the form POST request to display the form.

The GlideModalForm is set to fill the height of the document window.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideModalForm - GlideModalForm\(String title, String tableName, Function onCompletionCallback, Boolean readOnly\)

Creates an instance of the GlideModalForm class.

<table id="table_ikc_xjm_qv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td>

Modal form title.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td>

Table being shown.

</td></tr><tr><td>

onCompletionCallback

</td><td>

Function

</td><td>

Function to call after the form has been submitted and processed on the server. The callback function has the form`callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

 -   **action\_verb**: Name of the UI action executed. Examples are sysverb\_insert \(Submit button\), sysverb\_cancel, sysverb\_save \(Save button\).
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the modal form should be set to read only.Valid values:

-   true: Set form to read only.
-   false: Set for to read/write.

 Default: false

</td></tr></tbody>
</table>This example shows how to instantiate a GlideModalForm object.

```
function openDevice(deviceSysID, deviceName) {
  var uName = gel('hidden_user_name').value + "'s ";
  deviceName = new String(deviceName).escapeHTML();
  var gp = new GlideModalForm(uName + deviceName, "cmn_notif_device", refreshNotifPage);
  gp.addParm('sys_id', deviceSysID);
  gp.render();
}
```

## GlideModalForm - addParm\(String name, String value\)

Sets the specified form field to the specified value.

|Name|Type|Description|
|----|----|-----------|
|name|String|Form field name. If the specified name is not a field in the associated modal form, it is ignored.|
|value|String|Value to set the specified form field to.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call addParm\(\) to set the value of the sys\_id field the modal form.

```
function openDevice(deviceSysID, deviceName) {
  var uName = gel('hidden_user_name').value + "'s ";
  deviceName = new String(deviceName).escapeHTML();
  var gp = new GlideModalForm(uName + deviceName, "cmn_notif_device", refreshNotifPage);
  gp.addParm('sys_id', deviceSysID);
  gp.render();
}
```

## GlideModalForm - setSysID\(String sys\_id\)

Sets the object's sys\_id preference.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|The id preference. One of the query parameters passed to the form.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to use the setSysID\(\) method to initialize the value of the sys\_id.

```
function(startDate, endDate) {
  var dialog = new GlideModalForm("Add Schedule Item", "cmn_schedule_span");
  dialog.setSysID("-1");
  dialog.addParm("sysparm_collection", "cmn_schedule");
  dialog.addParm("sysparm_collectionID", this.sysId);
  dialog.addParm("sysparm_collection_key", "schedule");
 
  var q = "schedule=" + this.sysId + "^start_date_time="
   + startDate.serializeInUserFormat() + "^end_date_time="
   + endDate.serializeInUserFormat() + "^";

  if (startDate.isAllDay(endDate))
    q += "^all_day=true^";
 
  dialog.addParm("sysparm_query", q);
  dialog.render();
}
```

## GlideModalForm - setCompletionCallback\(Function callbackFunction\)

Sets the function to be called when the form has been successfully submitted and processed by the server.

<table id="table_aqr_ply_kv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

callbackFunction

</td><td>

Function

</td><td>

Callback function to call when the form has been successfully processed. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: action\_name from a sys\_ui\_action record
-   **sys\_id**: Sys\_id of the affected record
-   **table**: Name of the table containing the record
-   **displayValue**: Value that appears on the form

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to set the onload callback function of the associated modal.

```
function handleCreateOrEdit(targetFieldName, sourceFieldName, adapterRuleId, transformerSysId){
  dialog = new GlideModalForm('Edit Adapter Rule', "sys_adapter_rule");
  dialog.setSysID(adapterRuleId); //Pass in sys_id to edit existing record
  dialog.addParm('sysparm_form_only', 'true'); //Add or remove related lists
  dialog.setOnloadCallback(hideModalForm);
  dialog.setCompletionCallback(handleAdapterCreatedOrUpdated);
  dialog.render(); //Open the dialog
}
function handleAdapterCreatedOrUpdated(action_verb, sys_id, table, displayValue) {
  var draftRecordTransformer = g_form.getValue("draft_record_transformer");
  if(draftRecordTransformer == null || draftRecordTransformer.length == 0) {
    //sync Sticky Replications if it is enabled.
    var ajax = new GlideAjax('ReplicationPoolUtil');
    ajax.addParam('sysparm_name', 'syncStickyReplicationSet');
    ajax.addParam('sysparm_entry_set', g_form.getValue("entry_set"));
    ajax.getXMLWait();
  }
}
```

## GlideModalForm - setOnloadCallback\(Function callbackFunction\)

Sets the function to be called after the form has been loaded.

|Name|Type|Description|
|----|----|-----------|
|callbackFunction|Function|Function to call after the form has been loaded. The callback function has the form `callBackFunction(GlideModalForm obj)`|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the on load callback function of the associated modal.

```
function handleCreateOrEdit(targetFieldName, sourceFieldName, adapterRuleId, transformerSysId){
  dialog = new GlideModalForm('Edit Adapter Rule', "sys_adapter_rule");
  dialog.setSysID(adapterRuleId); //Pass in sys_id to edit existing record
  dialog.addParm('sysparm_form_only', 'true'); //Add or remove related lists
  dialog.setOnloadCallback(hideModalForm);
  dialog.setCompletionCallback(handleAdapterCreatedOrUpdated);
  dialog.render(); //Open the dialog
}
```

## GlideModalForm - render\(\)

Shows the modal form.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to call render\(\) to display the modal.

```
function openDevice(deviceSysID, deviceName) {
  var uName = gel('hidden_user_name').value + "'s ";
  deviceName = new String(deviceName).escapeHTML();
  var gp = new GlideModalForm(uName + deviceName, "cmn_notif_device", refreshNotifPage);
  gp.addParm('sys_id', deviceSysID);
  gp.render();
}
```

