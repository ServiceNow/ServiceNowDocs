---
title: ScriptLoader - Client
description: The ScriptLoader API provides methods to load scripts asynchronously.Loads scripts asynchronously.Gets scripts asynchronously.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# ScriptLoader- Client

The ScriptLoader API provides methods to load scripts asynchronously.

You can use this API in client-side scripts for a platform/desktop UI using ListV2 and ListV3 APIs. It isn't available for Service Portal, Mobile, or Agent Workspace.

You access ScriptLoader methods by using the global object `ScriptLoader`.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## ScriptLoader - getScripts\(Array scripts, Function callback\)

Loads scripts asynchronously.

|Name|Type|Description|
|----|----|-----------|
|scripts|Array|Array of scripts to load.|
|callback|Function|Function to call when the scripts have been loaded. The callback function must not have any arguments.|

|Type|Description|
|----|-----------|
|void| |

```
var scriptFiles=[
'scripts/classes/providers/ProviderUI.js',
'scripts/classes/providers/wf_provider_client_script.js'
];

ScriptLoader.getScripts(scriptFiles, function() {
  ProviderUI.setFields(['input_transform']);
  ProviderUI.apply();
  ProviderUI.removeDisabledAttribute("sys_readonly.wf_element_activity.access");
}
```

## ScriptLoader - getScripts\(String filePath, Function callback\)

Gets scripts asynchronously.

|Name|Type|Description|
|----|----|-----------|
|filePath|String|Path, including the file name, that contains one or more scripts.|
|callback|Function|Function to call after the scripts have been loaded. This callback function should not have arguments.|

|Type|Description|
|----|-----------|
|void| |

This example shows how load a utility script and then run the getDepartment\(\) function.

```
// Client script to load a utility script and run the getDepartment callback function
ScriptLoader.getScripts('sn_ui_script_util.Utilities.jsdbx', getDepartment);

function getDepartment() {
  var req = sn_ui_script_util.Utilities.rest('json');
  req.addParam("sysparm_query", "sys_id=" + newValue);
  req.addParam("sysparm_fields", "department");
  req.addParam("sysparm_display_value", true);
  req.success(updateNotes);
  req.get("/api/now/table/sys_user");
}

function updateNotes(data) {
  g_form.setValue("work_notes", data.result[0].department.display_value);
}
```

