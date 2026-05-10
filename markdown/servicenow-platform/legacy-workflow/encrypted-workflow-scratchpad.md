---
title: Encrypted workflow scratchpad
description: The Encrypted Workflow Scratchpad plugin \(com.snc.encrypted.scratchpad\) provides encrypted scratchpad support for workflow context and workflow executing activities.Request activation of the Encrypted Workflow Scratchpad plugin \(com.snc.encrypted.scratchpad\) from ServiceNow personnel
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Encrypted workflow scratchpad

The Encrypted Workflow Scratchpad plugin \(com.snc.encrypted.scratchpad\) provides encrypted scratchpad support for workflow context and workflow executing activities.

The platform supports encryption on most fields, and workflows can execute on tables with encrypted fields. Encrypted data is typically stored in the workflow scratch pad for workflows that execute using encrypted fields and must access this data after processing an approval, timer, or create task activity.

Data in the workflow scratchpad is not encrypted by default. The Workflow engine supports scratchpad encryption and executing activity records only when the Encrypted Workflow Scratchpad plugin is activated. Once activated, data stored in the wf\_context and wf\_executing scratchpads is protected by a private workflow engine encryption module, and is prevented from being stored in plain text.

## Incompatibility with domain separation

The Encrypted Workflow Scratchpad plugin is incompatible with domain separation. Activating the Encrypted Workflow Scratchpad plugin on a domain separated instance can produce encryption errors when running some workflows. Consider using a Workflow Studio flow instead.

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

## Request encrypted workflow scratchpad activation

Request activation of the Encrypted Workflow Scratchpad plugin \(com.snc.encrypted.scratchpad\) from ServiceNow personnel

### Before you begin

Role required: admin

The Encrypted Workflow Scratchpad plugin must be activated via a Customer Service and Support request. You should activate and thoroughly test the plugin in a non-production instance. Only after you satisfied with the results should you request activation in a production instance.

When requesting activation in a production instance, you should schedule a low transactional volume time to do so. Prior to its activation, first activate the Workflow Pause Utility \(com.glideapp.workflow.pause\), and then pause all active workflows. Refer to [Workflow pause utility](workflow-pause-utility.md). After activation of the Encrypted Workflow Scratchpad plugin, resume all paused workflows.

### About this task

There are two ways to request a plugin:

-   Access the Now Support Service Catalog directly by selecting **Automation Store** &gt; **Service Catalog** &gt; **Activate Plugin** on Now Support.
-   Access the Now Support Service Catalog through the All Applications page on your instance by following these steps.

For additional details about requesting a plugin, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)

Encrypted Workflow Scratchpad activates these related plugins if they are not already active.

<table id="table_rnl_3wk_fbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Encryption Support\[com.glide.encryption\]

</td><td>

Allows text fields and attached files to be encrypted.

</td></tr></tbody>
</table>### Procedure

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


### What to do next

After plugin activation, resume all paused workflows. Refer to [Pause and resume all or multiple workflows](../task/pause-resume-all-multiple-workflows.md).

**Related topics**  


[List of plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

