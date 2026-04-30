---
title: Create an interaction wrap up configuration
description: Create a configuration for each type of interaction that uses the interaction wrap up feature.
locale: en-US
release: xanadu
product: Interaction Management
classification: interaction-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Interaction wrap up, Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an interaction wrap up configuration

Create a configuration for each type of interaction that uses the interaction wrap up feature.

## Before you begin

Role required: admin

## About this task

Creating a configuration automatically enables the interaction wrap up feature and adds the Wrap Up state for interactions that match the configuration settings.

The **Interaction** &gt; **Wrap Up** module includes a list of wrap up configuration records. These configurations are stored in the Interaction Wrap Up Configuration \(interaction\_wrap\_up\_configuration\) table.

## Procedure

1.  Navigate to **Interaction** &gt; **Wrap Up**.

2.  Click **New**.

3.  Fill in the fields on the Interaction Wrap Up Configuration form.

<table id="table_e4r_dtz_z4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the interaction wrap up configuration.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the configuration is active. The default value is true.

</td></tr><tr><td>

Table

</td><td>

Read only. The table that stores the interaction records to which this configuration applies.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions that apply to the interaction records included in this configuration.

</td></tr><tr><td>

Enforce wrap up duration

</td><td>

Enables the system to automatically end the wrap up period. The default value is false.

 If enabled, the system automatically ends the wrap up period at the end of the wrap up duration \(set in the **Duration in seconds** field\) and moves the state of the interaction record from Wrap Up to Closed Complete.

</td></tr><tr><td>

Duration in seconds

</td><td>

The duration of the wrap up period. -   The default value is 60 seconds.
-   The value must be greater than 0.
The system displays this field when you enable the **Enforce wrap up duration** field.

</td></tr><tr><td>

Show duration to agent

</td><td>

Enables a duration countdown timer for the agent. The default value is false. The system displays this field when you enable the **Enforce wrap up duration** field.

**Note:** The interaction wrap up timer works in both CSM Configurable Workspace and CSM Agent Workspace but the timer display is only available in CSM Configurable Workspace.

</td></tr><tr><td>

Order

</td><td>

The order of the configuration, which is used in evaluation processing of wrap up configuration records. If there are multiple records, the lower order number takes precedence over higher numbers. The default value is 100.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Interaction wrap up](../concept/interaction-wrap-up-state.md)

