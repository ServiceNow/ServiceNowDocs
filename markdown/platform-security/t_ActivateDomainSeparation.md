---
title: Request domain separation
description: All domain support features are activated with a plugin called Domain Support - Domain Extensions Installer. Administrators can request activation of this plugin.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Domain separation setup and administration, Domain separation for service providers, Access Management]
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

2.  On the All Applications page, select **Request Plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of Activate Plugin form to capture details for activating the CSM Workspace plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/request-plugin.png)

3.  On Now Support, select the link to access the Now Support Service Portal Service Catalog.

    ![Message informing customers about new service portal with a link provided.](../../../reuse/images/hi-redirect.png)

4.  Select your instance.

5.  Select **Actions &gt; Activate Plugin**.

6.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Name of the plugin to activate.

 **Note:** If the system does not list the plugin you want or if you are activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

The date and time to activate the plugin.

 **Note:** Plugins are activated in two batches, once in the morning and once in the evening, on every business day in the US Pacific time zone. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr></tbody>
</table>    For example, see the following form to activate the CSM Workspace plugin on an instance named My Instance.

    ![Admin view of the form to capture details of the CSM Workspace plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Activate Plugin form")

7.  Select **Submit**.

    For additional details about requesting a plugin, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)


## Result

Activating the Domain Extension Installer plugin enables these features:

-   Domain separation is based on the Domain `[sys_domain]` table.
-   Delegated administration lets each domain have separate policy.
-   All records are part of the global domain.
-   The current user's domain determines the domain to use when viewing or operating on a record in a different domain.

**Related topics**  


[Domain separation plugin](../concept/domain-sep-plugin.md)

