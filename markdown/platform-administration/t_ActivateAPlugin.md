---
title: Activate a plugin
description: You can activate most plugins to expand features and functionalities in the ServiceNow AI Platform.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow plugins, Basic system configuration, Get started, Administer]
---

# Activate a plugin

You can activate most plugins to expand features and functionalities in the ServiceNow AI Platform.

## Before you begin

**Note:** Before requesting or activating a plugin, check whether the plugin has already been activated on your instance. For details on how to check a plugin activation status, see the [Plugin Activation Status \[KB0678767\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0678767) article in the Now Support knowledge base.

If you are ready to install, first confirm the product is an application or a plugin. See [KB1438103](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1438103) for more information. The subsequent activation workflow depends on this product type. For identification guidelines, see [Plugins vs Store Apps \[KB1585881\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585881).

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


1.  Obtain a detailed description of the reported issue.
2.  Verify the status of the plugin in the Plugins module \( v\_plugin\). The Plugins module maps to the v\_plugin table.
3.  Check the sys\_plugin\_log table for any skipped records.
4.  Validate the final record state \(skipped or loaded\) by querying the target table using the associated sys\_id. Most of the records should show a "loaded" status.

**Note:**

For detailed information on troubleshooting plugin issues, see [KB0691461](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=f8a2b7ee1b30a91026e3c8cc1d4bcbb8).

**Related topics**  


[List of plugins \(Zurich\)](../reference/list-of-plugins.md#)

