---
title: Request the Password Reset Windows App plugin
description: Request the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin that enables connections to the Active Directory \(AD\) credential store types. No other components are installed.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request the Password Reset Windows App plugin

Request the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin that enables connections to the Active Directory \(AD\) credential store types. No other components are installed.

## Before you begin

Role required: admin

## About this task

There are two ways to request a plugin:

-   Access the Now Support Service Catalog directly by selecting **All** &gt; **Service Catalog** &gt; **Activate Plugin** on Now Support. For more information about the list of plugins, see [List of Plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Access the Now Support Service Catalog through the All Applications page on your instance by following these steps.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  On the All Applications page, select **Request Plugin** to open the Request form on HI.

    ![Request Plugin button on the All Applications page.](../../../reuse/images/request-plugin.png)

3.  On Now Support, select the redirect link to access the Now Support Service Portal Service Catalog.

    ![HI redirect to Service Catalog..](../../../reuse/images/hi-redirect.png)

4.  Select your instance.

5.  Select **Actions &gt; Activate Plugin**.

6.  On the form, fill in the fields.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

Target Instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Plugin Name

</td><td>

Name of the plugin to activate.

</td></tr><tr id="date-time"><td>

Specify the date and time you would like this plugin to be enabled

</td><td>

The date and time must be at least two business days from the current time.**Note:** Plugins are activated in two batches, in the morning and in the evening, on every business day in the US Pacific time zone. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr><tr id="reasons-comments"><td>

Reason/Comments

</td><td>

Information that would be helpful for the ServiceNow personnel who are activating the plugin. For example, if you need the plugin activated at a specific time instead of during one of the default activation windows, specify that in the comments.

</td></tr></tbody>
</table>7.  Select **Submit**.


**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

