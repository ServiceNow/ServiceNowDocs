---
title: Parts of the user interface
description: The Script Debugger interface displays information about breakpoints set, the call stack and line number of the currently executing script line, details about variables and transactions, and status of console.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Parts of the user interface

The Script Debugger interface displays information about breakpoints set, the call stack and line number of the currently executing script line, details about variables and transactions, and status of console.

![Script debugger not paused](../image/script_debugger_not_paused.png "Script Debugger Not Paused")

![Script debugger paused](../image/script_debugger_paused.png "Script Debugger Paused")

|User interface element|Description|
|----------------------|-----------|
|Breakpoints|Displays a list of the breakpoints set by script type, script name, and line number. The debugger updates this list as you add and remove breakpoints.|
|Call stack|Displays a list of script calls that preceded or invoked the current line number. This information is only visible when the debugger pauses on a breakpoint.|
|Transaction details|Displays information about the current transaction. This information is only visible when the debugger pauses on a breakpoint.|
|Status|Displays if the debugger is waiting for a breakpoint, paused on a breakpoint, or has encountered an exception.|
|User|Displays the name of the user who is running the current debugger session.|
|Coding pane header|Displays the script type and name of the script in the coding pane.|
|Breakpoint icon|Indicates the line number where the debugger pauses when evaluating the current script.|
|Pause debugging button|Stops any current debugging session, and disables the Script Debugger for the current user. The Script Debugger doesn't pause on breakpoints for the current user until it's restarted.|
|Console|Displays a command line interface used for evaluating expressions during runtime. The console is available only when the script execution is paused.|
|Resume script execution button|Advances from the current breakpoint to the next breakpoint. If there are no other breakpoints, the script runs to completion.|
|Step over next function call button|Advances past the method that's about to be called, executing the method as a single step.|
|Step into next function call|Advances to the first line of executed code within a method call. Stepping into a method updates the current position within the call stack. If the user doesn't have read access to the method call, then this control acts like step over instead.|
|Step out of current function|Exits from current method call and returns to the calling script from the call stack. If the user isn't within a method call, then this control acts like step over instead.|
|Local|Displays a list of local scope JavaScript variable names and their values. This information is only visible when the debugger pauses on a breakpoint.|
|Closures|Displays a list of global scope JavaScript variable names and their values set by function closure. This information is only visible when the debugger pauses on a breakpoint.|
|Global|Displays a list of global scope JavaScript variable names and their values. This information is only visible when the debugger pauses on a breakpoint.|

## Session Log

![Session log user interface elements](../image/session-log.png "Session log")

|User interface element|Description|
|----------------------|-----------|
|Transactions|Transaction ID. Displays information about the current transaction.|
|Filter for log text|Field to enter text to filter the logs that contain a specific text.|
|Debug Output|Option to filter logs based on the dynamically loaded debug output types. For example, **Security Rule**.|
|Apps|Option to filter logs based on the dynamically loaded apps. For example, **Service Management Integrations**.|
|Message Type|Option to filter logs based on the dynamically log levels. For example, **Info**.|
|Clear log|Clears all logs.|
|Download log|Download the logs in HTML file format.|
|Settings|Session debug options. For information about the debug options, see [Session debug](../concept/c_SessionDebug.md#).|

**Parent Topic:**[Script Debugger and Session Log](../concept/script-debugger.md)

