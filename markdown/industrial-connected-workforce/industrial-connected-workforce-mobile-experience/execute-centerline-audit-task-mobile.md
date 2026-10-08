---
title: Execute a centerline audit task
description: Execute a centerline audit task with the Industrial Connected Workforce Mobile Experience to measure process parameters against published standards and submit your results from the shop floor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/execute-centerline-audit-task-mobile.html
release: australia
product: Industrial Connected Workforce Mobile Experience
classification: industrial-connected-workforce-mobile-experience
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [centerline audit, execute centerline task, setting group, parameter measurement]
breadcrumb: [Use, Industrial Connected Workforce Mobile Experience, Industrial Connected Workforce]
---

# Execute a centerline audit task

Execute a centerline audit task with the Industrial Connected Workforce Mobile Experience to measure process parameters against published standards and submit your results from the shop floor.

## Before you begin

Role required: sn\_icw\_ctl.user

The centerline audit task must have an **Active material** set before you can start execution. If it is not set, edit the task to add one. For more information, see [View and edit a centerline audit task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/view-edit-centerline-audit-task-mobile.md).

## Procedure

1.  Navigate to the **Tasks** tab and open the centerline audit task.

2.  On the **Details** tab, select **Start**.

    The execution screen opens and displays the parameters organized by setting group. Each setting group appears as a separate section.

3.  Use the section navigator to move between setting groups.

    You can tap any section to jump directly to it without completing the previous sections. A progress indicator shows which sections are complete and which still require input. The sections are numbered in the order defined in the setting configuration.

4.  For each parameter, enter the measured value in the input field.

    Parameters can be of the following types:

    -   Numeric: Enter the measured value. The unit of measurement is displayed alongside the input field.
    -   Pass/fail: Select the result from the available options.
    -   Enumeration: Select the applicable value from the drop-down list.
    As you enter each value, the parameter card shows whether the result is within specification. Colors indicate the status: green for compliant, amber or red for out of specification.

5.  Select the three-dot menu on the parameter card, then select **Open details** to view the full specification for a parameter.

    For more information about the setting definition detail screen, see [Open setting definition details during a centerline audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/open-setting-definition-details-mobile.md).

6.  To attach a photo or add a work note to a parameter result, use the attachment and note options on the parameter card.

7.  After entering all parameter values, select **Submit**.

    If any parameter results are outside the specification limits, a deviation is automatically created for each non-compliant parameter when you submit. You do not need to create the deviations manually. For more information, see [Create a deviation from a centerline task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/create-deviation-from-centerline-task-mobile.md).


## Result

The task is submitted and its state changes to **Submitted**. After all requirements are verified, the state changes to **Closed Complete**. Any out-of-specification parameters have associated deviations created automatically.

-   **[Open setting definition details during a centerline audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/open-setting-definition-details-mobile.md)**  
View the full specification for a setting definition during centerline audit execution without leaving the audit.

**Parent Topic:**[Using the Industrial Connected Workforce Mobile Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/using-icw-mobile-experience.md)

