---
title: Activate a plugin
description: You can activate most plugins to expand features and functionalities in the ServiceNow AI Platform.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow plugins, Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Activate a plugin

You can activate most plugins to expand features and functionalities in the ServiceNow AI Platform.

## Before you begin

Role required: admin.

**Note:** Before requesting or activating a plugin, check whether the plugin has already been activated on your instance. For details on how to check a plugin activation status, see the [Plugin Activation Status \[KB0678767\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0678767) article in the Now Support knowledge base.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[List of plugins \(Xanadu\)](../reference/list-of-plugins.md#)

