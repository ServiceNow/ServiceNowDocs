---
title: Request workflow pause utility
description: You can request the Workflow Pause Utility plugin \(com.glideapp.workflow.pause\) if you have the admin role. This plugin may include demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow pause utility, Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request workflow pause utility

You can request the Workflow Pause Utility plugin \(com.glideapp.workflow.pause\) if you have the admin role. This plugin may include demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

There are two ways to request a plugin:

-   Access the Now Support Service Catalog directly by selecting **Automation Store** &gt; **Service Catalog** &gt; **Activate Plugin** on Now Support.
-   Access the Now Support Service Catalog through the All Applications page on your instance by following these steps.

For additional details about requesting a plugin, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)

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


**Parent Topic:**[Workflow pause utility](../concept/workflow-pause-utility.md)

