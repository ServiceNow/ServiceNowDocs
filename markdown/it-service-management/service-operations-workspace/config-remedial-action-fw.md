---
title: Configure the Remedial Actions Framework
description: Configure the Remedial Actions Framework to add a new remedial action or modify an existing one.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the Remedial Actions Framework

Configure the Remedial Actions Framework to add a new remedial action or modify an existing one.

## Before you begin

Role required: sn\_reacf.sn\_remedial\_action\_admin

## Procedure

1.  Navigate to **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial Actions**.

    This table contains the list of the remedial actions available at the base system.

2.  Create a remedial action.

    1.  Select **New** to create a record.

        You can also select an existing action record to modify the action record.

    2.  On the Remedial Action form, fill in the fields.

<table id="table_ayf_sc4_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remedial action.

</td></tr><tr><td>

Action

</td><td>

Action that is performed. You must select a table name and a record in that table.**Note:** You must select the action table that is defined for the **Applicability** field of the Remedial Action Type record.

</td></tr><tr><td>

Type

</td><td>

Type of the remedial action or flow, such as CI action and standard change.

</td></tr><tr><td>

Description

</td><td>

Brief description of the remedial action.

</td></tr><tr><td>

Active

</td><td>

Option to activate the remedial action.

</td></tr><tr><td>

Target Table

</td><td>

Table for which the remedial action is applicable.

</td></tr><tr><td>

Match Target Extensions

</td><td>

Option to apply the remedial action to the child of the target table.

</td></tr><tr><td>

Target Conditions

</td><td>

Condition builder to configure the applicable remedial action for the target records.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  On the Remedial Action Parameters related list, add a parameter to the remedial action.

    The Remedial Action Parameters related list contains the list of parameters, such as **Process ID** and **Assigned to**, required to execute the remedial actions.

    1.  Select **New**.

    2.  On the Remedial Action Parameters form, fill in the fields.

<table id="table_ixc_h3c_dxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of parameter, such as integer, boolean, or reference.**Note:** If you select reference, you must also specify the reference table.

</td></tr><tr><td>

Label

</td><td>

Name of the parameter.

</td></tr><tr><td>

Mandatory

</td><td>

Option to mark the parameter as required.

</td></tr><tr><td>

Active

</td><td>

Option to activate the parameter.

</td></tr><tr><td>

Consider for concurrency check

</td><td>

Option to determine whether the parameter should be considered for the duplicate check of the remedial action.

</td></tr><tr><td class="sub-head" colspan="2">

Default Value

</td></tr><tr><td>

Default value

</td><td>

Default value of the parameter.**Note:** If this value isn’t defined, the default value that is specified in the CI Actions Framework tables is considered.

</td></tr><tr><td class="sub-head" colspan="2">

List specification

</td></tr><tr><td>

Choices

</td><td>

Type of list that must be applicable for the parameter.**Note:** This field is enabled only if the **Type** field is set to **Choice list**.

</td></tr></tbody>
</table>    3.  Select **Submit**.

4.  On the Remedial Action Roles related list, add a role.

    Remedial Action Roles contains the list of roles required to access and execute the remedial actions.

    1.  Select **New**.

    2.  Choose a **Role**.

    3.  Select **Submit**.

5.  On the User Criteria Action Inclusions related list, add a user criteria.

    The User Criteria Action Inclusion related list contains the list of user criteria that are permitted to execute the remedial action.

    1.  Select **New**.

    2.  Choose a **User Criteria**.

    3.  Select **Submit**.

6.  On the User Criteria Action Exclusions related list, add a user criteria.

    The User Criteria Action Exclusion related list contains the list of user criteria that aren’t permitted to execute the remedial action.

    1.  Select **New**.

    2.  Choose a **User Criteria**.

    3.  Select **Submit**.

7.  Navigate to **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial Action Types**.

    This table contains the list of remedial action types, such as CI action and standard change.

8.  Create a remedial action type.

    1.  Select **New**.

    2.  On the Remedial Action Type form, fill in the fields.

<table id="table_qbn_vm5_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remedial action type.

</td></tr><tr><td>

Applicability

</td><td>

List of Action tables where the remedial action type is applicable.

</td></tr><tr><td>

Processor

</td><td>

Script include that is used for the implementation of the extension point **RemedialActionProvider** to execute the remedial action.

</td></tr><tr><td>

Allow concurrent execution

</td><td>

Option to allow duplicate concurrent execution of remedial actions.**Note:** If the **Consider for concurrency check** option is set to false for all the parameters, then the duplicate actions are allowed by default.

</td></tr></tbody>
</table>    3.  Select **Submit**.

9.  Navigate to **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial Action Origin**.

    This table contains the list of applications where you can use the Remedial Actions Framework.

10. Add an application.

    1.  Select **New**.

    2.  Add the name of an application that you want to use for the Remedial Actions Framework.

    3.  Select **Submit**.


## What to do next

When a Remedial Action Type is created, you must create an implementation or do the necessary changes in the existing implementation of the **RemedialActionProvider** scripted extension point. To view and use the new or modified remedial actions, you must configure the Investigate UI to display the remedial actions. For more information, see [Customize the Investigate tab](../concept/customize-the-incident-record-page.md#).

**Parent Topic:**[Setting up Investigation Framework in Service Operations Workspace](../concept/set-up-investigate.md)

