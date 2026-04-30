---
title: List of steps for configuring embedded task automation
description: Use this list of steps to guide you through all the tasks for configuring an embedded task automation.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Embedded Task Automation in RPA Hub, Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# List of steps for configuring embedded task automation

Use this list of steps to guide you through all the tasks for configuring an embedded task automation.

Complete all the tasks for a step before moving on to the next step.

Do the steps in the order that they’re presented.

<table id="table_ar4_w1b_5vb"><thead><tr><th>

Task

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

1\) Familiarize yourself with Embedded Task Automation concepts.

</td><td>

For more information, see [Embedded Task Automation in RPA Hub](../concept/embedded-task-auto-rpa.md).

</td></tr><tr><td>

2\) Build an automation by using the new components in RPA Desktop Design Studio and publish it to the ServiceNow instance.

</td><td>

For more information about the new components, see [Forms](../../rpa-studio/concept/forms_sn_rpa_studio.md).

 For more information about publishing the automation RPA Desktop Design Studio, see [Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md).

</td></tr><tr><td>

3\) Create an attended bot process. Associate it with the package that is published in step 2.

</td><td>

For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

</td></tr><tr><td>

4\) Select the **Enable Embedded Task Automation** check box in the associated attended bot process form.On enabling this check box, two additional tabs, **Process Field Parameters** and **Attended Configuration**, are available on the bot process form.

</td><td>

For more information, see [Bot Process form in RPA Hub](bot-process-form.md).

</td></tr><tr><td>

5\) On the Process Field Parameters tab, create dynamic parameters that are used in the automation.

</td><td>

For more information, see [Create a process field parameter in RPA Hub](../task/create-process-field-param-rpa.md).

</td></tr><tr><td>

6\) Create an attended configuration record.

</td><td>

For more information, see [Create an attended configuration record in RPA Hub](../task/create-attended-config-rpa.md).

</td></tr><tr><td>

7\) On the Field Parameter Mappings tab, map the form fields to the process field parameters that are used in the automations.

</td><td>

For more information, see [Map a table field to a bot process field parameter in RPA Hub](../task/create-field-param-mapping-rpa.md).

</td></tr><tr><td>

8\) Activate an attended configuration record to enable the UI action that triggers the attended automation on the associated ServiceNow form.

</td><td>

For more information, see [Activate an attended configuration record in RPA Hub](../task/activate-attend-config-rpa.md).

</td></tr><tr><td>

9\) To trigger a bot process \(automation\) from a Workspace, a playbook, or any other service portal, you can create corresponding actions and call the RPAInstanceFormHooks Application Programming Interface \(API\).

</td><td>

For more information, see [Invoke Embedded Task Automation via API](../concept/create-button-att-config-rpa.md).

</td></tr><tr><td>

10\) To publish the bot process, assign the user with RPA AU \(RPA assisted user\) in the **Assigned User** or **Assigned Group** field in the Attended Users/Groups tab of the attended bot process record. If the auto assignment system property **sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment** is false, the attended robot record is available for the assigned RPA Assisted User.

If the auto assignment system property is true, an attended robot license is available to auto create an attended robot at the time of triggering.

</td><td>

For more information about assigning the user with RPA AU, see [Assign an attended user or group to an attended bot process](../task/assign-rda-users-botprocess.md).

 For more information about this system property, see [Configure RPA Hub properties](rpahub-sys-properties.md).

</td></tr><tr><td>

11\) Publish the bot process with the corresponding package published from the RPA Desktop Design Studio.

</td><td>

For more information, see [Publish an RPA Hub bot process](../task/publish-bot-process.md).

</td></tr><tr><td>

12\) The assigned user can view the UI action \(button\) on the corresponding ServiceNow form. Using this button, the user can trigger the attended bot process \(attended automation\). There are certain conditions to view this button \(UI action\).

</td><td>

For more information about the visibility conditions, see [Visibility conditions of the UI action \(button\)](visibility-cond-button-rpa.md).

</td></tr></tbody>
</table>