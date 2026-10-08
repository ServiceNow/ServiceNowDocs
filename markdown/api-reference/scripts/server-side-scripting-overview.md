---
title: Writing server-side scripts
description: Write scripts that run JavaScript on the application server to automate business processes, perform secure data operations, integrate with external systems, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/server-side-scripting-overview.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [use]
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Writing server-side scripts

Write scripts that run JavaScript on the application server to automate business processes, perform secure data operations, integrate with external systems, and more.

## Server-side API reference

When writing server-side scripts, you use server-side JavaScript APIs to change the functionality of applications. For information about available client-side APIs, see the [Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/api-server.md).

-   **[Server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ServerScripting.md)**  
Server-side scripts run on the server or database. They can change the appearance or behavior of ServiceNow or run as business rules when records and tables are accessed or modified.
-   **[JavaScript engine on the platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_JS_engine_upgrade.md)**  
The JavaScript engine that evaluates server-side scripts supports the ECMAScript 2021 \(ES12\) standard.
-   **[Script sandbox environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/script-sandbox-environment.md)**  
The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.
-   **[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/business-rules-classic/c_BusinessRules.md)**  
A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   **[Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ScriptIncludes.md)**  
Script includes are used to store JavaScript that runs on the server.
-   **[Background scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ScriptsBackground.md)**  
Administrators can use the **Scripts - Background** module to run arbitrary JavaScript code from the server.
-   **[Schedule pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_SchedulePages.md)**  
A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.
-   **[Script processors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_Processors.md)**  
Processors provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT or JSON. Creating custom processors is deprecated.
-   **[Using regular expressions in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_RegularExpressionsInScripts.md)**  
JavaScript regular expressions automatically use an enhanced regex engine, which provides improved performance and supports all behaviors of standard regular expressions as defined by Mozilla JavaScript. The enhanced regex engine supports using Java syntax in regular expressions.
-   **[Querying tables in script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_UsingGlideRecordToQueryTables.md)**  
Using methods in the GlideRecord API, you can return all records from a table, return records from a table that satisfy specific conditions, or return records that include a string from a single table or from multiple tables in a text index group.
-   **[Setting a GlideRecord variable to 'NULL'](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_SettingAGlideRecordVariableToNull.md)**  
GlideRecord variables \(including current\) are initially null in the database. Setting these back to an empty string, a space, or the JavaScript null value will not result in a return to this initial state.
-   **[Calculating a due date with DurationCalculator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_DrtnClDueDate.md)**  
Using the DurationCalculator script include, you can calculate a due date with either a simple duration or a relative duration base on schedules.
-   **[Parsing and extracting XML data in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_XMLDocumentScriptObject.md)**  
A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).

**Parent Topic:**[Scripting on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/scripting-landing.md)

**Related topics**  


[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/api-server.md)

