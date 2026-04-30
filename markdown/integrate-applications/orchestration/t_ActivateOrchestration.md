---
title: Activate Orchestration
description: The Orchestration \(com.snc.runbook\_automation\) plugin is available within a separate subscription from the rest of the ServiceNow platform.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Classic Orchestration, Creating integrations with applications]
---

# Activate Orchestration

The Orchestration \(com.snc.runbook\_automation\) plugin is available within a separate subscription from the rest of the ServiceNow platform.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

Role required: none

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

