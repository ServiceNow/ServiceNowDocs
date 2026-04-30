---
title: Debugging scripts
description: Debug scripts using session logs and ServiceNow AI Platform debugging tools such as a walk-through script debugger and error messages that display in the UI.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Debugging scripts

Debug scripts using session logs and ServiceNow AI Platform debugging tools such as a walk-through script debugger and error messages that display in the UI.

## Debugging server-side scripts

Use the Script Debugger and session logs to debug server-side code. For more information, see [Script Debugger and Session Log](script-debugger.md).

You can also use session debug to display error messages related to a server-side script that runs as a result of a client-side change. For more information, see [Session debug](c_SessionDebug.md#).

GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values. For more information, see [GSLog API](../../../app-store/dev_portal/API_reference/GSLogBoth/concept/GSLogBoth.md#).

## Debugging client-side scripts

Use session debug to display debugging messages in the user interface. For more information, see [Session debug](c_SessionDebug.md#). Use the session log to view logging information for script includes and custom UIs, such as Agent Workspace.

You can also debug client-side scripts using browser-based developers tools.

## Debugging applications and scopes

Use the application debugging options to understand how a script's application scope might affect your application, table, or record. You may need to update cross-scope privileges to troubleshoot scope access issues. See [Debugging applications](c_DebuggingApplications.md#).

-   **[Script Debugger and Session Log](script-debugger.md)**  
The Script Debugger enables users with the script\_debugger role to debug server-side JavaScript. Users with the log\_debugger role can use the Session Log to view and download required logs.
-   **[Session debug](c_SessionDebug.md#)**  
Enable session debugging to display debugging messages in the user interface.
-   **[Debugging applications](c_DebuggingApplications.md#)**  
Application developers can display debug messages about configuration records to help them troubleshoot issues. The Debug Scopes module provides information about the system switching between custom applications to run server-side scripts.
-   **[Debugging business rules](../../business-rules/reference/r_DebuggingBusinessRules.md)**  
Debugging business rules can be achieved with resources available in the ServiceNow product.
-   **[Debugging classifications](../reference/r_DebuggingClassifications.md)**  
You must add a system property to enable classification debugging.
-   **[Field watcher](c_FieldWatcher.md#)**  
The field watcher tool tracks and displays all actions that the system performs on a selected form field.
-   **[Writing to the debug log](c_WritingToTheDebugLog.md#)**  
To write to the debug log in your client-side JavaScript, or UI policies, make a call to the global function `jslog()`.
-   **[JavaScript debug window](c_JavaScriptDebugWindow.md#)**  
The JavaScript debug window appears in a bottom pane of the user interface when an administrator turns on debugging.
-   **[JS Code Coverage Debug](js-code-coverage-debug.md#)**  
The JS Code Coverage Debug application allows administrators and application developers to log the server-side scripts triggered during a user session and then review which lines of code the system ran.

**Parent Topic:**[Scripting](../../topic/c_Script.md)

