---
title: Script Tracer and debugging scripts
description: The Script Tracer can help you filter your debugging search to quickly narrow down script problems. You can identify lines of scripts in the Glide record that have undergone change during execution. Finding those specific lines of scripts rather than doing a wide search helps save time and improves productivity.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Script Tracer and debugging scripts

The Script Tracer can help you filter your debugging search to quickly narrow down script problems. You can identify lines of scripts in the Glide record that have undergone change during execution. Finding those specific lines of scripts rather than doing a wide search helps save time and improves productivity.

## Overview

Use the Script Tracer to narrow your search so you can debug scripts and business rules more efficiently. You can find the Script Tracer by searching in the left navigation pane.

**Note:** To use the Script Tracer, your role must be admin.

<table id="table_s5h_xzm_knb"><tbody><tr><td>

![Script Tracer in the navigation pane](../image/script-tracer-nav-menu.png)

</td><td>

![Script Tracer tab](../image/script-tracer-tab.png)

</td></tr></tbody>
</table>Once you enable Script Tracer and execute a UI transaction, the Tracer searches through all the scripts being executed. The following filters are available:

-   **File type**: Search for a specific file type
-   **Table**: Look in the specific table for the script being executed

The Script Tracer searches for changes in the script during execution and presents them in a list for you to examine. When you click **Start Tracer**, the Tracer begins searching for changes in the Glide record. You can click the **Debug Script** button at any time to see the script itself.![Script difference output](../image/script-tracer-diff-line.png)

Use the tabs to see specific information from the Tracer.

The **State** tab displays the differences between the old and new scripts.

-   By default, the **Show only changed values** check box is enabled, so you can avoid fields that have not changed.
-   To view all the fields \(changed or not\), you can clear that check box.

**Note:** If the file is not reflected in the trace statement, it means the changes in the Glide record is not recognized by the system.

If there are any errors, they display at the top of the State tab, with their line numbers and error message displayed in order of occurrence.![Errors listed in the State tab.](../image/script-tracer-error.png)

-   **Script**: Displays the line of changed scripts that the Glide record has undergone during execution. You can view the entire line of script by clicking the **Show Script** button.
-   **Transaction**: Shows all transaction records of the trace
-   **Debug Script**: Opens the script in Debugger to debug the script
-   **View File**: Opens the script in the ServiceNow platform for editing
-   **Clear trace**: Clears the trace when you are finished.

## Limiting the tracer

You may want to set a limit for your trace so that you don't generate too many returns. By default there will be up to 1,000 lines of script traced. Once this number is reached you must clear the trace and start tracing again. If you want to change the maximum number of lines for tracing you can configure your limit using the property **glide.debug.trace.trace\_line\_limit**.

Since each trace you run is new, make sure you're finished reading the results of one trace before clearing it and beginning another one.

To learn more, see [Debugging scripts](script-debug-overview.md).

**Parent Topic:**[Script Debugger and Session Log](script-debugger.md)

