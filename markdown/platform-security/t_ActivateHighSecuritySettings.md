---
title: Activating High Security Settings
description: The High Security Settings plugin is active by default on all new instances. If it is not active on your instance, you can request the plugin.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [High Security Settings]
---

# Activating High Security Settings

The High Security Settings plugin is active by default on all new instances. If it is not active on your instance, you can request the plugin.

## Before you begin

Role required: None

Before [activating High Security Settings](t_ActivateHighSecuritySettings.md) on an existing instance:

1.  Review the following information to understand the new behavior:
    -   [Access Control List Rules](../../contextual-security/concept/access-control-rules.md)
    -   [High Security Settings](../concept/c_HighSecuritySettings.md)
    -   [Default deny property](../concept/c_DefaultDenyProperty.md)
2.  Enable the plugin on a non-production instance. A recent clone of production is preferable.
3.  Test the revised functionality, especially the added ACLs and default-deny functionality. Continue testing until the system performs as expected. If users cannot access expected resources, ensure they have appropriate roles and ACL rules to grant them the access.
4.  Create update sets of any needed changes so you can apply them to production.

**Note:** To learn more about this plugin, see [Enable High Security Plugin \[Updated in Security Center 1.3\]](../../security-center/reference/sc-high-security-plugin.md) in Instance Security Hardening Settings.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of the Application Manager interface with the Request plugin option highlighted.](../../../reuse/images/request-plugin.png)

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

    ![Admin view of the form requesting the Event Management plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Completed Activate Plugin form")

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


