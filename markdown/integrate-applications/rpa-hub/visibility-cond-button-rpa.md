---
title: Visibility conditions of the UI action \(button\)
description: Ensure the following conditions are met to view the UI action \(button\) on the corresponding ServiceNow form, for the associated table that is selected in the Attended Configuration record. The visibility of the UI action is limited to classic environment.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Visibility conditions of the UI action \(button\)

Ensure the following conditions are met to view the UI action \(button\) on the corresponding ServiceNow form, for the associated table that is selected in the Attended Configuration record. The visibility of the UI action is limited to classic environment.

For other screens such as workspaces, playbook, the UI action must be created manually. For more information, see [Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md).

Familiarize yourself with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

<table id="table_ar4_w1b_5vb"><thead><tr><th>

Condition

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

The life cycle stage status of the associated bot process selected in the Attended Configuration record is **Published**.You cannot view the associated UI action on the ServiceNow form if the associated bot process is not available or is in **In Maintenance** state.

</td><td>

For more information, see [Bot Process form in RPA Hub](bot-process-form.md).

</td></tr><tr><td>

The **Enable Embedded Task Automation** check box must be selected in the associated attended bot process record.

</td><td>

For more information, see [Bot Process form in RPA Hub](bot-process-form.md).

</td></tr><tr><td>

The Attended Configuration record must be activated.

</td><td>

For more information, see [Activate an attended configuration record in RPA Hub](../task/activate-attend-config-rpa.md).

</td></tr><tr><td>

User must have the RPA Assisted user role.

</td><td>

For more information, see [Components installed with RPA Hub](installed-with-rpa-hub.md).

</td></tr><tr><td>

Robot record for that user must be available if the auto assignment system property **sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment** is false.

</td><td>

For more information about this system property, see [Configure RPA Hub properties](rpahub-sys-properties.md).

</td></tr><tr><td>

If the auto assignment system property **sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment** is true, you must have the license to create an attended robot.

</td><td>

For more information about this system property, see [Configure RPA Hub properties](rpahub-sys-properties.md).For more information about license, see [License distribution in RPA Hub](../concept/license-rpa-hub.md) and [Create a robot license distribution record in RPA Hub](../task/create-lua-record.md).

</td></tr><tr><td>

User must be associated to **Assigned Users/Groups** tab of the corresponding attended bot process selected in the Attended Configuration record.

</td><td>

For more information about license, see [Assign an attended user or group to an attended bot process](../task/assign-rda-users-botprocess.md).

</td></tr><tr><td>

Existing ServiceNow form record must match the conditions selected in attended configuration record.

</td><td>

For more information about creating an attended configuration record, see [Create an attended configuration record in RPA Hub](../task/create-attended-config-rpa.md).

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[List of steps for configuring embedded task automation](list-steps-eta-rpa.md)

