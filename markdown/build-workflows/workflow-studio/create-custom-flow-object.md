---
title: Create a custom flow to generate an object for each record in a list
description: Generate an object for each User record in a list. Learn how to use flow logic to iterate through a list of records.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Complex data, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a custom flow to generate an object for each record in a list

Generate an object for each User record in a list. Learn how to use flow logic to iterate through a list of records.

## Before you begin

-   Role required: admin
-   [Create a custom action to generate an object from a record](create-custom-action-object.md)

## About this task

Use this example to see demonstrations of these operations and steps.

-   Create a flow that runs on a daily schedule.
-   Look up User records filtered by the Department provided as an input.
-   Add flow logic that runs for each User record you looked up previously.
-   Create a contact object for each User record using the custom action you created previously.
-   Create a log message for each User record.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    The system displays the Workflow Studio landing page.

2.  Select **New** &gt; **Flow**

    The system displays the Flow Properties dialog.

3.  Enter these sample values.

    |Field|Value|
    |-----|-----|
    |Name|Create Contact Objects From Users|
    |Application|My Application|
    |Run As|User who initiates session|

4.  Select **Submit**.

    The system displays the Workflow Studio interface.

5.  Select **Click to add a Trigger** &gt; **Date** &gt; **Daily**.

6.  Select **Done** to close the trigger.

7.  Select **Click to add an Action, Flow Logic, or Subflow** &gt; **Action** &gt; **ServiceNow Core** &gt; **Look Up Records**.

    The system adds the action to the flow.

8.  For **Table**, select **User \[sys\_user\]**.

9.  For **Conditions**, add these values.

    -   **\[Department\]\[is\]\[Development\] \[AND\]**
    -   **\[Email\]\[is not empty\]**
10. Configure these field values.

    |Field|Value|
    |-----|-----|
    |Order by|Name|
    |Sort|a to z|
    |Max Results|1000|

11. Select **Done** to close the action.

12. Select **Click to add an Action, Flow Logic, or Subflow** &gt; **Flow Logic** &gt; **For Each**.

    The system adds the flow logic to the flow.

13. For **Items**, select **\[1-&gt;User Records\]**.

    **Note:** You can select the Action 1 **User Records** data pill from the data panel or from the Data Pill Picker button.

14. Select **Done** to close the flow logic.

15. Select the plus icon to add a child item to the For Each flow logic.

16. Select **Action** &gt; **My Application** &gt; **Create Contact Object**.

17. For **userRecord \[User\]**, select **\[2-&gt;User Record\]**.

    **Note:** You can select the Action 2 **User Record** data pill from the data panel or from the Data Pill Picker button.

18. Select **Done** to close the flow logic action.

19. Select the plus icon to add a child item to the For Each flow logic.

20. Select **Action** &gt; **ServiceNow Core** &gt; **Log**.

21. For **Message**, select **\[2.1-&gt;contact\]**.

    **Note:** You can select the Action 2.1 **contact** data pill from the data panel or from the Data Pill Picker button.

22. Select **Done** to close the flow logic action.

23. Select **Save**.


**Parent Topic:**[Complex data](../concept/complex-data.md)

