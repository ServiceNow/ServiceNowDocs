---
title: MobileScripts - Scoped
description: The MobileScripts API is the entry point for loading and calling custom mobile scripts stored in the Mobile Script \[sys\_sg\_mobile\_script\] table.Loads a mobile script by its API name and returns its exported value \(typically a class or function\) for immediate invocation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileScriptsScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileScripts - Scoped

The MobileScripts API is the entry point for loading and calling custom mobile scripts stored in the Mobile Script \[sys\_sg\_mobile\_script\] table.

It works like a script include, and can be resolved both on the device and on the instance.

Use this API to move reusable logic, such as a validator or a formatter, out of the inline expression on a button condition or a write-back action step. The script can then be called by name instead of being duplicated in each expression. A mobile script can also call another mobile script: the body of every mobile script runs with MobileScripts, [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md), and [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideRecordScopedAPI.md) already in scope, so a script can call `MobileScripts.get('ScriptA')` from within its own source.

When the script is evaluated on the instance, the results of `get()` are cached for the duration of the transaction, so repeated calls that use the same script name within a transaction don't run the script again. Resolving a script that depends on other scripts is limited by a configurable call depth, which is 25 by default. If resolution exceeds that depth, an error is thrown. This limit prevents mobile scripts from depending on each other in a loop.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no constructor. Access it with the static `MobileScripts.get(apiName)` method.

## MobileScripts - get\(String apiName\)

Loads a mobile script by its API name and returns its exported value \(typically a class or function\) for immediate invocation.

|Name|Type|Description|
|----|----|-----------|
|apiName|String|Dot-walked name in scope.name format \(for example, "global.ValidationHelper"\), matching a record in the sys\_sg\_mobile\_script table.|

|Type|Description|
|----|-----------|
|Object|The script's exported class, function, or object. Resolved exports are cached for the rest of the transaction, so repeated calls with the same apiName are cheap. If apiName does not resolve to a record in sys\_sg\_mobile\_script, throws IllegalArgumentException.|

This example calls a static method exported by a mobile script named global.TaskValidator.

```
var canComplete = MobileScripts.get('global.TaskValidator').canComplete(current.getValue('sys_id'));
mgs.info(canComplete);
```

Output:

```
true
```

