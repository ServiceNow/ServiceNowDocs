---
title: MobileScripts - Scoped
description: The MobileScripts API is the entry point for loading and calling custom mobile scripts stored in the Mobile Script \[sys\_sg\_mobile\_script\] table.Loads a mobile script by its name and returns the value that the script exports, such as a class or function, so that a script can call it right away.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileScriptsScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileScripts - Scoped

The MobileScripts API is the entry point for loading and calling custom mobile scripts stored in the Mobile Script \[sys\_sg\_mobile\_script\] table.

It works like a script include, and can be resolved both on the device and on the instance.

Use this API to move reusable logic, such as a validator or a formatter, out of the inline expression on a button condition or a write-back action step. The script can then be called by name instead of being duplicated in each expression. A mobile script can also call another mobile script: the body of every mobile script runs with MobileScripts, [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), and [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md) already in scope, so a script can call `MobileScripts.get('ScriptA')` from within its own source.

When the script is evaluated on the instance, the results of `get()` are cached for the duration of the transaction, so repeated calls that use the same script name within a transaction don't run the script again. Resolving a script that depends on other scripts is limited by a configurable call depth, which is 25 by default. If resolution exceeds that depth, an error is thrown. This limit prevents mobile scripts from depending on each other in a loop.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no constructor. Access it with the static `MobileScripts.get(apiName)` method.

## MobileScripts - get\(String apiName\)

Loads a mobile script by its name and returns the value that the script exports, such as a class or function, so that a script can call it right away.

|Name|Type|Description|
|----|----|-----------|
|apiName|String|Name of the mobile script, in the format `scope.name`, such as `global.ValidationHelper`. The name must match a record in the Mobile Script \[sys\_sg\_mobile\_script\] table.|

|Type|Description|
|----|-----------|
|Object|The value that the script exports, such as a class, function, or object. If `apiName` does not match a record in the Mobile Script table, the method throws an `IllegalArgumentException` error. When the script runs on the instance, the result is saved for the rest of the transaction, so repeated calls with the same name don't run the script again.|

This example loads a mobile script named `global.TaskValidator`, calls its canComplete\(\) method with the sys\_id of the current record, and logs whether the task can be completed.

```
var canComplete = MobileScripts.get('global.TaskValidator').canComplete(current.getValue('sys_id'));
        mgs.info(canComplete);
```

Output:

```
true
```

This example uses the same validator in a write-back action to stop a task from being completed while it has open child tasks. The script handles the case where the mobile script name doesn't match a record, which makes get\(\) throw an error. Keeping the check in a mobile script means that every button and action that needs it calls the same logic.

```
try {
        var validator = MobileScripts.get('global.TaskValidator');
        if (validator.canComplete(current.getValue('sys_id'))) {
        mgs.addInfoMessage('Task can be completed.');
        } else {
        mgs.addErrorMessage('Complete all child tasks first.');
        }
        } catch (e) {
        mgs.info('Could not load global.TaskValidator: ' + e);
        }
```

Message shown to the user when the task has open child tasks:

```
Complete all child tasks first.
```

