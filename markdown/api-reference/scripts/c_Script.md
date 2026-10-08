---
title: Exploring scripting
description: Learn how to use scripts to extend your instance beyond standard configurations. With scripts, you can automate processes, add functionality, integrate your instance with an outside application and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_Script.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Exploring scripting

Learn how to use scripts to extend your instance beyond standard configurations. With scripts, you can automate processes, add functionality, integrate your instance with an outside application and more.

ServiceNow JavaScript APIs enable you to perform database operations without writing SQL queries, display UI pages, define UI actions, and more. Scripts can be server-side \(run on the server or database\), client-side \(run in the user's browser\), or run on the MID Server.

**Note:** Scripts can't contain [reserved words](https://www.w3schools.com/js/js_reserved.asp).

## Server-side scripts

Perform database operations. For example, use a server-side script to update a record. Create a script in a scoped application or in the global scope. Each execution context includes a set of available APIs.

-   **Scoped environment**

    Use scoped APIs when scripting in a scoped application. Scoped Glide APIs don't include all the methods included in the global Glide APIs, and you can't call a global Glide API in a scoped application. To learn more about application scopes, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/c_ApplicationScope.md).

-   **Global environment**

    The global scope is a special application scope that identifies applications developed before application scoping, or applications intended to be accessible to all other global applications. Use global APIs when scripting in the global scope.


To learn more about server-side scripting, see [Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md).

## Client-side scripts

Make changes to the appearance of forms, display different fields based on values that are entered, or change other custom display options. Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

Client scripts can also be called by other scripts or modules, including UI policies. To learn more about client-side scripting, see [Writing client-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-side-scripting-overview.md).

-   **[Available script types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_17Scripts.md)**  
Scripts can be used in many places. The most important detail is whether the script runs on the client or the server.
-   **[Execution order of scripts and engines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_ExecutionOrderScriptsAndEngines.md)**  
Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.
-   **[Script evaluation of fields by data type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_ScriptingOfFieldTypes.md)**  
Script fields evaluate data based on the field type of the input.
-   **[Scripting alert, info, and error messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_ScriptingAlertInfoAndErrorMsgs.md)**  
You can send messages to users as alerts, informational messages, or error messages.
-   **[Glide platform stack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_GlideStack.md)**  
Glide is an extensible Web 2.0 development platform written in Java that facilitates rapid development of forms-based workflow applications \(work orders, trouble ticketing, and project management, for example\).
-   **[JavaScript syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_SyntaxEditor.md)**  
The JavaScript syntax editor provides support for editing JavaScript scripts.

**Parent Topic:**[Scripting on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/scripting-landing.md)

**Related topics**  


[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/api-server.md)

[Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/api-client.md)

