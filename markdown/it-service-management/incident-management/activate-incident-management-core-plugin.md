---
title: Request Incident Management — Core
description: Incident Management - Core plugin \(com.snc.incident\_management\) is a new incident state model that includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Incident Management plugins, Reference section for Incident Management, Incident Management, IT Service Management]
---

# Request Incident Management — Core

Incident Management - Core plugin \(com.snc.incident\_management\) is a new incident state model that includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Incident Management - Core \(com.snc.incident\_management\) is available by default in new instances. Customers upgrading from Geneva or earlier versions must request the plugin. For more information, see [KB0564465](https://support.servicenow.com/kb_view.do?sysparm_article=KB0564465).

**Note:** If the new state model is installed on upgraded instances, then ensure that the old states are mapped to the new ones. The mapping is especially important if you have made customizations, implemented workflows, added script includes, and added business rules.

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


**Parent Topic:**[Incident Management plugins](../concept/incident-mgmt-plugins.md)

**Related topics**  


[List of Australia plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

