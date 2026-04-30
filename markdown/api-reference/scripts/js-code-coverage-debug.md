---
title: JS Code Coverage Debug
description: JS Code Coverage Debug allows administrators and application developers to log the server-side scripts triggered during a user session and then review which lines of code the system ran.The JS Code Coverage application highlights script fields to indicate whether the system ran or skipped each line.You can activate the JS Code Coverage Debug plugin \(com.glide.js.coverage\) if you have the admin role.Use JS Code Coverage Debug to record a user session and then review which server-side scripts and lines of code the system ran.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# JS Code Coverage Debug

JS Code Coverage Debug allows administrators and application developers to log the server-side scripts triggered during a user session and then review which lines of code the system ran.

Users with the js\_coverage\_debugger role can debug server-side scripts without having to set breakpoints or review onscreen debug messages. Instead, the system saves script usage data in the JavaScript Code Coverage \[sys\_js\_code\_coverage\] table. Each JavaScript Code Coverage record contains:

-   The user session that called the script.
-   The script record the system called identified by table, sys\_id, and script field.
-   The script record the system called identified by type and name.
-   The transaction that called the script.
-   The start time of the transaction.
-   The contents of the script field highlighted to indicate which lines the system ran.

**Note:** JS Code Coverage Debug doesn't log information for client-side scripts.

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

## JS Code Coverage highlighting

The JS Code Coverage application highlights script fields to indicate whether the system ran or skipped each line.

The color of the highlight indicates how the system evaluated the code line.

Administrators and application developers can use this information to conduct more targeted debugging activities such as using the Script Debugger to determine why script conditions are not being met.

![Sample code highlighting](../image/js-code-coverage-highlighting.png "Sample code highlighting")

|Highlight color|Description|
|---------------|-----------|
|Green|This is an executable line of code that the system ran during the session.|
|Red|This is an executable line of code that the system skipped for some reason. The system may have skipped an executable line of code because the necessary script conditions were not met or because the script function was never called. You may want to use the Script Debugger to determine why the system skipped the line of executable code.|
|Gray|This is a non-executable line of code such as white space, code comment, or a portion of an expression split across multiple lines that cannot run on its own.|

## Activate JS Code Coverage Debug

You can activate the JS Code Coverage Debug plugin \(com.glide.js.coverage\) if you have the admin role.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


### What to do next

To see the components the plugin installed, refresh the plugin form and select the **Plugin Files** related list.

## Debug with JS Code Coverage Debug

Use JS Code Coverage Debug to record a user session and then review which server-side scripts and lines of code the system ran.

### Before you begin

Role required: js\_coverage\_debugger or admin

### Procedure

1.  Navigate to **All** &gt; **JS Code Coverage Debug** &gt; **Enable Coverage**.

    The system logs which server-side scripts and code lines the system runs as well as displays session debug messages in the JS Code Coverage namespace.

    ![Debug with code coverage](../image/js-code-coverage-session-debug.png)

2.  Navigate to the table or page whose logic you want to test.

    For example, navigate to **Incident** &gt; **Create New**.

3.  Trigger the server-side script or scripts you want to test.

    For example, create an incident with an associated configuration item to test several business rules.

4.  When you have completed testing, navigate to **JS Code Coverage Debug** &gt; **Disable Coverage**.

    The system stops logging script and code lines run.

5.  Navigate to **JS Code Coverage Debug** &gt; **Coverage Data**.

    The system displays the list of coverage data associated with the current user session.

6.  Select the script or transaction you want to review.

    |Column|Description|
    |------|-----------|
    |Script Name|Displays the script run by table name, sys\_id value, and script field.|
    |Script Reference|Displays the script run by script type and name.|
    |Transaction Name|Displays the transaction that called the script by thread ID and URI.|

    The system displays the JS Code Coverage Debug record.

    ![JS code coverage debug section](../image/sample-code-coverage-incident-events.png)

7.  Review the **Script** field to determine which lines of code the system ran.


### What to do next

Use the code coverage information to do more targeted debugging activities such as set breakpoints and review variable values with the Script Debugger. For more information, see [Script Debugger and Session Log](script-debugger.md).

