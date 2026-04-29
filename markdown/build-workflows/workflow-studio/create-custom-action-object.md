---
title: Create a custom action to generate an object from a record
description: Generate an object from a User record. Learn how to use an Action output to create an object from record values.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Complex data, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a custom action to generate an object from a record

Generate an object from a User record. Learn how to use an Action output to create an object from record values.

## Before you begin

Role required: admin

## About this task

Use this example to see demonstrations of these operations and steps.

-   Create action inputs for the User record fields First name, Last name, and Email.
-   Lookup a User record matching the action input values.
-   Create an action output for a contact object.
-   Save the contact object as a template.
-   Map contact object values to User record field values.
-   Test the action with a sample user.

## Procedure

1.  Create an application to store your work.

    Use the [Guided Application Creator](https://www.servicenow.com/docs/access?context=guided-app-creator&version=australia&pubname=australia-application-development&ft:locale=en-US).

    For example, create `My Application`.

2.  Navigate to **Process Automation** &gt; **Flow Designer**.

    The system displays the Workflow Studio landing page.

3.  Select **New** &gt; **Action**

    The system displays the Action Properties dialog.

4.  Enter these sample values.

    |Field|Value|
    |-----|-----|
    |Name|Create Contact Object From User|
    |Application|My Application|
    |Accessible From|All application scopes|

5.  Select **Submit**.

    The system displays the Workflow Studio interface.

6.  From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

7.  Configure the action input with these values.

    |Field|Value|
    |-----|-----|
    |Label|First name|
    |Type|String|
    |Mandatory|True|

8.  From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

9.  Configure the action input with these values.

    |Field|Value|
    |-----|-----|
    |Label|Last name|
    |Type|String|
    |Mandatory|True|

10. From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

11. Configure the action input with these values.

    |Field|Value|
    |-----|-----|
    |Label|Email address|
    |Type|String|
    |Mandatory|False|

12. From Action Outline, select **Outputs** &gt; **Create Output**.

    The system displays a new action ouput.

13. Configure the output variable with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |contact|contact|Object|False|

14. From the row for the contact Object, select **Add Child Item**.

15. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |First name|first\_name|String|True|

16. From the row for the contact Object, select **Add Child Item**.

17. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Last name|last\_name|String|True|

18. From the row for the contact Object, select **Add Child Item**.

19. Configure the child item with these values.

    |Label|Name|Type|Mandatory|
    |-----|----|----|---------|
    |Email address|email\_address|String|False|

20. From the row for the contact Object, select **Toggle Advanced Inputs**.

21. From the Advanced Options, select **Save As Template**.

    The system displays the Save As Template dialog.

22. For **Enter a Name**, enter `contact`.

23. Click **Save**.

24. Select **Exit Edit Mode**.

    The System displays the output fields you created.

25. Configure the outputs with these values.

    |Label|Value|
    |-----|-----|
    |First name|**\[step-&gt;Look Up Record step-&gt;Record-&gt;First name\]**|
    |Last name|**\[step-&gt;Look Up Record step-&gt;Record-&gt;Last name\]**|
    |Email Address|**\[step-&gt;Look Up Record step-&gt;Record-&gt;Email\]**|

    **Note:** You can select data pills from the data panel or from the Data Pill Picker button.

26. Select **Save**.

27. Select **Test**.

    The system displays the Test Action dialog.

28. Enter these test values.

    |Input|Value|
    |-----|-----|
    |First name|Abel|
    |Last name|Tuter|

29. Select **Run Test**.

    The system runs the action with the test values provided.

30. Select **Action has executed. To view the action, click here.**

    The system displays the action execution details.

31. Review the runtime value for the action Output data.

    The system displays output data in JSON format.

    For example, sample contact object JSON for the user Abel Tuter.

    ```
    {
        "contact": {
            "email_address": "abel.tuter@example.com",
            "last_name": "Tuter",
            "first_name": "Abel"
        }
    }
    ```


## Result

You have a custom action that looks up a User record and converts it into a contact object.

## What to do next

Customize the action to use your own logic.

**Parent Topic:**[Complex data](../concept/complex-data.md)

