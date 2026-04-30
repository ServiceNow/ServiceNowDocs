---
title: Use Generative AI Controller with Workflow Studio
description: Summarize the information automatically and add it to a form with the Generative AI Controller Summarize action in Workflow Studio. You can build a flow to summarize any field.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Use Generative AI Controller with Workflow Studio

Summarize the information automatically and add it to a form with the Generative AI Controller Summarize action in Workflow Studio. You can build a flow to summarize any field.

## Before you begin

Role required: admin

## About this task

In this example, you can build a flow to summarize the comments in the work notes of an incident and use that summary in the resolution notes.

For more information on tracking Generative AI Controller usage, see [Monitoring Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **New** &gt; **Flow**.

3.  Enter the name of the flow, such as `Summarize Comments and Work Notes`.

4.  Select **Submit**.

5.  Select **Add a trigger**.

6.  Select when you would like the flow to run.

    To follow this example, select **Record** &gt; **Updated**. ![Trigger action panel open and Updated is highlighted.](../image/new-flow-trigger-select.png)

7.  Select the table that the flow should run on.

    For this example, select the Incident table.

8.  Select the **Add filters** button to add a condition for the flow.

    The Condition is `State changes to Resolved`. ![Trigger update record filled in, including the condition.](../image/new-flow-trigger-condition-filled.png)

9.  Select **Done**.

10. Under Actions, select **Add an Action**, **Flow Logic**, or **Subflow** and then select **Action** to open the Actions panel.

    ![Open action panel.](../image/new-flow-first-action.png)

11. Select the **Generative AI Controller** &gt; **Summarize** action and select it.

    ![Generative AI Controller Summarize action.](../image/new-flow-first-action-summarize-select.png)

12. Drag a data pill from the Data panel or select the data pill picker icon \( ![Data pill picker icon.](../image/data-pill-picker-icon.png)\) to search.

    In this case, drag the **Trigger** &gt; **Incident Record** &gt; **Comments and Work notes** pill.

    **Note:** If the field that you want to summarize isn't a String field, you must cast the field as a String. You can cast the field as a String with scripting or by adding text to the **textToSummarize** field in addition to the data pill, like in the following example.

    ![Generative AI Controller Summarize action filled in to summarize comments and work notes.](../image/new-flow-data-pill-picker-comments-and-worknotes-filled.png)

13. Select **Done**.

14. Add an action by selecting **Add an Action, Flow Logic, or Subflow**.

15. In the action selector, search for **Update Record** and select the action.

    ![Update Record action in the Actions panel](../image/new-flow-action-update-record.png)

16. Drag the **Trigger** &gt; **Incident Record** data pill into the **Record** field or select the icon to search.

    The Table field is filled in automatically based on the Trigger record.

    ![Filled-in updated record with data pill for target record.](../image/new-flow-update-record-record-data-pill.png)

17. Select **Add field value** and search for the fields that you want to update.

    In the following example, select **Resolution notes**.

18. Add the **Summarize** &gt; **Response** data pill into the data field by dragging it from the Data panel or with the data pill picker.

    ![Filled-in Resolution notes field in the update record action.](../image/new-flow-summarize-action-response-in-field.png)

19. Select **Done**.

    ![Resolution notes field with summarize response included.](../image/new-flow-update-record-filled.png)

20. Save the flow by selecting **Save**.


## What to do next

After you've saved the flow, activate it to migrate it to production or test it further.

