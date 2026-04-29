---
title: Activate an attended configuration record in RPA Hub
description: Activate an attended configuration record to enable the UI action that triggers the attended automation on the associated ServiceNow form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Embedded Task Automation \(ETA\), Use, RPA Hub, Workflow Data Fabric]
---

# Activate an attended configuration record in RPA Hub

Activate an attended configuration record to enable the UI action that triggers the attended automation on the associated ServiceNow form.

## Before you begin

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md).

Create an attended configuration record. For more information, see [Create an attended configuration record in RPA Hub](create-attended-config-rpa.md).

Verify that the attended configuration record is either in **Draft** state or **Inactive** state.

Verify that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process that is assigned to an Attended Configuration record.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Navigate to the Attended Configuration record either from the Attended Configuration menu list or from an attended bot process record's related list.

<table id="choicetable_uqv_q52_vzb"><thead><tr><th align="left" id="d660076e139">

Option

</th><th align="left" id="d660076e142">

Action

</th></tr></thead><tbody><tr><td id="d660076e148">

**From an Attended Configuration menu list**

</td><td>

1.  On the **Lists** tab, in **Build**, select **Attended Configurations**.
2.  Open an attended configuration record.


</td></tr><tr><td id="d660076e175">

**From an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process.
3.  On the Attended Configurations tab, select an attended configuration record.


</td></tr></tbody>
</table>4.  In the form header, select **Activate**.


## Result

The corresponding UI action is created on the ServiceNow form. On selecting this UI action, if there are any unsaved changes, the save confirmation dialog box is displayed. Otherwise, corresponding bot process \(automation\) is triggered. If the UI action isn’t visible, refer to the visibility conditions. For more information, see [Conditions for the visibility of UI action \(button\)](../reference/visibility-cond-button-rpa.md).

**Parent Topic:**[Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md)

**Related topics**  


[Deactivate an attended configuration record in RPA Hub](deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](delete-attended-config-rpa.md)

[Edit an attended configuration record in RPA Hub](edit-attended-config-rpa.md)

[Invoke Embedded Task Automation via API in RPA Hub](../concept/create-button-att-config-rpa.md)

[Conditions for the visibility of UI action \(button\)](../reference/visibility-cond-button-rpa.md)

