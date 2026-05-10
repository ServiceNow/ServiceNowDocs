---
title: Script Debugger and Session Log
description: The Script Debugger enables users with the script\_debugger role to debug server-side JavaScript. Users with the log\_debugger role can use the Session Log to view and download required logs.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Debugger and Session Log

The Script Debugger enables users with the script\_debugger role to debug server-side JavaScript. Users with the log\_debugger role can use the Session Log to view and download required logs.

Users with the script\_debugger role can perform these actions using Script Debugger:

-   Have a dedicated debug transaction, which applies only to the current session.
-   Set and remove breakpoints.
-   Pause the current session at a breakpoint.
-   Evaluate expressions during runtime.
-   Step through code line-by-line.
-   Step into and out of function and method calls.
-   View the value of local and global variables.
-   View the value of private variables from function closures.
-   View the call stack.
-   View the transaction that the system is processing.
-   Turn off the script debugger to resume running paused scripts.

Use the Session Log tab to retrieve the session log for business rules, script includes, and a custom UI such as ServiceNow® Agent Workspace that has a GraphQL component. Users with the log\_debugger role can:

-   View session logs in a separate tab.
-   Download a log.
-   View logs for Agent Workspace.
-   Specify debug options to view or download only the required logs.

By default, 100 transactions and 10,000 messages appear on the Session Log tab. If the transaction or message count exceeds the default value, the session log is cleared and the next transactions or messages appear. You can configure this transaction and message count using the **glide.debugger.log.transaction.count** and **glide.debugger.log\_messages\_limit** user preferences respectively. For more information about the **glide.debugger.log.transaction.count** and **glide.debugger.log\_messages\_limit** user preferences, see [User preference settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_UserPreferenceSettings.md).

**Note:** Enable Session Log as a separate tab with Script Debugger using the **glide.debugger.log.ui** system property.

-   The **Page** option displays logs under forms and lists and on the **Session Log** tab.
-   The **Session** option displays logs only on the **Session Log** tab.

For more information about the **glide.debugger.log.ui** system property, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

When you execute a statement in the Console, the executed statement is stored in the browser cache. You can use the up arrow key to get the previous statement and down arrow key to get the next statement from the browser cache. The user preference setting,**glide.debugger.console.cached\_stmt\_limit**, defines the number of statements cached in a browser session. The default statement cache value is 20 and the maximum value is 100. You can configure the statement cache value from user preferences.

**Note:** The cached statements are not available when the browser cache is cleared or when you log in from a different browser or a different computer.

The Script Debugger can pause any server-side script that runs in an interactive transaction such as business rules, script includes, script actions, or UI actions that require a response to proceed. If the GlideSystem method isInteractive\(\) returns **True** when running the script in context, then the Script Debugger can pause it.

**Note:** Some script objects, such as script includes, can be called from multiple contexts. For example:

-   when a business rule runs a script include on a form submit that is an interactive transaction waiting on the form data to change before continuing.
-   when a scheduled job runs the same script include that is a non-interactive background transaction that can also run other scripts simultaneously.

To debug client-side scripts, you can use browser-based developers tools.

A debugger transaction remains open as long as the user session is valid. If a user logs out or their session times out, the system closes the debugger transaction.

To view debug logs, see [Display debugging logs](c_SessionDebug.md#).

**Note:** When the Script Debugger is enabled, code is executed in interpreted mode. If parts of the script are set to run in strict mode, the debugger is not able to find the correct objects and the debugger fails. The Script Debugger must run on scripts outside of strict mode.

-   **[Access the Script Debugger](../task/launch-script-debugger.md)**  
Developers can access the Script Debugger from the application navigator, Studio, or from the syntax editor.
-   **[Script Debugger user interface](../reference/parts-script-debugger-interface.md)**  
The Script Debugger user interface \(UI\) displays information about breakpoints set, the call stack and line number of the currently executing script line, details about variables and transactions, and status of console.
-   **[Evaluate expressions in runtime using Console](../task/evaluate-expressions.md)**  
Define, declare, and verify new variables and functions while you debug a script in runtime using Console. The script execution must be paused to use Console.
-   **[Set or remove breakpoints](../task/set-remove-breakpoints.md)**  
Set breakpoints or conditional breakpoints to pause scripts at specific lines, and remove breakpoints when you are done debugging them.
-   **[Set or remove logpoints](../task/set-remove-logpts.md)**  
Set breakpoints or conditional logpoints to log messages to the console at specific lines, and remove logpoints when you are done debugging them.
-   **[Script Debugger multiple developer support](multiple-developer-support.md)**  
The Script Debugger allows multiple developers to debug their own transactions without affecting each other.
-   **[Script Debugger impersonation support](impersonation-support.md)**  
You can use the Script Debugger while impersonating another user, but only if the impersonated user has the script\_debugger role and has read access to the target script.
-   **[Script Debugger Scripts - Background support](scripts-background-support.md)**  
The Scripts - Background module does not support setting breakpoints directly in the script field. You can however, set breakpoints in the script objects called or triggered by the Scripts - Background module.
-   **[Domain separation and Script Debugger](domain-separation-script-debugging.md)**  
Domain separation is supported in Script Debugger. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

