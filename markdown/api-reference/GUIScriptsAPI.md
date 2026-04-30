---
title: GlideUIScripts - Client
description: The GlideUIScripts API provides methods to access UI scripts from within client-side code.Calls a UI script from a client script or other client-side code. Returns a promise.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideUIScripts- Client

The GlideUIScripts API provides methods to access UI scripts from within client-side code.

There is no constructor for this class. Access methods using the `g_ui_scripts` global object in any client-side code, such as client or validation scripts.

This API is only supported in Workspaces and Service Portal. It is not supported in the Core UI \(UI16\).

To use this API, the **UI Type** field must be set to **Mobile / Service Portal** or **All** on both the client script and the UI script. It cannot be set to **Desktop**.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideUIScripts - getUIScript\(String scriptName\)

Calls a UI script from a client script or other client-side code. Returns a promise.

Use the `then()` function to perform an asynchronous action after the call resolves.

**Note:** This method is not supported in Internet Explorer 11 when called outside of the Angular application environment. If calling a UI script outside of an Angular context using IE11, call the script directly using the `g_ui_scripts['nameOfScript'];` syntax.

|Name|Type|Description|
|----|----|-----------|
|scriptName|String|API name of the UI script to run.|

|Type|Description|
|----|-----------|
|Promise|The result of the asynchronous call.|

In this example, a client script calls a UI script to show an alert when the page loads.

```
// Client script
function onLoad() {
    g_ui_scripts.getUIScript('myUIScript').then(function(script) {
        script.myUIScriptMethod();
    }, function() {
        console.log('The script did not load');
    });
}
```

```
// UI script - myUIScript
(function() {
    return {
        myUIScriptMethod: function() { 
            alert("This is an alert.");
        }
    };
})();
```

