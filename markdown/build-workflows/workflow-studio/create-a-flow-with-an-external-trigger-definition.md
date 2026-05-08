---
title: Create a flow with an external trigger
description: Set up a flow with a base system external trigger definition. The flow responds to an event-driven external trigger from a third-party system. For example, run a flow when an issue is created in a third-party issue-tracking system.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a flow with an external trigger

Set up a flow with a base system external trigger definition. The flow responds to an event-driven external trigger from a third-party system. For example, run a flow when an issue is created in a third-party issue-tracking system.

## Before you begin

Role required: flow\_designer or admin

Subscription required: This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Ensure that you've configured the external trigger endpoints for the third-party application spoke. For more information about configuring the third-party spoke, see Set up external trigger endpoints.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Create New** &gt; **Flow**.

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

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see OAuth 2.0 credentials.

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

    If you have a saved external trigger, the trigger is displayed under the installed third-party spoke for you to use. You can add additional conditions as required. See [Create a saved external trigger](../../flow-designer/task/create-saved-external-trigger.md).

    1.  Under the TRIGGER section, select **Add a trigger**.

    2.  Under the INSTALLED SPOKES heading, select a spoke from the Trigger list.![Select spoke.](../images/select-spoke.png)

    3.  Select the predefined external trigger definition.![External trigger definition.](../images/select-external-trigger-definition.png)

        To learn more about external trigger definitions, see Conditional and event-driven inbound integration.

    4.  To define the conditions for the flow to execute, in the Condition 1 field, drag the appropriate data pill and enter the value.

    5.  Select **Done**.

        You've set up the trigger.

6.  Add actions, subflows, and flow logic to the flow.

7.  Test the flow.

8.  Activate the flow.

    Activate the flow if the test returns the desired outcome. For more information on testing and activating your flow, see [Test a flow](../../flow-designer/task/flow-test.md) and [Activate a flow](../../flow-designer/task/flow-activate.md).


**Parent Topic:**[Create a flow in Workflow Studio](../../flow-designer/task/create-flow.md)

