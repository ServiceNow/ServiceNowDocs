---
title: Create a process field parameter in RPA Hub
description: Define process field parameters \(dynamic parameters\) that are required in the automation \(bot process\).
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Create a process field parameter in RPA Hub

Define process field parameters \(dynamic parameters\) that are required in the automation \(bot process\).

## Before you begin

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

Verify that you’ve completed the tasks that are related to configuring the Embedded Task Automation in RPA Hub. For more information, see [List of steps for configuring embedded task automation](../reference/list-steps-eta-rpa.md).

Create an attended bot process. For more information about creating an attended bot process, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Verify that the **Enable Embedded Task Automation** check box is selected in the associated attended bot process form. For more information about the bot process form, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

**Important:** After selecting the **Enable Embedded Task Automation** check box, if the **Process Field Parameters** tab isn’t displayed on the bot process, then it’s possible that your related lists are customized. Add the related list manually.

Verify that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

Process field parameters are used for setting the value or getting the value of a field on a particular form.

You can create a process field parameter in two ways. Perform this task to create it from a bot process.

Otherwise, create it while mapping the field parameters by selecting the **Create parameter** button from the **Field Parameter Mappings** tab. For more information, see [Map a table field to a bot process field parameter in RPA Hub](create-field-param-mapping-rpa.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open an attended bot process that you want to create and associate a process field parameter to.

5.  On the **Process Field Parameters** tab, select **New**.

6.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the process field parameter for the associated bot process.For example, Location, First Name, Title

</td></tr><tr><td>

Description

</td><td>

Brief description of the parameter.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  To delete a process field parameter record, select the record and then select **Delete**.

    **Note:** If a parameter is mapped in the attended configuration record, then you must delete the mapping to delete the parameter. You can’t delete a parameter, if the associated bot process is published.


**Related topics**  


[Create an attended configuration record in RPA Hub](create-attended-config-rpa.md)

[Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md)

[Deactivate an attended configuration record in RPA Hub](deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](delete-attended-config-rpa.md)

[Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md)

[Visibility conditions of the UI action \(button\)](../reference/visibility-cond-button-rpa.md)

