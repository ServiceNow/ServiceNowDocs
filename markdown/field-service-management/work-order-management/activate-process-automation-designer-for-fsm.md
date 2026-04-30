---
title: Activate Playbooks for Field Service Management
description: Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Playbooks for Field Service Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
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


## Result

Enabling the **Playbooks for Field Service Management \[com.sn\_fsm\_playbook\]** plugin lets you create Playbooks for these tables and their [extensions](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US):

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

