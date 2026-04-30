---
title: Assign a trigger to a flow
description: Now that you created a trigger, use Workflow Studio to specify the flow a trigger executes. The flows can provide alerts for unexpected behavior.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Assign a trigger to a flow

Now that you created a trigger, use Workflow Studio to specify the flow a trigger executes. The flows can provide alerts for unexpected behavior.

## Before you begin

Role required: admin

## About this task

Triggers, by themselves, execute nothing. After defining a trigger in MetricBase, you use Workflow Studio to associate the trigger with a flow.

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **Trigger Flows.**.

2.  Select **New Flow**.

3.  Fill in the fields.

<table id="choicetable_hsk_2zm_pgb"><thead><tr><th align="left" id="d408325e95">

Field

</th><th align="left" id="d408325e98">

Description

</th></tr></thead><tbody><tr><td id="d408325e104">

**Flow name**

</td><td>

Name of the flow to execute.

</td></tr><tr><td id="d408325e113">

**Description**

</td><td>

Explanation of what the flow does and why you are associating this flow with the trigger.

</td></tr><tr><td id="d408325e122">

**Application**

</td><td>

Application scope to create your flow in. The value, **Global**, is the default.

</td></tr><tr><td id="d408325e134">

**Protection**

</td><td>

Option to make the flow read-only. Selecting read-only prevents users who do not own the application scope from changing the flow. You can only select a value when you create the flow in an application scope you own.

</td></tr><tr><td id="d408325e144">

**Run As**

</td><td>

Choose whether the flow runs as **System User** or **User who initiates the session** \(the current user\). For example, comments to incident records or approval emails should come from the current user making the comment or approval. Flows run by the initiating user respect settings that are user-specific like date/time format. The **Run As** setting does not apply to child subflows.

**Note:** If you select **User who initiates the session**, ensure that security restrictions \(ACLs\) do not prevent the users who trigger the flow from performing the flow actions.

</td></tr><tr><td id="d408325e170">

**Run with roles**

</td><td>

Select the roles can run the flow. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select **Add a trigger** to specify the trigger that kicks off this flow.

6.  In the dialog box that appears, scroll, and select MetricBase for the trigger type.

7.  Under **TRIGGER**, fill in the form to define the trigger to associate with this flow.

    1.  In the **MetricBase Trigger** list, select a trigger by either selecting the magnifying glass to select an existing trigger or selecting the plus sign \(+\) to define a new trigger.

    2.  Add requirements for the flow to execute by adding filter conditions.

    3.  Beside **Condition Script**, select the magnifying glass to select a Condition Script or click the plus \(+\) to create a script.

        Condition scripts add additional requirements for a trigger to execute a flow.

    ![Condition script in Workflow Studio.](../image/condition-script-flow-designer.png)

8.  Under **ACTIONS**, select **Click to add an Action, Flow Logic, or Subflow**

    1.  When selecting an action, select an action category in the first column of the dialog box, and a flow action in the second column.

    2.  Create combinations of different actions, flow logics, and subflows to get the desired behavior.

    3.  Select **Done** to complete each part of the flow action.

    ![Selecting a flow.](../image/flow-action.png)

9.  Select **Save**.

10. Test the flow.

    1.  In the flow tab in Workflow Studio, select **Test**.

    2.  Select the trigger **Level** to test, provide the **time of metric event**, and what **record** is triggering.

        Different triggers may execute different flows. ![Test the flow.](../image/test-flow.png)

        **Note:** When you test a flow, the system does not execute the trigger, and therefore does not create a record. By selecting a record in the Test flow dialog box, the system acts as if that record was just created. For more information, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    3.  Select **Submit**.

        The test completes. Select the message to view the flow execution details. Edit the settings if necessary, save again, and then retest.

11. Select **Activate** to activate the trigger.

    The flow does not execute unless you activate it.


