---
title: Request Service Mapping
description: Service Mapping is available under the ITOM Visibility subscription and requires activation by ServiceNow personnel.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Request Service Mapping

Service Mapping is available under the ITOM Visibility subscription and requires activation by ServiceNow personnel.

## Before you begin

Role required: none

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

Role required: admin

## About this task

****The following plugins are activated automatically when the Service Mapping plugin \(com.snc.service-mapping\) is activated:

-   Discovery \(com.snc.discovery\)

    **Note:** If you're activating the Discovery plugin for the first time in the Xanadu release, install the Discovery \(com.snc.discovery\) plugin first, then install the Discovery and Service Mapping Patterns \(com.sn\_itom\_pattern\) plugin version 1.0.52 for Cloud Discovery to work. You can then upgrade to Xanadu.

-   Pattern Designer \(com.snc.pattern.designer\)
-   Cloud Provisioning and Governance Core \(com.snc.cloud.core\)
-   Performance Analytics – Content Pack – Service Mapping \(com.snc.service-mapping.pa.content\)
-   Event Management and Service Mapping Core \(com.snc.service-watch\)

    **Note:** The Event Management and Service Mapping Core \(com.snc.service-watch\) plugin is different from the Event Management plugin \(com.glideapp.itom.snac\).


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


**Related topics**  


[Credentials required for host discovery](../reference/r_Credentials4HostDiscovery.md)

