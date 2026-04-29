---
title: Request ITSM Roles - Request Management
description: Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Request Management plugin \(com.snc.itsm.roles.request\_management\) to gain more control over the access that different service desk agents, technicians, and managers have within your Request Management process.
locale: en-US
release: australia
product: Request Management
classification: request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Request Management, IT Service Management]
---

# Request ITSM Roles - Request Management

Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Request Management plugin \(com.snc.itsm.roles.request\_management\) to gain more control over the access that different service desk agents, technicians, and managers have within your Request Management process.

## Before you begin

Role required: admin

## About this task

The ITSM Roles plugin \(com.snc.itsm.roles\) includes an additional security model. The security model provides more granular roles across ITSM applications as well as within them, allowing you flexibility in setting up access controls. The ITSM Roles plugin is available by default in new instances. Users upgrading from Madrid or earlier versions must request the plugin.

<table id="table_ayg_r2j_nhb"><thead><tr><th>

Plugin

</th><th>

Adds roles

</th></tr></thead><tbody><tr><td>

Business Stakeholder \[com.snc\_business\_stakeholder\]

</td><td>

business\_stakeholder**Note:** The business\_stakeholder role contains the sn\_incident\_read, sn\_problem\_read, sn\_change\_read, sn\_request\_read, and approver\_user roles.

</td></tr><tr><td>

ITSM Roles — Incident Management \[com.snc.itsm.roles.incident\_management\]

</td><td>

-   sn\_incident\_read
-   sn\_incident\_write

</td></tr><tr><td>

ITSM Roles — Problem Management \[com.snc.itsm.roles.problem\_management\]

</td><td>

-   sn\_problem\_read
-   sn\_problem\_write

</td></tr><tr><td>

ITSM Roles — Change Management \[com.snc.itsm.roles.change\_management\]

</td><td>

-   sn\_change\_read
-   sn\_change\_write

</td></tr><tr><td>

ITSM Roles — Request Management \[com.snc.service\_management.roles.request\_management\]

</td><td>

-   sn\_request\_read
-   sn\_request\_write
-   sn\_request\_comment\_write

 **Note:** The sn\_request\_comment\_write role alone doesn't give access to comments write, you need write access for the table.

</td></tr></tbody>
</table>To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

**Note:** Activate the ITSM Roles plugin on a subproduction environment and test the functionality before requesting activation in the production environment. For assistance, contact the ServiceNow Professional Services team.

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


-   **[Components installed with ITSM Roles — Request Management](req-mgmnt-roles-instld-itsm.md)**  
Several user roles are installed with the activation of the ITSM Roles - Request Management plugin \(com.snc.itsm.roles.request\_management\).

**Parent Topic:**[Request Management reference](../../request-management/concept/request-management-reference.md)

