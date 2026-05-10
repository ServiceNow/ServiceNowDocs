---
title: Create a flow with an SLA Task trigger
description: Configure your Service Level Agreement \(SLA\) definition to run a flow as the action plan.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a flow with an SLA Task trigger

Configure your Service Level Agreement \(SLA\) definition to run a flow as the action plan.

## Before you begin

-   Role required: flow\_designer or admin

## About this task

An SLA Task trigger only runs when a task record matches the conditions of a Service Level Agreement \(SLA\) definition. For example, you can run a flow whenever an incident record matches the **Priority 1 resolution \(8 hour\)** SLA Definition.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **+ New** &gt; **New Flow**.

3.  On the form, fill in the fields.

<table id="table_kdg_zxh_ldb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify your flow. The system computes the internal name of the flow from the name.

</td></tr><tr><td>

Application

</td><td>

Application scope to create your flow in. Global is the default.

</td></tr><tr><td>

Description

</td><td>

Description of your flow.

</td></tr><tr><td>

Protection

</td><td>

Selection to specify if the flow is read-only. You can only select a value when you create the flow in an application scope that you own.

</td></tr><tr><td>

Run As

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 The system runs flow actions as the user who initiates the flow. Verify that all users who can trigger a flow have the necessary security access to run its actions. The initiating user also determines user-specific settings such as date/time formats.

 **Note:** Inbound email flows ignore this setting and always run as the user who initiates the session. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The system displays the Flow Designer page.

5.  Select **Select to add a Trigger** &gt; **Application** &gt; **SLA Task**.

6.  Add actions, subflows, and flow logic to the flow.

    Add [SLA Percentage Timer actions](../reference/sla-percentage-timer-action.md) to specify what to do when a task record attached to an SLA reaches specific percentages of completion.

7.  Test the flow.

    For more information, see [Test a flow](flow-test.md) and [Activate a flow](flow-activate.md).

    Once behaving as desired, activate the flow.

8.  [Create an SLA definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/t_CreateAnSLADefinition.md)

    1.  In the **Flow** field, select the SLA Task flow you previously created.

        **Note:** The **Flow** field only displays flows with an SLA Task trigger.

    2.  Click **Submit**.


## Result

When the SLA Definition conditions are true, the system runs the specified SLA task flow.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

