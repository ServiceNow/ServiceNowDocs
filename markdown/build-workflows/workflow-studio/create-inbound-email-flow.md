---
title: Create a flow with an inbound email trigger
description: Start a flow when your instance receives an email.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow with an inbound email trigger

Start a flow when your instance receives an email.

## Before you begin

Role required: flow\_designer or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **+ New** &gt; **Flow**.

3.  In the flow properties, set **Run as** to **User who initiates session**.

    **Important:** Inbound email flows use the email sender as the user who initiates the session. If the system doesn't recognize the sender, the inbound email flow runs as the Guest user. Setting the inbound email flow to run as the user who initiates the session ensures that the flow actions are limited by user access controls. If the initiating user needs elevated privileges for some reason, have the inbound email flow call a subflow that runs with the required roles.

4.  In the Trigger section, select the plus icon \(![Plus icon](../../../build/app-engine-studio/image/plus-icon.png)\) to add a trigger.

5.  Select **Inbound Email**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Email conditions|Conditions to qualify which emails start your flow. The condition builder uses fields from the Email \[sys\_email\] table. For example, to trigger a flow for an inbound email in which a user replies to a system notification, set the condition to **\[Receive type\] \[is\] \[Reply\]**.|
    |Reply Record Type|Table that is associated with the target email. For example, to trigger a flow from a reply email that a user sends from an incident record notification, select **Incident \[incident\]**.|

7.  Select **Done**.

8.  Add actions, subflows, and flow logic to the flow.

9.  Add stages to the flow to report progress to the requester.

    See [Flow and subflow stages](../concept/flow-designer-stages.md).

10. Test the flow.

    To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.. For more information, see [Test a flow](flow-test.md).

11. If the test is successful, activate the flow.

    For more information, see [Activate a flow](flow-activate.md).


## Result

When an inbound email meets the conditions that you set, the associated flow triggers and runs the actions.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

