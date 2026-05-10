---
title: Process flow formatter
description: The process flow formatter provides a graphical summary of the stages in a process. The formatter is typically shown at the top of forms that are part of a process.You can activate the Process Flow Formatter plugin.You can create a process flow formatter stage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Process flow formatter

The process flow formatter provides a graphical summary of the stages in a process. The formatter is typically shown at the top of forms that are part of a process.

Each record on the Flow Formatter \[sys\_process\_flow\] table represents a process stage and can have a different condition applied to it. When specified conditions are fulfilled, the formatter highlights the current stage and places a check mark next to all previous stages.

These examples show a workflow in Core UI interface.



![image.process-flow]

When any formatter stages are defined for a table, they appear on the form associated with that table in the order specified, assuming the formatter has been added to the form.

**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

## Activate the process flow formatter

You can activate the Process Flow Formatter plugin.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## Create a process flow formatter

You can create a process flow formatter stage.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Process Flow**.

2.  Click **New**.

3.  Complete the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Table|Select a table for this process flow formatter.|
    |Name|Enter a name to identify the formatter.|
    |Label|Enter the name to be displayed in the form configuration slushbucket.|
    |Active|Select the check box to ensure that the formatter stage is active. When the check box is cleared, the formatter stage does not appear in the flow display.|
    |Order|Enter a number to indicate where in the process flow the formatter will be displayed. Formatters are arranged with the lowest number on the left and the highest number on the right.|
    |Condition|Use the condition builder to set the conditions under which the formatter is highlighted as current. Any field available in the condition builder, such as SLA or Impact, can be used to trigger a process flow stage.|
    |Description|Describe the process flow formatter. This description does not appear on the actual formatter.|

4.  Repeat as necessary for each stage.


