---
title: Activate database rotation
description: Learn how to activate database rotation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Applying database rotation techniques, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate database rotation

Learn how to activate database rotation.

## Before you begin

Role required: admin

## About this task

There are two database rotation plugins.

-   The Database Rotations \(com.snc.db.rotation\) plugin activates Table Rotation and Table Extension without any tables automatically included.
-   The Database Rotations Default Tables \(com.snc.db.rotation\_default\_tables\) plugin applies Table Rotation and Extension to specific tables.

    **Note:** Deployment of this plugin should be executed in partnership with a ServiceNow representative.


For new instances, database rotation is active by default. If you are upgrading from a previous version, users with the admin role can activate the Database Rotations \(com.snc.db.rotation\) plugin if it isn't already active.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Do not activate the Database Rotations Default Tables \(com.snc.db.rotation\_default\_tables\) plugin. Instead, specify the tables manually, after consulting a ServiceNow representative.

**Parent Topic:**[Applying database rotation techniques](../concept/c_DatabaseRotation.md)

**Related topics**  


[Table rotation](../../platform-performance/concept/c_TableRotation.md)

[Table extension](../../managing-data/concept/table-extension.md)

