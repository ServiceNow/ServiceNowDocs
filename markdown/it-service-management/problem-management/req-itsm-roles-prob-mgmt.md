---
title: Request ITSM Roles — Problem Management
description: Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\) to gain more control over the access that different service desk agents, technicians, and managers have within your Problem Management process.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Problem Management plugins, Configure, Problem Management, IT Service Management]
---

# Request ITSM Roles — Problem Management

Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\) to gain more control over the access that different service desk agents, technicians, and managers have within your Problem Management process.

## Before you begin

Role required: admin

## About this task

The ITSM Roles plugin activates several related plugins such as Business Stakeholder \(com.snc\_business\_stakeholder\), ITSM Roles — Incident Management \(com.snc.itsm.roles.incident\_management\), ITSM Roles — Problem Management \(com.snc.itsm.roles.problem\_management\), ITSM Roles — Change Management \(com.snc.itsm.roles.change\_management\), and ITSM Roles — Request Management \(com.snc.service\_management.roles.request\_management\). The related plugins updates the security model and introduces roles for respective products.

With the introduction of the new roles, ITSM provides more control over the access that users have within the process.

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


-   **[Components installed with ITSM Roles — Problem Management](../reference/prob-roles-instld-itsm-roles.md)**  
Several user roles are installed with activation of the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\).

**Parent Topic:**[Problem Management plugins](../concept/problem-mgmt-plugins.md)

**Related topics**  


[List of Zurich plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

