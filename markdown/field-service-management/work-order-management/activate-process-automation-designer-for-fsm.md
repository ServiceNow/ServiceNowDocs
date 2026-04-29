---
title: Activate Playbooks for Field Service Management
description: Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbooks, Set up work orders and tasks, Configure, Field Service Management]
---

# Activate Playbooks for Field Service Management

Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.

## Before you begin

Role required: Admin.

## About this task

In order to create Playbooks in Workflow Studio that are triggered by Field Service Management tables, you must [purchase a subscription to Field Service Management](https://www.servicenow.com/lpgp/pricing-field-service-management.html).

To purchase this subscription, contact your ServiceNow account manager. Your account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps to enable the **Playbooks for Field Service Management \[com.sn\_fsm\_playbook\]** plugin:

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


## Result

Enabling the **Playbooks for Field Service Management \[com.sn\_fsm\_playbook\]** plugin lets you create Playbooks for these tables and their [extensions](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=australia&pubname=australia-platform-administration&ft:locale=en-US):

-   Work Task Flow \[sf\_work\_task\]
-   Work Order Flow \[sf\_work\_order\]
-   Work Order Task \[wm\_Task\]
-   Work Order \[wm\_order\]
-   Work Order Model \[cmdb\_workorder\_product\_model\]
-   Work Task Model \[cmdb\_worktask\_product\_model\]
-   Work Type \[wm\_work\_type\]
-   Agent Personal Schedule \[agent\_events\]
-   Appointment Booking \[sn\_apptmnt\_booking\_appointment\_booking\]
-   Questionnaire \[wm\_questionnaire\]
-   Service Order Task \[sm\_task\]
-   Service Order Task Template Dependency \[sm\_m2m\_task\_template\_dependency\]
-   Asset Usage \[sm\_asset\_usage\]
-   Part Requirement \[sm\_part\_requirement\]
-   Service Management Incidentals \[sm\_incidentals\]

