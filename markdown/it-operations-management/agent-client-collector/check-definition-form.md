---
title: Agent Client Collector check definition page
description: The fields to be configured on the Check Definition page, when creating a check definition.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector check definition page

The fields to be configured on the Check Definition page, when creating a check definition.

<table id="table_ntn_dwf_vyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name for the check.

</td></tr><tr><td>

Check Type

</td><td>

Select the type of check. The available monitoring options are:-   Events
-   Metrics

</td></tr><tr><td>

Active

</td><td>

Select to activate the check.

</td></tr><tr><td>

Is Proxy Valid

</td><td>

Select to indicate that the check's policy is set to work as a proxy.When viewing this option in the check instance, it is read-only.

</td></tr><tr><td>

Command Auto Generation

</td><td>

Select to automatically generate the command with the **Command Prefix** value and the **Parameters** tab values.

</td></tr><tr><td>

Command Prefix

</td><td>

The command that is used for automatic generation when the **Command Auto Generation** check box is selected. The prefix consists of any portion of the command which is static \(does not change\), such as the script name.

</td></tr><tr><td>

Command

</td><td>

-   Enter the command that the Agent Client Collector executes.

**Note:** When the **Command Auto Generation** check box is selected, this field is automatically populated with the prefix and flags of the active parameters specified in the **Parameters** tab.

-   The field contains parameters taken from one or more of the following:

    -   Simple template: `{{.labels.params_field_name}}`: Takes values from entries in the **Parameters** tab. For example, a string of `{{.labels.params_warning}}` means that the value of the **warning** parameter is used \(provided it has been configured on the **Parameters** tab\).
    -   Monitored CI: `{{.labels.params_ci_field_name}}`: Takes values automatically from the monitored CI, where `field_name` is replaced with the exact name of the required field in the CI table.

</td></tr><tr><td>

Configuration Data Files

</td><td>

Select the configuration data files to be downloaded when the check runs.

</td></tr><tr><td>

Description

</td><td>

Description of the check.

</td></tr><tr><td>

Exec Mode

</td><td>

The execution mode of the check. Available options are:-   **shell**: To be used for checks which do not support **execv**.
-   **execv**: Provides enhanced security during check execution.

The default execution modes are:

-   Existing check definitions: **shell**
-   New check definitions: **execv**
-   If no value is entered in the field: **shell**

When upgrading to version 2.9.0, if this field is read-only, ensure that you disable the read-only status, as described in the \(KB1122498\) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Interval

</td><td>

The amount of time, in seconds, to wait between check executions.For example, a value of 60 means that the check runs every 60 seconds.

 Specified value must be an integer.

</td></tr><tr><td>

Timeout

</td><td>

The amount of time, in seconds, after which the check execution stops when no output is returned.For example, a value of 60 means that when the check execution doesn't return a value for 60 seconds, the execution stops.

</td></tr><tr><td>

Event status change threshold

</td><td>

The number of consecutive times that a check's response status must happen before a new event is sent.For example, if this value is set to 5, a check whose response status changes from **OK** to **Error** generates a new event with an **Error** status only after the fifth consecutive occurrence of the status change.

After an agent restart, an initial event is always sent.

Default value: 5 \(except for AWS event policies\)

</td></tr><tr><td>

Event status repair threshold

</td><td>

The number of consecutive times that a check's response status must improve to close the previous event.For example, if this value is set to 3, a check whose response status changes from **Error** to **OK** closes the previous event and generates a new event with an **OK** status only after the third consecutive occurrence of the status change.

Default value: 1 \(except for AWS event policies\)

</td></tr><tr><td>

Credential failure regex

</td><td>

The string from the check's output indicating that the check failed due to a credentials error. The agent then continues searching credentials that are part of the credential alias until it finds the correct one.This field is relevant \(and mandatory\) when the check's policy uses a credential alias. When creating a new check, enter the string manually.

</td></tr><tr><td>

Plugins

</td><td>

Select the plugins to be associated with the check. Once this is done, the plugins download before the check executes.

</td></tr></tbody>
</table>-   **[Check definition form parameters tab](check-definition-parameters-tab.md)**  
The Parameters tab definitions for the **Command** field on the check definition form.
-   **[Test check dialog box fields](test-check-dialog-box.md)**  
The dialog box fields when testing a check definition.

**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

