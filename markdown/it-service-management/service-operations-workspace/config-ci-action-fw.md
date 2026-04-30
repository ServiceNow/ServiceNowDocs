---
title: Configure CI Actions
description: Configure the CI Action Framework to add a new CI action or modify an existing one.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Setting up Investigation Framework in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure CI Actions

Configure the CI Action Framework to add a new CI action or modify an existing one.

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Navigate to **All** &gt; **Metrics and CI Actions Framework** &gt; **Administration** &gt; **Actions**.

    This table contains the list of all CI actions.

2.  Create a CI Action.

    1.  Select **New** to create a record.

        You can also select an existing action record to modify the record.

    2.  On the Action form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the CI action.|
        |CI Class|CI class for which the CI action is applicable, such as computer \[cmdb\_ci\_computer\].|
        |Active|Option to activate the CI action.|
        |Description|Brief description of the CI action.|

    3.  Select **Submit**.

3.  On the Action Role related list, add a role.

    The Action Role related list contains the list of roles required to access and execute the CI actions.

    1.  Select **New**.

    2.  Choose a **Role**.

    3.  Select **Submit**.

4.  On the User Criteria Action Inclusion related list, add a user criteria.

    The User Criteria Action Inclusion related list contains the list of user criteria that are allowed to execute the CI action.

    1.  Select **New**.

    2.  Choose a **User Criteria**.

    3.  Select **Submit**.

5.  On the User Criteria Action Exclusion related list, add a user criteria.

    The User Criteria Action Exclusion related list contains the list of user criteria that aren’t permitted to execute the CI action.

    1.  Select **New**.

    2.  Choose a **User Criteria**.

    3.  Select **Submit**.

6.  On the Action Configuration related list, create a record.

    The Action Configuration related list contains a list of action configurations applicable to CI. You can create multiple configurations for a CI action based on different providers or CI class.

    1.  Select **New** to create a record.

        You can also select an existing action record to modify the action configuration record.

    2.  On the Action Configuration form, fill in the fields.

<table id="table_sfz_jt1_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the action configuration for the CI action.

</td></tr><tr><td>

Provider

</td><td>

Provider for which you want to create the action configuration.

</td></tr><tr><td>

CI Class

</td><td>

CI class applicable to the action configuration.

</td></tr><tr><td>

Allow matching CI Class extension

</td><td>

Option to apply the configuration to the child of CI class, such as device or server.

</td></tr><tr><td>

CI Condition

</td><td>

Condition builder to configure the CIs where the action configuration is applicable.

</td></tr><tr><td>

Action Type

</td><td>

Action type that is used to execute the CI action. It can be a flow or a script.

</td></tr><tr><td>

Action execution flow

</td><td>

A flow that is used to execute the CI action.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the configuration is applicable in case there are multiple configurations available for a CI action.**Note:** The first applicable adapter configuration that is based on the **Order** value is only considered for executing the CI action.

</td></tr><tr><td>

Duplicate request time limit \(seconds\)

</td><td>

Sets the number of seconds to prevent the execution of duplicate action requests when one with the same parameters is already in progress.

</td></tr></tbody>
</table>    3.  Select **Submit**.

7.  On the Action Configuration Step related list, create or modify a record.

    The Action Configuration Step related list contains the list of steps applicable for the action configuration.

    1.  Select **New** to create a record.

        You can also select an existing record to modify the steps record.

        A list of provider-specific action configuration table is displayed, such as Agent Client Collector \(ACC\) Action Configuration and Microsoft Endpoint Configuration Manager \(MECM\) Action Configuration.

    2.  Select the provider for which you want to create an adapter configuration.

        For example, ACC Action Configuration for Agent Client Collector for Investigation.

    3.  On the Action configuration step form, fill in the fields.

<table id="table_iqz_fz1_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the step that you want to create for the action configuration.

</td></tr><tr><td>

Active

</td><td>

Option to activate the action configuration step.

</td></tr><tr><td>

Sequence

</td><td>

Step sequence that is executed if multiple steps exist for an action configuration record.

</td></tr><tr><td>

Check definition

</td><td>

Check definition that is used for the execution and handling the output of the command. For example, remedial-action.**Note:** This is applicable only if the provider is Agent Client Collector for Investigation.

</td></tr><tr><td>

Command

</td><td>

Command that is executed.**Note:** This field is applicable only if the provider is Agent Client Collector for Investigation.

</td></tr><tr><td>

Action Input

</td><td>

Input parameters required by flow action.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Flow Action

</td><td>

MECM spoke flow action to perform the write operation on the MECM device.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Output Flow Action

</td><td>

MECM spoke flow action to look up the write operation response from the MECM server.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Validate

</td><td>

Option to validate the command.

</td></tr><tr><td>

Validation script

</td><td>

Script that is run to check if the command has a valid execution and output. **Note:** This field is visible only if the **Validate** option is selected.

</td></tr><tr><td>

Run

</td><td>

Values for how and when the command must be validated. You can select the following values:-   Once: Validation must be run once.
-   Poll: Validation must be run more than once.
**Note:** This field is visible only if the **Validate** option is selected.

</td></tr><tr><td>

Polling count

</td><td>

Maximum number of times the validation is run for the command.**Note:** This field is visible only if **Run** field is set to **Poll**.

</td></tr><tr><td>

Polling interval

</td><td>

Time interval in which the validation must be rerun for the command execution.**Note:** This field is visible only if **Run** field is set to **Poll**.

</td></tr></tbody>
</table>8.  On the Action Parameter related list, create a record.

    The Action Parameter related list contains the list of parameters required to execute the CI action.

    1.  Select **New** to create a record.

        You can also select an existing record to modify the parameter record.

    2.  On the Action Parameter form, fill in the fields.

<table id="table_iph_qv1_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of the parameter, such as integer or reference.**Note:** If you select reference, you must also specify the reference table.

</td></tr><tr><td>

Label

</td><td>

Name of the parameter.

</td></tr><tr><td>

Mandatory

</td><td>

Option to mark the applicability of the parameter as required.

</td></tr><tr><td>

Active

</td><td>

Option to activate the action parameter.

</td></tr><tr><td class="sub-head" colspan="2">

Default value

</td></tr><tr><td>

Default value

</td><td>

Default value of the parameter.

</td></tr><tr><td class="sub-head" colspan="2">

Choice list specification

</td></tr><tr><td>

Choices

</td><td>

Type of choice list that must be applicable for the parameter.**Note:** This field is enabled only if the **Type** field is set to **Choice list**.

</td></tr></tbody>
</table>    3.  Select **Submit**.


## What to do next

You must configure the Remedial Actions Framework. For more information, see [Configure the Remedial Actions Framework](config-remedial-action-fw.md).

**Parent Topic:**[Setting up Investigation Framework in Service Operations Workspace](../concept/set-up-investigate.md)

