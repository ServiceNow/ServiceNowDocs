---
title: Scripting
description: Use scripts to extend your instance beyond standard configurations. With scripts, you may automate processes, add functionality, integrate your instance with an outside application and more.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [API implementation, API implementation and reference]
---

# Scripting

Use scripts to extend your instance beyond standard configurations. With scripts, you may automate processes, add functionality, integrate your instance with an outside application and more.

APIs \(Application Programming Interfaces\) provide classes and methods that you can use in scripts to define functionality. ServiceNow provides APIs as JavaScript classes, web services, and other points of connection for integrations. Note that you cannot access commonly used JavaScript objects \(such as DOM or Window\). Jelly scripts are also used in some modules. Jelly is used to turn XML into HTML and may include both client-side and server-side scripts.

Scripts may be server-side \(run on the server or database\), client-side \(run in the user's browser\), or run on the MID server.

**Note:** When you are writing scripts, you cannot use [reserved words](https://www.w3schools.com/js/js_reserved.asp).

Understand JavaScript before you begin customizing your instance, and with Jelly if you intend to deploy Jelly scripts.

## Server-side scripts

Perform database operations. For example, use a server-side script to update a record. Create a script in a scoped application or in the global scope. Each execution context includes a set of available APIs.

-   **Scoped environment**

    Use scoped APIs when scripting in a scoped application. Scoped Glide APIs do not include all the methods included in the global Glide APIs, and you cannot call a global Glide API in a scoped application.

-   **Global environment**

    The global scope is a special application scope that identifies applications developed prior to application scoping, or applications intended to be accessible to all other global applications. Use global APIs when scripting in the global scope.


To learn more about server-side scripting, see [Server-side scripting](../server-scripting/concept/c_ServerScripting.md). To learn more about application scope, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).

## Client-side scripts

Make changes to the appearance of forms, display different fields based on values that are entered, or change other custom display options.

-   onLoad client scripts run when the form or page is loaded
-   onChange client scripts run when something specific gets changed AND also when the form or page loads
-   onSubmit client scripts run when the form is submitted

Client Scripts can also be called by other scripts or modules, including UI policies. To learn more about client-side scripting, see [Client-side scripting](../client-scripts/concept/client-side-scripting-overview.md).

-   **[Available script types](../general-scripting/reference/r_17Scripts.md)**  
Scripts can be used in many places. The most important detail is whether the script runs on the client or the server.
-   **[Glide class overview](../general-scripting/reference/r_GlideClassOverview.md)**  
The ServiceNow Glide classes expose JavaScript APIs that enable you to conveniently work with tables using scripts.
-   **[Execution order of scripts and engines](../general-scripting/reference/r_ExecutionOrderScriptsAndEngines.md)**  
Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.
-   **[Script evaluation of fields by data type](../general-scripting/reference/r_ScriptingOfFieldTypes.md)**  
Script fields evaluate data based on the field type of the input.
-   **[Scripting alert, info, and error messages](../general-scripting/reference/r_ScriptingAlertInfoAndErrorMsgs.md)**  
You can send messages to customers as alerts, informational messages, or error messages.
-   **[JavaScript syntax editor](../general-scripting/concept/c_SyntaxEditor.md)**  
The JavaScript syntax editor provides support for editing JavaScript scripts.
-   **[HTML syntax editor](../general-scripting/concept/html-syntax-editor.md)**  
The HTML syntax editor provides support for editing HTML and Jelly scripts and defines what's rendered when the page is displayed. The HTML syntax editor can contain either static XHTML or dynamically generated content defined as Jelly, and can call script includes and UI Macros.
-   **[Code editor](../general-scripting/concept/monaco-editor.md)**  
The code editor provides support to use programming language services in a text editor and is used in scripts.
-   **[Server-side scripting](../server-scripting/concept/c_ServerScripting.md)**  
Server scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.
-   **[Client-side scripting](../client-scripts/concept/client-side-scripting-overview.md)**  
Run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
-   **[Useful scripts](../useful-scripts/concept/usefulScripts.md)**  
Server-side and client scripts that provide useful functionality not included in the core system.
-   **[Creating custom UI Pages and UI macros](../general-scripting/concept/create-custom-ui-pages.md)**  
Use UI pages to create custom pages for an application and UI macros for custom controls or interfaces.
-   **[Debugging scripts](../debugging/concept/script-debug-overview.md)**  
Debug scripts using session logs and ServiceNow AI Platform debugging tools such as a walk-through script debugger and error messages that display in the UI.
-   **[Packages Call Removal Tool](../general-scripting/concept/c_PackagesCallRemovalTool.md#)**  
The Packages Call Removal Tool provides modules to identify fields that might contain scripts, find scripts that contain Packages calls to ServiceNow Java classes, and to examine proposed script changes that eliminate those Packages calls.

**Parent Topic:**[API implementation](../../build/applications/concept/api-implementation.md)

