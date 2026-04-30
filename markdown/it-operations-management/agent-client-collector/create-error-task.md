---
title: Create a task to address Agent Client Collector errors
description: Create tasks to resolve errors relating to the Agent Client Collector \(ACC\). Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create a task to address Agent Client Collector errors

Create tasks to resolve errors relating to the Agent Client Collector \(ACC\). Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.

## Before you begin

Role required: agent\_client\_collector\_user, itil

## About this task

After a task is created for an error, all errors with a matching error code get grouped into the task. When the task is resolved, all errors in the task are automatically resolved, unless an error is marked as **Ignored**.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Issues**.

    The **ACC Error Messages** page appears.

2.  Hover under the search icon to the left an error code.

    The preview icon ![Preview icon](../image/preview-icon.png) appears.

3.  Select the preview icon and select the **Open Record** button on the resulting pop-up window.

    The **ACC Error Message** page appears, containing details of the selected error.

    ![ACC Error Message form](../image/acc-error-message-form.png)

    -   Use the string in the **Key** field to identify the policy or agent record that is associated with the given error.
    -   A suggestion for resolving the error appears in the **ACC Error Message Suggestion** section at the bottom of the page. Select the link for more details on the suggestion.
    -   The suggestion in the **ACC Error Message Suggestion** section isn't done automatically. It must be performed by an administrator to resolve the error.
4.  Select the **Create ACC Error Task** button to create a task to address the error.

    The **ACC Error Task** page appears, displaying the newly created error task.

    ![ACC Error Task page](../image/acc-error-task-page.png)

    -   All errors with an error code matching the selected error are included in the new task.
    -   Entries listed on the **Active Errors** tab are errors which haven’t been resolved and aren’t marked as Ignored.
    -   Entries listed on the **Inactive Errors** tab are errors which are either resolved or marked as Ignored.
5.  Configure the fields on the page.

    For details on the available fields, see [ACC Error Task page](../reference/error-task-page.md).

6.  Select **Update** to save the newly created task.


**Related topics**  


[Ignore an Agent Client Collector error](ignore-acc-errors.md)

