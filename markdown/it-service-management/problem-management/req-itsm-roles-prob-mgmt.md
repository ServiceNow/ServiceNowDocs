---
title: Request ITSM Roles — Problem Management
description: Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\) to gain more control over the access that different service desk agents, technicians, and managers have within your Problem Management process.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Problem Management plugins, Configuring Problem Management, Problem Management, IT Service Management]
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


-   **[Components installed with ITSM Roles — Problem Management](../reference/prob-roles-instld-itsm-roles.md)**  
Several user roles are installed with activation of the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\).

**Parent Topic:**[Problem Management plugins](../concept/problem-mgmt-plugins.md)

**Related topics**  


[List of Xanadu plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

