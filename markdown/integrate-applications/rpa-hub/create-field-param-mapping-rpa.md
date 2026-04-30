---
title: Map a table field to a bot process field parameter in RPA Hub
description: Map form fields of the associated attended configuration table \(Table field\) to the process field parameters used in the automations. For example, if "First name" is the process field parameter used in the automation, then it’s mapped to the form's 'requested\_for.first\_name' field.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Create an attended configuration record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Map a table field to a bot process field parameter in RPA Hub

Map form fields of the associated attended configuration table \(**Table** field\) to the process field parameters used in the automations. For example, if "`First name`" is the process field parameter used in the automation, then it’s mapped to the form's '`requested_for.first_name`' field.

## Before you begin

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

Verify that you’ve completed the tasks that are related to configuring the Embedded Task Automation in RPA Hub. For more information, see [List of steps for configuring embedded task automation](../reference/list-steps-eta-rpa.md).

Create an attended bot process. For more information about creating an attended bot process, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Verify that the **Enable Embedded Task Automation** check box is selected in the associated attended bot process form. For more information about the bot process form, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Create an attended configuration record. For more information, see [Create an attended configuration record in RPA Hub](create-attended-config-rpa.md).

Create process field parameters that are used in the automations.

-   For more information about creating process field parameters from a bot process, see [Create a process field parameter in RPA Hub](create-process-field-param-rpa.md).
-   You can create a process field parameter by performing step 7 of this task. Verify that the associated bot process isn’t published. Also verify that the associated attended configuration record is either in **Draft** or **Inactive** state.

Verify that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process that is assigned to an Attended Configuration record. Verify that the Attended Configuration record that is assigned to the given field parameter mapping, must be either in **Inactive** or **Draft** state.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

Field parameter mapping enables an easy data flow during the execution of a bot process.

You can’t map the same process field parameter with multiple fields. A process field parameter, for example, Name, can't be mapped with more than one field, for example, First name and Last name.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Map a field parameter from either the Attended Configuration menu list or from an attended bot process record's related list.

<table id="choicetable_uqv_q52_vzb"><thead><tr><th align="left" id="d125848e204">

Option

</th><th align="left" id="d125848e207">

Action

</th></tr></thead><tbody><tr><td id="d125848e213">

**Map a field parameter from an Attended Configuration menu list**

</td><td>

1.  On the **Lists** tab, in **Build**, select **Attended Configurations**.
2.  Open an attended configuration record.


</td></tr><tr><td id="d125848e240">

**Map a field parameter from an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process.
3.  On the Attended Configurations tab, select an attended configuration record.


</td></tr></tbody>
</table>4.  On the **Field Parameter Mappings** tab, select **New**.

5.  On the Field and parameter mapping dialog box, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

\[Auto-generated\] Associated attended configuration table.

</td></tr><tr><td>

Process Field Parameter

</td><td>

Select a process field parameter to set or get the value of a field from the particular ServiceNow form.For example, if you select 'BadgeID' in the **Process Field Parameter** field, select '`Badge Id`' in the **Field**. To set the value in the "Badge Id" field of the request table, you can update the value of the "BadgeID" process field parameter.

![Field parameter mapping.](../image/field-param-mapping.png)

Process field parameters that are already mapped to the fields are unavailable for mapping.

</td></tr><tr><td>

Field

</td><td>

Select a form field to map with a process field parameter.

</td></tr></tbody>
</table>6.  Perform any of the following tasks to save the mapping.

<table id="choicetable_z1v_dzc_lzb"><thead><tr><th align="left" id="d125848e378">

Option

</th><th align="left" id="d125848e381">

Action

</th></tr></thead><tbody><tr><td id="d125848e387">

**Only save the mapping**

</td><td>

Select **Save**.

</td></tr><tr><td id="d125848e399">

**Save the mapping and map another field parameter**

</td><td>

Select **Save &amp; map next**.Repeat step 5 to map another field to another process field parameter.

</td></tr></tbody>
</table>7.  To create a process field parameter that can be used in the automation, perform the following steps:

    1.  On the **Field Parameter Mappings** tab, select **Create parameter**.

    2.  On the create a parameter dialog box, fill in the fields.

<table id="table_ofd_wbf_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the form process field parameter.Process field parameters are used for setting the value or getting the value of a field on a particular form.

</td></tr><tr><td>

Description

</td><td>

Brief description of the process field parameter.

</td></tr></tbody>
</table>    3.  Select **Create**.

    4.  Refer to step 5 to map this process field parameter to the form field.

    5.  Select **Save**.

8.  Repeat steps 5 and 6 to map more field parameters.


## What to do next

Activate an attended configuration record. For more information, see [Activate an attended configuration record in RPA Hub](activate-attend-config-rpa.md).

**Related topics**  


[Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md)

[Deactivate an attended configuration record in RPA Hub](deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](delete-attended-config-rpa.md)

[Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md)

[Visibility conditions of the UI action \(button\)](../reference/visibility-cond-button-rpa.md)

