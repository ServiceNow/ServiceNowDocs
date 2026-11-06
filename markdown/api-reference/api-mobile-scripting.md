---
title: Mobile Scripting API reference
description: Mobile Scripts are JavaScript APIs that you write in the sn\_mobile\_scripting scoped namespace to evaluate conditions and read or update records for mobile app components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/api-mobile-scripting.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [API reference, API implementation and reference]
---

# Mobile Scripting API reference

Mobile Scripts are JavaScript APIs that you write in the sn\_mobile\_scripting scoped namespace to evaluate conditions and read or update records for mobile app components.

Mobile scripting supports a smaller set of classes and methods than server-side scripting, because the same script must be able to run against the local database on a device. Depending on the use case and execution context, a mobile script runs on the device or on the instance.

Whether a script that uses this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The same script is used in both cases, without modification.

## API access requirements

The Mobile Scripting classes are provided within the sn\_mobile\_scripting namespace and require the Mobile Scripting plugin \(com.glide.sg.mobile\_scripting\).

To create or modify the scripts that call this API, you need the mobile\_admin role.

## Supported components

Mobile scripts are currently supported for the following components:

-   **Button conditions**: Determine whether a button is shown or enabled for the current record and user.
-   **Write-back actions \(WBA\)**: Set field values on a record when the action runs.

## Available classes

-   [MobileGlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md): Work with date values.
-   [MobileGlideDateTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md): Work with date and time values.
-   [MobileGlideElement - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md): Read and set values on a single field.
-   [MobileGlideRecord - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md): Query, read, and update records.
-   [MobileGlideSystem - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md) \(mgs\): Utility methods for the current user, session, and date-time values.
-   [MobileGlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md): Work with time values.
-   [MobileGlideUser - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md): Access the current user's profile, roles, and groups.
-   [MobileScripts - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileScriptsScopedAPI.md): Load and invoke custom mobile scripts.

## Instantiating a class

```
var gr = new MobileGlideRecord('incident');
```

MobileGlideSystem is available as the mgs object and doesn't require instantiation.

## Mobile scripts supported syntax

Mobile Scripts supports four invocation patterns for scripts stored in the Mobile Scripts table. The following sections define valid syntax and disallowed dynamic lookup methods.

-   Supported patterns include ES6 class instances, static ES6 classes, object literals, and IIFE-based objects, invoked through MobileScripts.get with direct script names.
-   Disallows ServiceNow Class.create patterns, variables, concatenation, template literals, expressions, conditionals, instance-based access, dynamic properties, and array or object access.

## Supported syntax for the Script field in the Mobile Scripts table

The following patterns are supported.

1.  **ES6 classes**.

    Syntax: `new (MobileScripts.get("<ScopeName>.<ScriptName>"))(<ctorArgs>).method(<args>)`

    The parentheses around MobileScripts.get\(\) are required. Without them, `new` is applied to `get()` instead of to the class it returns.

    For readability, assign the returned class to a constant, and then instantiate it on a separate line: `const TaskValidator = MobileScripts.get("global.TaskValidator"); new TaskValidator(current.getValue('sys_id')).canComplete(current);`

    In this example, the script defines a class, then creates an instance by passing constructor arguments and calls its method.

    ```
    // Script: "TaskValidator"
    class TaskValidator {
      constructor(taskId) {
        this.taskId = taskId;
      }
      canComplete(current) {
        return current.getValue('state') === '2';
      }
    }
    
    // Usage:
    const TaskValidator = MobileScripts.get("global.TaskValidator");
    new TaskValidator(current.getValue('sys_id')).canComplete(current);
    ```

2.  **ES6 classes \(static methods\)**.

    Syntax: `MobileScripts.get("<ScopeName>.<ScriptName>").method(<args>)`

    Define a class with static methods, then call a method directly on the class without creating an instance.

    ```
    // Script: "DateHelper"
              class DateHelper {
              static isOverdue(taskId) {
              var gr = new MobileGlideRecord('wm_task');
              gr.get(taskId);
              return gr.getValue('due_date') < mgs.getDateTime();
              }
              }
              
              // Usage:
              MobileScripts.get("global.DateHelper").isOverdue(current.getValue('sys_id'))
    ```

3.  **Object literals**

    Syntax: `MobileScripts.get("<ScopeName>.<ScriptName>").method(<args>)`

    Define an object literal with methods, then call a method on the object by its script name.

    ```
    // Script: "UserHelper"
              var UserHelper = {
              getFullName: function(userId) {
              var gr = new MobileGlideRecord('sys_user');
              gr.get(userId);
              return gr.getValue('first_name') + ' ' + gr.getValue('last_name');
              }
              };
              
              // Usage:
              MobileScripts.get("global.UserHelper").getFullName(current.getValue('assigned_to'))
    ```

4.  **IIFE patterns**

    Syntax: `MobileScripts.get("<ScopeName>.<ScriptName>").method(args)`

    Wrap the object in an immediately invoked function that returns the public methods, then call them by script name.

    ```
    // Script: "StatusChecker"
              var StatusChecker = (function() {
              function isActive(record) {
              return record.getValue('active') === 'true';
              }
              return { isActive: isActive };
              })();
              
              // Usage:
              MobileScripts.get("global.StatusChecker").isActive(current)
    ```


## Unsupported syntax for the Script field in the Mobile Scripts table

The following patterns aren't supported.

1.  **Script include Class.create\(\) pattern**

    The `Class.create()` pattern is a ServiceNow-specific utility for defining classes using the JavaScript prototype chain. It predates ES6 classes and is commonly used in server-side script includes.

    ```
    var TaskValidator = Class.create();
              TaskValidator.prototype = {
              initialize: function() { ... },
              canComplete: function(current) { ... },
              type: 'TaskValidator'
              };
    ```

2.  **Variable usage**

    Passing a variable as the script name isn't allowed. Use the script name as a literal string.

    ```
    //NOT ALLOWED
              var scriptName = "ValidationHelper";
              MobileScripts.get(scriptName)
              
              //NOT ALLOWED
              const name = "Helper";
              MobileScripts.get(name)
    ```

3.  **String concatenation**

    Building the script name by joining strings isn't allowed. Use the full script name as a single literal string.

    ```
    //NOT ALLOWED
              MobileScripts.get("Validation" + "Helper")
              MobileScripts.get("Helper" + suffix)
    ```

4.  **Template literals**

    Template literals, including ones with embedded variables, aren't allowed for the script name. Use a plain string literal instead.

    ```
    //NOT ALLOWED
              MobileScripts.get(`ValidationHelper`)
              MobileScripts.get(`${scriptName}Helper`)
    ```

5.  **Expressions or function calls**

    Script names computed by a function call, method call, or property expression aren't allowed.

    ```
    //NOT ALLOWED
              MobileScripts.get(getScriptName())
              MobileScripts.get(scriptName.trim())
              MobileScripts.get(obj.scriptName)
    ```

6.  **Ternary or conditional operators**

    Choosing between script names with a conditional operator isn't allowed. Call the specific script name directly.

    ```
    //NOT ALLOWED
              MobileScripts.get(flag ? "ScriptA" : "ScriptB")
              MobileScripts.get(enabled ? "Helper" : "DefaultHelper")
    ```

7.  **Instance method usage**

    Calling get on an instance of MobileScripts isn't allowed. Call get on MobileScripts directly.

    ```
    //NOT ALLOWED
              var mobileScripts = new MobileScripts();
              mobileScripts.get("ValidationHelper")
    ```

8.  **Dynamic property access**

    Reading the script name from an object property, with dot or bracket notation, isn't allowed.

    ```
    //NOT ALLOWED
              var obj = { name: "ValidationHelper" };
              MobileScripts.get(obj.name)
              MobileScripts.get(obj["name"])
    ```

9.  **Array or object access**

    Reading the script name from an array element isn't allowed.

    ```
    // NOT ALLOWED
              var scripts = ["Helper1", "Helper2"];
              MobileScripts.get(scripts[0])
    ```


