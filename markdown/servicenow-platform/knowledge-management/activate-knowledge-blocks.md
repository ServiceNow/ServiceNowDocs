---
title: Activate knowledge blocks
description: You can activate knowledge blocks \[com.snc.knowledge\_blocks\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate knowledge blocks

You can activate knowledge blocks \[com.snc.knowledge\_blocks\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Knowledge blocks activates these related plugins if they are not already active.

<table id="table_b1h_mld_dbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Management Advanced\[com.snc.knowledge\_advanced\]

</td><td>

Enables advanced features for Knowledge Management, such as article versioning. For a full list of features, see [activate the Knowledge Management Advanced plugin](activate-knowledge-advanced-plugin.md).**Note:** Knowledge blocks can be used with or without the article versioning feature. To disable the feature, see [Disable the article versioning feature](article-versioning-disable-property.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

