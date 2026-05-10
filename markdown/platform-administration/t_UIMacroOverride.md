---
title: Override a formatter with macros
description: The system uses formatters to handle complex rendering of specific form elements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Override a formatter with macros

The system uses formatters to handle complex rendering of specific form elements.

## Before you begin

Role required: ui\_macro\_admin

## About this task

Examples of form elements rendered by formatters in the base platform are:

-   Activity formatter: Displays the list of activities, or history, on a task form.
-   Process flow formatter: Displays the different stages in a linear process flow across the top of a record.
-   Task parent breadcrumbs formatter: Provides breadcrumbs to show the parent or parents of the current task.
-   Approval summarizer formatter: Displays dynamic summary information about the element being approved.

A UI macro can override formatters provided in the base system.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Macros**.

2.  Click **New**.

3.  In the **Name** field, enter the same name as the formatter you want to override, but omit the .xml extension.

4.  Complete the remaining fields on the form.

5.  Click **Submit**.


## Example

This example shows the form that defines the existing approval summarizer formatter:

![Approval summarizer formatter](../image/Formatter.png)

Here is the form for the UI macro that overrides the approval summarizer formatter:

![Override the formatter](../image/FormatterOverride.png)

**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

**Related topics**  


[Create a UI macro for a formatter](t_CreateAUIMacro.md)

[Create a formatter and add it to a form](t_CreateAFormatter.md)

