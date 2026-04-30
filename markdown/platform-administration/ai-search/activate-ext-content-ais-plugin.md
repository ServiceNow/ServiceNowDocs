---
title: Request the External Content for AI Search plugin
description: Request activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\) to enable indexing of searchable content and metadata from records in external data sources.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Indexing and searching external content, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Request the External Content for AI Search plugin

Request activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\) to enable indexing of searchable content and metadata from records in external data sources.

## Before you begin

You must purchase a paid subscription before requesting activation of the plugin. For details on purchasing a paid subscription for a plugin, see [ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md).

Role required: admin

## About this task

You can't activate the External Content for AI Search plugin from your instance or the ServiceNow Store. Use this procedure to submit a Now Support request for activation of the plugin for your instance.

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


**Parent Topic:**[Indexing and searching external content in AI Search](../concept/external-content-ais.md)

