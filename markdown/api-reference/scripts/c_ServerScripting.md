---
title: Server-side scripts
description: Server-side scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_ServerScripting.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Server-side scripts

Server-side scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.

Server-side JavaScript APIs provide classes and methods that you can use in scripts to perform server-side tasks. Server-side scripts run in either the global scope or a scoped application scope, which determines which APIs are accessible.

## Immediately invoked function expressions

The system uses immediately invoked function expressions when a script runs in a single context, such as in a [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/t_CreateATransformMap.md). Functions that run from multiple contexts use [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ScriptIncludes.md) instead.

By enclosing a script in an immediately invoked function expression, you can:

-   Ensure that the script does not impact other areas of the product, such as by overwriting global variables.
-   Pass useful variables or objects as parameters.
-   Identify function names in stack traces.
-   Eliminate having to make separate function calls.

An immediately invoked function expression follows this format:

```javascript
(function functionName(parameter){
 
  //The script you want to run
 
})('value');//Note the parenthesis indicating this function should run.
```

You can declare functions within the immediately invoked function expression. These inner functions are accessible only from within the immediately invoked function expression.

```javascript
(function functionName(parameter){
 
  function helperFunction(parameter){//return some value}
 
  var value = helperFunction(parameter);//Valid function call.
 
  //perform any other script actions
 
})('value');
 
var value2 = helperFunction(parameter);//Invalid. This function is not accessible from outside the self-executing function.
```

**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

