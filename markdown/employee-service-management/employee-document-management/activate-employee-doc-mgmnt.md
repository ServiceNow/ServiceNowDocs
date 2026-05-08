---
title: Activate Employee Document Management
description: You can activate the Employee Document Management \[com.sn\_employee\_document\_management\] plugin with the admin role. This plugin includes demo data and activates related plugins if they are not already active.The Employee Document Management Bulk Uploads requires separate subscriptions to the Orchestration \[com.snc.runbook\_automation\] and ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\] plugins. These plugins must be activated by ServiceNow personnel.
locale: en-US
release: australia
product: Employee Document Management
classification: employee-document-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Employee Document Management, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Activate Employee Document Management

You can activate the Employee Document Management \[com.sn\_employee\_document\_management\] plugin with the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Employee Document Management](../concept/configuring-employee-document-management.md)

**Related topics**  


[Defining and setting for employee documents](../concept/hr-doc-management-config.md#)

## Request employee document management bulk uploads

The Employee Document Management Bulk Uploads requires separate subscriptions to the Orchestration \[com.snc.runbook\_automation\] and ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\] plugins. These plugins must be activated by ServiceNow personnel.

### Before you begin

Role required: admin

### About this task

There is demo data available that provides configuration examples of a local directory and third-party, cloud-based document repositories. These examples help you to configure Employee Document Management bulk uploads with your own internal document repository.

To view the demo data, you must activate the Orchestration \[com.snc.runbook\_automation\] and ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\] plugins first.

The Employee Document Management \[com.sn\_hr\_employee\_document\_management\] plugin must be activated last.

<table id="table_h55_lbp_sfb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Orchestration\[com.snc.runbook\_automation\]

</td><td>

Required for bulk imports from local drives.

</td></tr><tr><td>

ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\]

</td><td>

Required for bulk imports from third-party, cloud-based document repositories.

</td></tr></tbody>
</table>To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

### Procedure

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


**Related topics**  


[bundle-platadm.list-of-plugins]

