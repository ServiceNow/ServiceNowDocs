---
title: Create a formatter and add it to a form
description: Create the formatter after creating the UI macro that defines the content.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a formatter and add it to a form

Create the formatter after creating the UI macro that defines the content.

## Before you begin

Role required: ui\_macro\_admin

## About this task

With the UI macro in place, create the formatter that references it, and add it to the form.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Formatters**.

2.  Click **New**.

3.  In the **Name** field, enter a descriptive name for the formatter.

4.  In the **Formatter** field, enter the name of the UI macro with `.xml` appended to it.

5.  In the **Table** field, select the table in which the formatter will be used.

6.  In the **Type** field, select **Formatter**.

7.  Click **Submit**.

8.  To add the formatter to a form, configure the form design and add the formatter.

    The formatter appears on the form according to your selections.


**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

**Related topics**  


[Activity formatter](../concept/c_ActivityFormatter.md#)

[Create a UI macro for a formatter](t_CreateAUIMacro.md)

[Process flow formatter](../reference/r_ProcessFlowFormatter.md#)

[Parent breadcrumbs formatter](t_TaskParentBreadcrumbsFormatter.md#)

[Approval summarizer formatter](../../service-administration/reference/r_ApprovalSummarizerFormatter.md)

[Limit the number of activity stream entries](limit-activity-stream-entries.md)

[Override a formatter with macros](t_UIMacroOverride.md)

