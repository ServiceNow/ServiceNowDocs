---
title: Script Debugger step-through and console controls
description: After the Script Debugger pauses a script, use the step-through controls to move between script lines and move between scripts in the call stack. Use the Console controls to expand console, collapse console, clear console, and rerun expressions.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Script Debugger user interface, Script Debugger, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Debugger step-through and console controls

After the Script Debugger pauses a script, use the step-through controls to move between script lines and move between scripts in the call stack. Use the Console controls to expand console, collapse console, clear console, and rerun expressions.

|Control|Icon|Description|
|:------|:---:|:----------|
|Stop debugging SHIFT+F2|![Pause debugging - SHIFT+F2 icon](../image/script-debugger-pause.png)|Stops any current debugging session, and disables the Script Debugger for the current user. The Script Debugger does not pause on breakpoints for the current user until it is restarted.|
|Start debugger - F2|![Start debugger - F2 icon](../image/script-debugger-start-debugger.png)|Enables the Script Debugger for the current user. The Script Debugger pauses on breakpoints.|
|Resume script execution - F9|![Resume script execution - F9 icon](../image/script-debugger-resume.png)|Advances from the current breakpoint to the next breakpoint. If there are no other breakpoints, the script runs to completion.|
|Step over next function call - OPTION+F9|![Step over next function - OPTION+F9 icon](../image/script-debugger-step-over.png)|Advances to the next evaluated line of script based on current conditions. The Script Debugger skips any lines of code that do not need to run because their conditions are not met. For example, when the condition of an `if` statement is not true, the debugger skips the code block for the condition.|
|Step into next function call - OPTION+F10|![Step into next function call - OPTION+F10 icon](../image/script-debugger-step-into.png)|When the Script Debugger pauses on a method call, this control allows the user to advance to the first line of executed code within the method call. Stepping into a method updates the current position within the call stack. If the user does not have read access to the method call, then this control acts like step over instead.|
|Step out of current function - OPTION+F11|![Step out of current function - OPTION+F11 icon](../image/script-debugger-step-out.png)|When the Script Debugger pauses within a method call, this control allows the user to exit the current method call and return to the calling script from the call stack. If the user is not within a method call, then this control acts like step over instead.|

|Control|Icon|Description|
|-------|----|-----------|
|Open Console|![Expand console](../image/console_expand.png)|Expands the Console.|
|Close Console|![Collapse Console](../image/console_collapse.png)|Collapses the Console.|
|Clear expressions|![Clear expressions in Console](../image/console_clear.png)|Clears all the expressions in the Console.|
|Re-execute expression|![Re-execute an expression in Console](../image/console_re-execute.png)|Re-executes the expression which is already executed.|

**Parent Topic:**[Script Debugger user interface](parts-script-debugger-interface.md)

**Related topics**  


[Set or remove breakpoints](../task/set-remove-breakpoints.md)

