---
title: Activate Orchestration
description: The Orchestration \(com.snc.runbook\_automation\) plugin is available within a separate subscription from the rest of the ServiceNow platform.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Orchestration

The Orchestration \(com.snc.runbook\_automation\) plugin is available within a separate subscription from the rest of the ServiceNow platform.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

Role required: none

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of the Application Manager interface with the Request plugin option highlighted.](../../../reuse/images/request-plugin.png)

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

    ![Admin view of the form requesting the Event Management plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Completed Activate Plugin form")

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


-   **[List of Orchestration plugins](../reference/list-orchestration-plugins.md)**  
This table lists all plugins available for Orchestration and their dependencies.
-   **[Orchestration Runtime plugin](../reference/orchestration-runtime-plugin.md)**  
The Orchestration – Runtime plugin enables other applications on the ServiceNow® platform to automate tasks, without requiring an Orchestration subscription.
-   **[List of Orchestration activities](../../../administer/orchestration-activities/reference/r_ListOfOrchestrationActivities.md)**  
Use Orchestration activities in a Workflow to integrate with third-party systems.
-   **[Available activity packs](../../../administer/orchestration-activities/task/t_ActivateAnActivityPack.md)**  
Activity packs are available with your subscription to Orchestration.
-   **[Deprecated Orchestration activities](../../../administer/orchestration-activities/reference/r_OrchestrationBasicActivities.md)**  
These Orchestration activities have been deprecated.

**Parent Topic:**[Classic Orchestration](../reference/r-orchestration.md)

