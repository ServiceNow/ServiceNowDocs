---
title: Script Debugger status
description: The Script Debugger status determines what debugging actions are available and what information it can display.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Debugger status

The Script Debugger status determines what debugging actions are available and what information it can display.

The Script Debugger displays its status at the bottom left of the user interface.

![The Script Debugger Status field showing the sample status EXECUTION_PAUSED](../image/script-debugger-status.png "Sample Script Debugger status")

<table id="table_dty_1dm_zw"><thead><tr><th>

Status

</th><th>

Occurs when

</th><th>

Description

</th><th>

Actions available

</th></tr></thead><tbody><tr><td>

WAITING\_FOR\_FIRST\_BREAKPOINT

</td><td>

The user opens a Script Debugger window or tab.

</td><td>

The Script Debugger is ready to pause script and display debugging information.

</td><td>

Pause script at the first breakpoint in the call stack.

</td></tr><tr><td>

EXECUTION\_PAUSED

</td><td>

-   The Script Debugger pauses on a breakpoint.
-   The user steps over, steps into, or steps out to the next line of evaluated code.

</td><td>

The Script Debugger has paused on a line of code, and the user can debug the script. Console is enabled.

</td><td>

-   Resume processing until the Script Debugger reaches the next breakpoint.
-   Step through a script.
-   Display the call stack.
-   Display transaction information.
-   Display variable values.
-   Evaluate expressions in Console during runtime.

</td></tr><tr><td>

WAITING\_FOR\_BREAKPOINT

</td><td>

-   The user resumes processing until the Script Debugger reaches the next breakpoint.
-   The user steps through a script until the Script Debugger reaches the next line of code to evaluate or the transaction completes.

</td><td>

The Script Debugger is searching for the next line of code at which to pause. Users will typically never see this status because the Script Debugger changes status after it locates the next breakpoint or script line to evaluate.

</td><td>

-   Pause script at the next breakpoint.
-   Pause script at the next script line requiring evaluation.

</td></tr><tr><td>

OFF

</td><td>

-   The user pauses the Script Debugger.
-   The user closes the Script Debugger window or tab.
-   The user session ends for any reason.
-   The administrator resets all Script Debugger instances by navigating to the `debugger_reset.do` page.

</td><td>

The Script Debugger is inactive and does not pause scripts or display debugging information.

</td><td>

-   Start the Script Debugger.
-   Open a Script Debugger window or tab.

</td></tr></tbody>
</table>## Log entries

Every time a debug transaction finishes executing, the system creates a log entry for it with a `DEBUGGED` prefix. For example:

```
2016-08-15 15:57:32 (197) Default-thread-3 900F510167112200C4098C7942415A75 *** End
#39, path: /my-app.do, user: admin, DEBUGGED total transaction time: 0:00:11.010,
transaction processing time: 0:00:11.010, network: 0:00:00.000, chars: 6,058, uncompressed
chars: 20,731, SQL time: 50 (count: 34), business rule: 0 (count: 0), phase 1 
form length 56,464, largest chunk written: 10,428, request parms size: 40, largest input read: 0
```

**Parent Topic:**[Script Debugger and Session Log](script-debugger.md)

