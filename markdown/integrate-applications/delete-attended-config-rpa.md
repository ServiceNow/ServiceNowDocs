---
title: Delete an attended configuration record in RPA Hub
description: Delete an attended configuration record that you no longer need.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Embedded Task Automation \(ETA\), Use, RPA Hub, Workflow Data Fabric]
---

# Delete an attended configuration record in RPA Hub

Delete an attended configuration record that you no longer need.

## Before you begin

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md).

Create an attended configuration record. For more information, see [Create an attended configuration record in RPA Hub](create-attended-config-rpa.md).

Ensure that the attended configuration record is either in **Draft** state or **Inactive** state.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

If you delete an attended configuration record, the associated mapping records and the UI Actions \(if any\) that are created for the ServiceNow form upon activation are also deleted. The created UI action on the associated ServiceNow form will not be visible.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Navigate to the Attended Configuration record either from the Attended Configuration menu list or from an attended bot process record's related list.

<table id="choicetable_uqv_q52_vzb"><thead><tr><th align="left" id="d580285e140">

Option

</th><th align="left" id="d580285e143">

Action

</th></tr></thead><tbody><tr><td id="d580285e149">

**From an Attended Configuration menu list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Attended Configurations**.
2.  Open an attended configuration record.


</td></tr><tr><td id="d580285e176">

**From an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process.
3.  On the Attended Configurations tab, select an attended configuration record.


</td></tr></tbody>
</table>4.  In the form header, select **Delete**.


**Parent Topic:**[Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md)

**Related topics**  


[Activate an attended configuration record in RPA Hub](activate-attend-config-rpa.md)

[Deactivate an attended configuration record in RPA Hub](deactivate-attend-config-rpa.md)

[Edit an attended configuration record in RPA Hub](edit-attended-config-rpa.md)

[Invoke Embedded Task Automation via API in RPA Hub](../concept/create-button-att-config-rpa.md)

[Conditions for the visibility of UI action \(button\)](../reference/visibility-cond-button-rpa.md)

