---
title: Request Predictive Intelligence for Incident
description: To activate Predictive Intelligence for Incident, request the Predictive Intelligence for Incident plugin \(com.snc.incident.ml\) through the Now Support Customer Service system. This plugin activates related plugins if they are not already active.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for IT Service Management, IT Service Management]
---

# Request Predictive Intelligence for Incident

To activate Predictive Intelligence for Incident, request the Predictive Intelligence for Incident plugin \(com.snc.incident.ml\) through the Now Support Customer Service system. This plugin activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Predictive Intelligence for Incident plugin activates these related plugins if they are not already active.

<table id="table_o2w_dby_jlb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predictive Intelligence for Contextual Search\[com.snc.contextual\_search\_ml\]

</td><td>

Enables customers to leverage machine-learning algorithms for searching with Contextual Search. For example: Similar Open Incidents. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td></tr></tbody>
</table>## Procedure

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


-   **[Predictive Intelligence for Incident](../concept/pi-for-incident.md)**  
Use your instance records to build Incident Management -specific solutions.

**Parent Topic:**[Machine learning solutions for IT Service Management](../../it-service-management/concept/machine-learning-itsm.md)

**Related topics**  


[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

