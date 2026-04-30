---
title: Create an attended configuration record in RPA Hub
description: Create an attended configuration record in RPA Hub to trigger an attended bot process that is enabled with embedded task automation.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Create an attended configuration record in RPA Hub

Create an attended configuration record in RPA Hub to trigger an attended bot process that is enabled with embedded task automation.

## Before you begin

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

Verify that you’ve completed the tasks that are related to configuring the Embedded Task Automation in RPA Hub. For more information, see [List of steps for configuring embedded task automation](../reference/list-steps-eta-rpa.md).

Create an attended bot process. For more information about creating an attended bot process, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Verify that the **Enable Embedded Task Automation** check box is selected in the associated attended bot process form. For more information about the bot process form, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Verify that the Robotic Process Automation \(RPA\) developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Create an attended configuration record from either the menu list or from an attended bot process record's related list.

<table id="choicetable_fr4_mn2_vzb"><thead><tr><th align="left" id="d376324e149">

Option

</th><th align="left" id="d376324e152">

Action

</th></tr></thead><tbody><tr><td id="d376324e158">

**Create an attended configuration record from the menu list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Attended Configurations**.
2.  Select **New**.


</td></tr><tr><td id="d376324e188">

**Create an attended configuration record from an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process that you want to create and associate an attended configuration to.
3.  On the Attended Configurations tab, select **New**.


</td></tr></tbody>
</table>4.  On the Attended Configuration form, fill in the fields.

    For more information, see [Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md).

5.  Select **Save**.


**Related topics**  


[Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md)

[Activate an attended configuration record in RPA Hub](activate-attend-config-rpa.md)

[Deactivate an attended configuration record in RPA Hub](deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](delete-attended-config-rpa.md)

[Create a process field parameter in RPA Hub](create-process-field-param-rpa.md)

[Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md)

[Visibility conditions of the UI action \(button\)](../reference/visibility-cond-button-rpa.md)

