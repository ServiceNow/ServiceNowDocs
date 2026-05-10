---
title: Server-side scripting
description: Server scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Server-side scripting

Server scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.

Server-side Glide APIs \(Application Programming Interfaces\) provide classes and methods that you can use in scripts to perform server-side tasks.

## Immediately invoked function expressions

The system uses immediately invoked function expressions when a script runs in a single context, such as in a [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md). Functions that run from multiple contexts use [Script includes](c_ScriptIncludes.md#) instead.

By enclosing a script in an immediately invoked function expression, you can:

-   Ensure that the script does not impact other areas of the product, such as by overwriting global variables.
-   Pass useful variables or objects as parameters.
-   Identify function names in stack traces.
-   Eliminate having to make separate function calls.

An immediately invoked function expression follows this format:

```
(function functionName(parameter){
 
  //The script you want to run
 
})('value');//Note the parenthesis indicating this function should run.
```

You can declare functions within the immediately invoked function expression. These inner functions are accessible only from within the immediately invoked function expression.

```
(function functionName(parameter){
 
  function helperFunction(parameter){//return some value}
 
  var value = helperFunction(parameter);//Valid function call.
 
  //perform any other script actions
 
})('value');
 
var value2 = helperFunction(parameter);//Invalid. This function is not accessible from outside the self-executing function.
```

-   **[Glide Server APIs](../../glide-server-apis/topic/p_GlideServerAPIs.md#)**  
ServiceNow provides APIs for the Glide Server.
-   **[Classic Business rules](../../business-rules/concept/c_BusinessRules.md#)**  
A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   **[Script includes](c_ScriptIncludes.md#)**  
Script includes are used to store JavaScript that runs on the server.
-   **[Processors](../../processors/concept/c_Processors.md)**  
Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.
-   **[Scripts - Background module](c_ScriptsBackground.md)**  
Administrators can use the Scripts - Background module to run arbitrary JavaScript code from the server.
-   **[Script sandbox environment](script-sandbox-environment.md)**  
The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.
-   **[Installation settings](c_InstallationSettings.md)**  
Installation settings are global business rules with calculated names. Installation settings are calculated just before a record is displayed and facilitate dynamic determination of access and roles. Installation Settings permit the programmatic determination of a setting.
-   **[Using DurationCalculator to calculate a due date](c_DrtnClDueDate.md#)**  
Using the DurationCalculator script include, you can calculate a due date, using either a simple duration or a relative duration base on schedules.
-   **[Querying tables in script](c_UsingGlideRecordToQueryTables.md#)**  
Using methods in the GlideRecord API, you can return all records from a table, return records from a table that satisfy specific conditions, or return records that include a string from a single table or from multiple tables in a text index group.
-   **[Running order guides automatically](c_RunningOrderGuidesAutomatically.md#)**  
Service catalog order guides allow customers to make a single service catalog request that can generate several ordered items. Administrators can configure order guides to run automatically, from a workflow or a script to generate a set of ordered items without manually submitting a service catalog request. Administrators can also review and reprocess the order guide failures.
-   **[Scriptable assignment of execution plans](c_ScptblAsmtExctnPlns.md#)**  
Each catalog item has an associated execution plan, used whenever an item of that type is ordered; if no plan is specified, the default plan is used. This default is effective for most organizations, but your execution plan may need to vary based on additional criteria.
-   **[Using regular expressions in server-side scripts](../../general-scripting/concept/c_RegularExpressionsInScripts.md)**  
JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.
-   **[Scriptable service catalog variables](c_ScriptableServiceCatalogVariables.md)**  
You can use scripting to reference any request item variable from a table in scoped and non-scoped environment.
-   **[Setting a GlideRecord variable to 'NULL'](../reference/r_SettingAGlideRecordVariableToNull.md)**  
GlideRecord variables \(including current\) are initially null in the database. Setting these back to an empty string, a space, or the JavaScript null value will not result in a return to this initial state.
-   **[Schedule Pages](../../server-api/concept/c_SchedulePages.md#)**  
A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.
-   **[XMLDocument script object](c_XMLDocumentScriptObject.md)**  
A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).
-   **[JavaScript engine on the platform](../../JavaScript-engine-upgrade/concept/c_JS_engine_upgrade.md)**  
The JavaScript engine that evaluates server-side scripts supports the ECMAScript 2021 \(ES12\) standard.
-   **[JavaScript API Context-sensitive help](../../general-scripting/concept/c_ScriptingAssistance.md)**  
The syntax editor can display context-sensitive API information.

**Parent Topic:**[Scripting](../../topic/c_Script.md)

