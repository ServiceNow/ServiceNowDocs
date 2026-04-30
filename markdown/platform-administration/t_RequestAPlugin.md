---
title: Request a plugin
description: If a plugin does not appear in the Application Manager, you cannot activate it yourself. Request activation of the plugin by ServiceNow personnel.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow plugins, Basic system configuration, Get started, Administer]
---

# Request a plugin

If a plugin does not appear in the Application Manager, you cannot activate it yourself. Request activation of the plugin by ServiceNow personnel.

## Before you begin

**Note:** Before requesting or activating a plugin, check whether the plugin has already been activated on your instance. For details on how to check a plugin activation status, see the [Plugin Activation Status \[KB0678767\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0678767) article in the Now Support knowledge base.

Role required: admin

## About this task

There are two ways to request a plugin:

-   Access the Now Support Service Catalog on Now Support. Open the Activate Plugin page using this link: [Activate Plugin](https://support.servicenow.com/now?id=ns_automation_store&catalog_sys_id=891f088e465667e234a3cb52ffa1d299).
-   Access the Now Support Service Catalog through the Application Manager on your instance by following the procedure.

## Procedure

1.  Navigate to **Admin** &gt; **Application Manager**.

2.  From the Application Manager, select **Request Plugin** to open the **Activate Plugin** form on Now Support.

    ![Request Plugin button in the Application Manager.](../image/request-plugin-appmgr.png)

3.  On the **Activate Plugin** form on Now Support, provide the following information.

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
</table>    For example, see the following request to activate the CSM Workspace plugin on an instance named My Instance.

    ![Completed form to activate a plugin.](../../../reuse/images/activate-plugin-form.png "Activate Plugin form")

4.  Click **Submit**.

    For additional details about requesting a plugin, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)


**Parent Topic:**[ServiceNow plugins](../concept/c_ServiceNowPlugins.md)

**Related topics**  


[Activate a plugin](t_ActivateAPlugin.md)

[List of plugins \(Zurich\)](../reference/list-of-plugins.md#)

