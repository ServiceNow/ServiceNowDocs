---
title: Deactivate an attended configuration record in RPA Hub
description: Deactivate an attended configuration to move the record to inactive state.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Deactivate an attended configuration record in RPA Hub

Deactivate an attended configuration to move the record to inactive state.

## Before you begin

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

Create an attended configuration record. For more information, see [Create an attended configuration record in RPA Hub](create-attended-config-rpa.md).

Ensure that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process that is assigned to an Attended Configuration record.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

Deactivating an attended configuration record moves the state from **Active** to **Inactive**, opens the form for editing, and the configuration disconnects from the associated ServiceNow form. The created UI action on the associated ServiceNow form will not be visible.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Navigate to the Attended Configuration record either from the Attended Configuration menu list or from an attended bot process record's related list.

<table id="choicetable_uqv_q52_vzb"><thead><tr><th align="left" id="d96104e134">

Option

</th><th align="left" id="d96104e137">

Action

</th></tr></thead><tbody><tr><td id="d96104e143">

**From an Attended Configuration menu list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Attended Configurations**.
2.  Open an attended configuration record.


</td></tr><tr><td id="d96104e170">

**From an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process.
3.  On the Attended Configurations tab, select an attended configuration record.


</td></tr></tbody>
</table>4.  In the form header, select **Deactivate**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Activate an attended configuration record in RPA Hub](activate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](delete-attended-config-rpa.md)

[Edit an attended configuration record in RPA Hub](edit-attended-config-rpa.md)

[Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md)

[Visibility conditions of the UI action \(button\)](../reference/visibility-cond-button-rpa.md)

