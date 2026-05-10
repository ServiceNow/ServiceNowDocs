---
title: Set up a highlighted value in a form header in CSM Configurable Workspace
description: You can configure fields that appear as highlighted values in a form header in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up a highlighted value in a form header in CSM Configurable Workspace

You can configure fields that appear as highlighted values in a form header in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

After creating a highlighted value, you must link it to a highlighted value configuration if you want it to appear in CSM Configurable Workspace.

**Note:** You can also use highlighted values from CSM Agent Workspace in CSM Configurable Workspace if you link the value to the highlighted value configuration.

One highlighted value configuration, **CSM/FSM Configurable Workspace Highlighted Value Config**, is included with CSM Configurable Workspace. You can use this configuration out of the box without completing any additional configuration steps.

## Procedure

1.  Create a highlighted value.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Highlighted Values**.

    2.  Select **New**.

    3.  Fill in the fields on the Highlighted Value form and select **Submit**.

        |Field|Description|
        |-----|-----------|
        |Table|Table that contains the field that you want to highlight in the form header.|
        |Field|Field that you want to highlight.|

    4.  In the Highlighted Values list, select the record you created.

    5.  In the Highlighted Value Conditions related list, select **New**.

    6.  Fill in the fields on the Highlighted Value Condition form.

        |Field|Description|
        |-----|-----------|
        |Conditions|Condition builder where you can set the conditions for your highlighted value to display.|
        |Status|Background color. Each status has its own color, for example, Critical displays a red background, Moderate displays a purple background, and Info displays a blue background.|
        |Show icon|Toggle that makes a small circle display in addition to the background coloring.|
        |Value Override|Text that renders instead of the Status value. For example, instead of "Critical," you can display, "Address this immediately." You can reference a text value using`{{value}}`.|
        |Application|Application scope that contains the record.|
        |Order|Order that the highlighted values are evaluated.|

    7.  Select **Submit**.

2.  Add the highlighted value to the highlighted value configuration.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Highlighted Values Configurations**.

    2.  Select the configuration.

    3.  In the Highlighted Values related list, select **Edit**.

    4.  Move the desired value from the left column to the right column to add it to the selected configuration.

    5.  Select **Save**.


**Related topics**  


[Configure a highlighted value for a form header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/config-ws-highlight-value.md)

