---
title: Activate flow reporting
description: Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. Specify the level of detail the execution details contain.Generate execution details for an individual flow, subflow, or action every time it runs, not just during testing.Generate execution details for all items that Workflow Studio runs rather than just generating execution details during testing.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Flow administration, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Activate flow reporting

Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. Specify the level of detail the execution details contain.

**Parent Topic:**[Flow administration](../concept/flow-administration.md)

## Activate reporting for an individual flow, subflow, or action

Generate execution details for an individual flow, subflow, or action every time it runs, not just during testing.

### Before you begin

Role required: flow\_operator or admin

### About this task

**Warning:** To avoid performance issues on your production instance, activate and configure reporting on the non-production instance that you use for testing.

You can activate reporting for an individual flow, subflow, or action by creating a record on the Settings \[sys\_flow\_execution\_setting\] table. Each Settings record specifies the flow, subflow, or action to generate execution details for and the level of detail to use. You can create as many Settings records as you want. The system generates execution details each time the flow, subflow, or action is directly run. Actions or subflows that run from a parent flow use the Settings record of the parent flow.

**Note:** You can call actions and subflows directly using the action API or script API.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Administration** &gt; **Settings**.

    The system displays the list of individual items for which flow reporting is activated.

2.  In the **Flow/SubFlow/Action** field, select the lookup icon \(![](../images/lookup-using-list-icon.png)\) to select the type item for which you want to activate reporting.

    The system displays a dialog box to select the type and specific instance.

3.  In the **Table name** field, select the matching table for the item.

    |Option|Description|
    |------|-----------|
    |**Flow**|Table for flows and subflows|
    |**Action Type**|Table used for actions|

4.  In the **Document** field, select the lookup icon \(![](../images/lookup-using-list-icon.png)\).

    The system displays a list of items of the matching type.

5.  Select the individual flow, subflow, or action for which you want to activate reporting.

6.  Select **OK** to close the dialog box.

7.  In the **Reporting** field, select the level of runtime data to generate and display in flow execution details.

    -   **Off**

        The system doesn't generate flow execution details. The system only generates execution details when you run a test.

        **Note:** Testing an action or flow generates execution details at the Trace level.

    -   **Basic: Runtime states and durations only**

        The system generates runtime execution details for each flow, subflow, and action run. You can see the runtime state and duration for these basic items. You can also see configuration and runtime values for flow triggers, subflow inputs, and subflow outputs.

    -   **Full: Action configuration and runtime values \(for debugging only\)**

        The system generates configuration and runtime execution details for each flow, subflow, and action run. You can see the runtime state, duration, input values, and output values for all items. For custom actions, you can also see the runtime state, duration, input values, and output values of its steps. You can also see the configuration values for flow triggers, subflows, actions, and steps that are part of a custom action.

        **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration.

    -   **Trace: All values \(for testing and Support only\)**

        The system generates configuration and runtime execution details for each flow, subflow, action, and step run. You can see the runtime state, duration, input values, and output values for all items. You can also see the configuration values for flow triggers, subflows, actions, and steps.

        **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration. Testing an action or flow generates execution details at the Trace level.

8.  Select **Submit**.

    For example, this setting enables the full reporting level and warning log level for the Acknowledge Alert flow. ![Flow reporting setting for the Acknowledge Alert flow](../images/example-flow-reporting-setting.png)


### Result

Workflow Studio generates execution details for the individual flow, subflow, or action.

## Activate reporting for all items

Generate execution details for all items that Workflow Studio runs rather than just generating execution details during testing.

### Before you begin

Role required: flow\_designer, action\_designer, admin

### About this task

**Important:** To avoid performance issues on your production instance, activate and configure reporting on the non-production instance that you use for testing.

By default, the system only generates execution details when you run a test. You can activate reporting for all items that Workflow Studio runs by setting the **com.snc.process\_flow.reporting.level** system property.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Administration** &gt; **Properties**.

2.  Set the property **Level of reporting data generated by the flow engine**.

    -   **Off**

        The system doesn't generate flow execution details. The system only generates execution details when you run a test.

        **Note:** Testing an action or flow generates execution details at the Trace level.

    -   **Basic: Runtime states and durations only**

        The system generates runtime execution details for each flow, subflow, and action run. You can see the runtime state and duration for these basic items. You can also see configuration and runtime values for flow triggers, subflow inputs, and subflow outputs.

    -   **Full: Action configuration and runtime values \(for debugging only\)**

        The system generates configuration and runtime execution details for each flow, subflow, and action run. You can see the runtime state, duration, input values, and output values for all items. For custom actions, you can also see the runtime state, duration, input values, and output values of its steps. You can also see the configuration values for flow triggers, subflows, actions, and steps that are part of a custom action.

        **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration.

    -   **Trace: All values \(for testing and Support only\)**

        The system generates configuration and runtime execution details for each flow, subflow, action, and step run. You can see the runtime state, duration, input values, and output values for all items. You can also see the configuration values for flow triggers, subflows, actions, and steps.

        **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration. Testing an action or flow generates execution details at the Trace level.

    **Warning:** Avoid enabling the Full reporting option on a production instance. Full reporting generates execution details for every flow and action run on the instance. Creating and storing these execution details consumes system memory and can lower system performance. Instead, only enable reporting for specific flows and actions or test them on a non-production instance.

3.  Select **Save**.


### Result

Workflow Studio generates execution details for all items you specified in the system property.

