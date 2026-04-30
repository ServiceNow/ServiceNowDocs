---
title: Create an action as an activity automation plan
description: Create an example action to configure and run as an activity from Playbooks.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Activity definitions, Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create an action as an activity automation plan

Create an example action to configure and run as an activity from Playbooks.

## Before you begin

Role required:

-   This task requires some knowledge of creating flows in Workflow Studio environment. For more information, see [Building flows](../../flow-designer/concept/flows.md).
-   This task requires some knowledge of server-side scripting. For more information, see [Server-side scripting](https://www.servicenow.com/docs/access?context=c_ServerScripting&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   admin

## About this task

Each activity definition requires an automation plan to run Workflow Studio content. The automation plan tells the Workflow Studio Playbooks builder what input values to use when running an action or subflow. An automation plan can specify static default values or can prompt playbook owners to provide dynamic values when they add an activity to a playbook.

In this example, you create a reusable Workflow Studio action to use as an activity's automation plan. The action you create associates a Task \[task\] record with a parent record.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  In the main header, click **+ New** &gt; **Action**.

    The Action Properties screen appears.

3.  In the Action Properties screen, fill in the following fields:

    |Field|Action|
    |-----|------|
    |Name|Enter `Associate Record with Parent`.|
    |Application|Leave **Global** selected.|
    |Accessible From|Leave **All application scopes** selected.|

4.  Click **Submit**.

    The Workflow Studio design environment appears.

5.  Under the Action Outline, click **Inputs**.

6.  In the Action Input header, click **+ Create Input**, and then fill in the following fields:

    |Field|Action|
    |-----|------|
    |Label|Enter `Record`.|
    |Name|Enter `record`.|
    |Type|Select **Reference.Task\[task\]**|

7.  In the Action Input header, click **+ Create Input**, and then fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Label|Enter `Parent Record`.|
    |Name|Enter `record`.|
    |Type|Select **Reference.Task\[task\]**|

8.  Click the add a new step icon \(![Add a new step icon](../../flow-designer/images/add-new-step-icon.png)\).

    The Select Step to add screen appears.

9.  Under ServiceNow Data, select the **Update Record** step.

    The **Update Record** step appears in the Action Outline under Inputs.

10. In the **Record** field, click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\), and then dot-walk to **Inputs** &gt; **Record**.

11. Under Field Values, click **+Add Field Value**, and then select **Parent** from the list.

12. Next to the **Parent** field, click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\), and then dot-walk to **Inputs** &gt; **Parent Record**.

13. Under the Action Outline, click **Outputs**.

14. Under Action Output, click **+ Create Output**, and then fill in the following fields:

    |Field|Action|
    |-----|------|
    |Label|Enter `Record`.|
    |Name|Enter `record`.|
    |Type|Select **Reference.Task\[task\]**|

15. In the Action Output header, click **+ Create Output**, and then fill in the following fields:

    |Field|Action|
    |-----|------|
    |Label|Enter `Parent Record`.|
    |Name|Enter `record`.|
    |Type|Select **Reference.Task\[task\]**|

16. In the Action Output header, click **Exit Edit Mode**.

17. Next to the **Record** output's Value column, click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\), and then dot-walk to **Inputs** &gt; **Record**

18. Next to the **Parent Record** output's Value column, click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\), and then dot-walk to **Inputs** &gt; **Parent Record**.

19. In the main header, click **Save** &gt; **Publish** to make your action available to add to an activity definition's automation plan.


## Result

You can now add your custom Workflow Studio action to an automation plan for your custom activity definition.

## What to do next

Add your custom action to an automation plan when you [Create an activity definition](create-activity-definition.md).

**Parent Topic:**[Activity definitions](../concept/activity-definitions.md)

**Related topics**  


[Create an activity definition](create-activity-definition.md)

[UI Layouts](../concept/experience-types.md)

