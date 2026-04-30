---
title: Activate Employee Document Management
description: You can activate the Employee Document Management \[com.sn\_employee\_document\_management\] plugin with the admin role. This plugin includes demo data and activates related plugins if they are not already active.The Employee Document Management Bulk Uploads requires separate subscriptions to the Orchestration \[com.snc.runbook\_automation\] and ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\] plugins. These plugins must be activated by ServiceNow personnel.
locale: en-US
release: xanadu
product: Employee Document Management
classification: employee-document-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Employee Document Management, Employee Document Management, HR Service Delivery, Employee Service Management]
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

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


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


**Related topics**  


[List of plugins \(Madrid\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

