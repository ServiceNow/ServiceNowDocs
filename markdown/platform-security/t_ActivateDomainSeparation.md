---
title: Request domain separation
description: All domain support features are activated with a plugin called Domain Support - Domain Extensions Installer. Administrators can request activation of this plugin.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Request domain separation

All domain support features are activated with a plugin called **Domain Support - Domain Extensions Installer**. Administrators can request activation of this plugin.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the **com.glide.domain.msp\_extensions.installer** plugin activated on your organization's production and sub-production instances, generally within a few days.

If you do not have an account manager, decide to delay activation after purchase, or want to evaluate the product on a sub-production instance without charge, follow these steps.

Role required: admin

## About this task

If the Domain Support \(com.glide.domain\) plugin is already active, content in the Domain Support - Domain Extensions Installer and Domain Support - Domain Extensions plugins will not be installed to avoid potential conflict with an existing implementation.

Domain separation replaces Company Separation. Starting with the Helsinki release, the Company Separation plugin can no longer be activated. However, if company separation is already active when you activate domain separation, both plugins are active at the same time. You can control the company separation activation status with the **glide.db.separation.field** property.

**Note:** Domain paths are used for all customers on Helsinki and later. Domain numbering is no longer used. Customer Service and Support can assist in the upgrade.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

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

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


## Result

Activating the Domain Extension Installer plugin enables these features:

-   Domain separation is based on the Domain `[sys_domain]` table.
-   Delegated administration lets each domain have separate policy.
-   All records are part of the global domain.
-   The current user's domain determines the domain to use when viewing or operating on a record in a different domain.

**Related topics**  


[Domain separation plugin](../concept/domain-sep-plugin.md)

