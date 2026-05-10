---
title: Set up a flow with external trigger definition
description: Set up a flow that responds to an event-driven external trigger from a third-party system and executes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Set up a flow with external trigger definition

Set up a flow that responds to an event-driven external trigger from a third-party system and executes.

## Before you begin

Role required: flow\_designer

Subscription required: Integration Hub Enterprise pack

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Create New** &gt; **Flow**.

    ![Create Flow button.](../images/create-flow.png)

3.  Fill out the **Flow properties** form.

<table id="table_kdg_zxh_ldb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify your flow. The system creates the internal name of the flow from this name.

</td></tr><tr><td>

Description

</td><td>

Description of your flow.

</td></tr><tr><td>

Application

</td><td>

Application scope to create your flow in. Global is the default.

</td></tr><tr><td>

Protection

</td><td>

Specify if the flow is read-only. **Note:** This is an optional field with two values: None and Read-only. Choose read-only if the flow is within an application scope that you own.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 **Note:** By default, flows run as the user who initiates the session.

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see [OAuth 2.0 credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/oauth-2-credentials.md).

 When flows run as the user who initiates the session, the system limits flow actions by user Access Control Rule \(ACL\) restrictions. Ensure that security restrictions don't prevent users who trigger the flow from performing flow actions. Flows run by the initiating user also respect user-specific settings such as date/time formats.

 **Note:** Inbound email flows ignore this setting and always run as the user who initiates the session. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr></tbody>
</table>4.  Select **Submit**.

    **Note:** If this is your first time in Workflow Studio, a welcome screen appears. You can choose to either take the welcome tour or skip the tour.

5.  Add a trigger to your flow.

    1.  Under the TRIGGER section, select **Add a trigger**.

    2.  Under the INSTALLED SPOKES heading, select a spoke from the Trigger list.

        ![Select spoke.](../images/select-spoke.png)

    3.  Select the predefined external trigger definition.

        ![External trigger definition.](../images/select-external-trigger-definition.png)

    4.  To define the conditions for the flow to execute, in the Condition 1 field, drag the appropriate data pill and enter the value.

        ![Datapill use.](../images/datapill-flow.png)

    5.  To define an extra condition, select **OR** or **AND**.

        A condition field is added.

    6.  In the condition field, drag the appropriate data pill and enter the value.

    7.  Select **Done**.

        You've set up the trigger.

6.  Set up the actions from the Action Picker.

    1.  Under ACTIONS, select ![Action Picker icon.](../images/action-designer.png).

    2.  Select **Action**.

    3.  Under INSTALLED SPOKES, select the spoke and then select the action.

        You can also select an action from the Core Actions.

    4.  Provide the details for the action.

    5.  Select **Done**.

    You've set up the flow.


**Parent Topic:**[Conditional and event-driven inbound integration](../concept/conditional-and-event-driven-inbound-integration.md)

