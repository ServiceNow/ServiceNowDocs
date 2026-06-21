---
title: Use Generative AI Controller with Workflow Studio
description: Summarize the information automatically and add it to a form with the Generative AI Controller Summarize action in Workflow Studio. You can build a flow to summarize any field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/generative-ai-controller/use-generative-ai-controller-with-flow-designer.html
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

For more information on tracking Generative AI Controller usage, see Monitoring Now Assist usage.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **New** &gt; **Flow**.

3.  Enter the name of the flow, such as `Summarize Comments and Work Notes`.

4.  Select **Submit**.

5.  Select **Add a trigger**.

6.  Select when you would like the flow to run.

    To follow this example, select **Record** &gt; **Updated**. \[Omitted image "new-flow-trigger-select.png"\] Alt text: Trigger action panel open and Updated is highlighted.

7.  Select the table that the flow should run on.

    For this example, select the Incident table.

8.  Select the **Add filters** button to add a condition for the flow.

    The Condition is `State changes to Resolved`. \[Omitted image "new-flow-trigger-condition-filled.png"\] Alt text: Trigger update record filled in, including the condition.

9.  Select **Done**.

10. Under Actions, select **Add an Action**, **Flow Logic**, or **Subflow** and then select **Action** to open the Actions panel.

    \[Omitted image "new-flow-first-action.png"\] Alt text: Open action panel.

11. Select the **Generative AI Controller** &gt; **Summarize** action and select it.

    \[Omitted image "new-flow-first-action-summarize-select.png"\] Alt text: Generative AI Controller Summarize action.

12. Drag a data pill from the Data panel or select the data pill picker icon \( \[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon.\) to search.

    In this case, drag the **Trigger** &gt; **Incident Record** &gt; **Comments and Work notes** pill.

    **Note:** If the field that you want to summarize isn't a String field, you must cast the field as a String. You can cast the field as a String with scripting or by adding text to the **textToSummarize** field in addition to the data pill, like in the following example.

    \[Omitted image "new-flow-data-pill-picker-comments-and-worknotes-filled.png"\] Alt text: Generative AI Controller Summarize action filled in to summarize comments and work notes.

13. Select **Done**.

14. Add an action by selecting **Add an Action, Flow Logic, or Subflow**.

15. In the action selector, search for **Update Record** and select the action.

    \[Omitted image "new-flow-action-update-record.png"\] Alt text: Update Record action in the Actions panel

16. Drag the **Trigger** &gt; **Incident Record** data pill into the **Record** field or select the icon to search.

    The Table field is filled in automatically based on the Trigger record.

    \[Omitted image "new-flow-update-record-record-data-pill.png"\] Alt text: Filled-in updated record with data pill for target record.

17. Select **Add field value** and search for the fields that you want to update.

    In the following example, select **Resolution notes**.

18. Add the **Summarize** &gt; **Response** data pill into the data field by dragging it from the Data panel or with the data pill picker.

    \[Omitted image "new-flow-summarize-action-response-in-field.png"\] Alt text: Filled-in Resolution notes field in the update record action.

19. Select **Done**.

    \[Omitted image "new-flow-update-record-filled.png"\] Alt text: Resolution notes field with summarize response included.

20. Save the flow by selecting **Save**.


## What to do next

After you've saved the flow, activate it to migrate it to production or test it further.

