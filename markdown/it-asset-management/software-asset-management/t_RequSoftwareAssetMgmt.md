---
title: Request Software Asset Management
description: The ServiceNow Software Asset Management Professional \(com.snc.samp\) plugin requires a separate subscription. This plugin includes demo data. Depending on your environment, you may choose to request one or more related plugins.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Software Asset Management, IT Asset Management]
---

# Request Software Asset Management

The ServiceNow® Software Asset Management Professional \(com.snc.samp\) plugin requires a separate subscription. This plugin includes demo data. Depending on your environment, you may choose to request one or more related plugins.

## Before you begin

To purchase a subscription or load demo data after activation, contact your ServiceNow account manager. Within a few days, the account manager can activate the plugin and load any demo data on the production and non-production instances of your organization.

If you do not have an account manager, decide to delay activation until after your purchase, or want to evaluate the product on a non-production instance at no extra charge, you can use this procedure to submit a plugin activation request through the ServiceNow® Now Support Service Portal.

**Warning:** If you upgrade to the Software Asset Management Professional \(com.snc.samp\) plugin from the Software Asset Management plugin \(com.snc.software\_asset\_management\), then you cannot revert to the Software Asset Management plugin \(com.snc.software\_asset\_management\).

Role required: admin

## About this task

Depending on your environment, you can request related plugins with the Software Asset Management Professional \(com.snc.samp\) plugin. You can request the optional plugins through either the Now Support Service Portal or through the ServiceNow Store.

For the list of Software Asset Management Professional plugins, see [Components installed with Software Asset Management Professional](../reference/sam-installed-components.md).

Only ServiceNow personnel can activate the Software Asset Management Professional \(com.snc.samp\) plugin and other related plugins. The plugins are not visible in the plugin list, even after activation.

**Warning:** After installing the Software Asset Management application for the first time, or upgrading from the Software Asset Management Foundation plugin, you need to revert customizations for all features work. The Revert Customizations module in the Software Asset Management application can revert customized files related to Software Asset Management back to the base configurations that were skipped during the installation or upgrade process. See [Revert Software Asset Management customizations](revert-sam-customizations.md)

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

 **Note:** Select Software Asset Management Professional Master Workspace \(com.sn\_samp\_master\_ws\) plugin. If the system does not list the plugin you want or if you are activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

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


**Parent Topic:**[Configuring Software Asset Management](../concept/Config-sam-workspace.md)

