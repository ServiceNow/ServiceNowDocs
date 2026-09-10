---
title: Activate flow reporting
description: Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. Specify the level of detail the execution details contain.Generate execution details for an individual flow, subflow, or action every time it runs, not just during testing.Generate execution details for all items that Workflow Studio runs rather than just generating execution details during testing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/enable-flow-reporting.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow administration, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Activate flow reporting

Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. Specify the level of detail the execution details contain.

**Parent Topic:**[Flow administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-administration.md)

## Activate reporting for an individual flow, subflow, or action

Generate execution details for an individual flow, subflow, or action every time it runs, not just during testing.

### Before you begin

Role required: flow\_operator or admin

**Warning:** To avoid performance issues on your production instance, activate and configure reporting on the non-production instance that you use for testing.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Depending on whether you want to activate reporting for a flow, subflow, or an action, select Flows, Subfows, or Actions on the header.

3.  Open the flow, subflow, or the action for which you want to activate reporting.

4.  If you want to enable reporting for a flow or a subflow, select Edit flow or Edit subflow.

5.  From the More actions menu \[Omitted image "more-actions-menu-icon.png"\] Alt text: The More Actions icon, select the reporting settings.

6.  From the **Reporting Level** list, select the level of runtime data to generate and display in flow execution details.

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

7.  Select **Update**.


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

