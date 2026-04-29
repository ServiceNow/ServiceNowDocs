---
title: Activate Problem Management Best Practice — Madrid — State Model
description: You can activate the Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) on your instance using the Problem Management Migration Utility store app.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migration job, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Activate Problem Management Best Practice — Madrid — State Model

You can activate the Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) on your instance using the Problem Management Migration Utility store app.

## Before you begin

Before you activate the plugin, be sure to resolve blocking modifications. For more information, see [Resolve blocking modifications](resolve-blocking-modifications.md).

Role required: admin

## About this task

An administrator must activate the Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) \(first introduced in the Madrid release\) through the Migration Utility because the plugin includes features that are not compatible with the previous version of Problem Management.

New York Patch 9 or Orlando Patch 3 or later are required before the administrator can see and activate the problem state model plugin on an instance. If you do not have the required patch, you have to request the plugin as it is a development plugin.

## Procedure

1.  Activate the plugin.

    If you have the required patch level, you have access to the plugin and can activate it. If you do not have the patch level, you must request it.

<table id="choicetable_zxl_xhm_plb"><tbody><tr><td id="d374726e92">

**Activate the plugin \(required patch level is installed\)**

</td><td>

1.  Click **Request Plugin** in the plugin activation stage of the migration utility migration job.
2.  On the System Plugin page, click the **Activate/Repair** related link.
3.  Click **Activate**.
4.  Close and reload the form.

The plugin status changes to **Activated**. You can return to the Migration Utility and continue with the migration.

</td></tr><tr><td id="d374726e130">

**Request the plugin**

</td><td>

1.  Click **Request Plugin** in the plugin activation stage of the migration utility migration job.
2.  On the [ServiceNow HI Request Plugin](https://support.servicenow.com/hisp?id=hisp_sc_item&sys_id=891f088e465667e234a3cb52ffa1d299) page, provide the required details.
    -   Target instance: Instance on which to request the plugin
    -   Plugin Name: `com.snc.best_practice.problem.madrid.state_model`
    -   Reason/Comments: `Request from the Problem Management Migration Utility`
    -   Select Maintenance Start Time: Select your preferred start time
3.  Click **Submit**.
4.  Once the plugin is activated, return to the Migration Utility and continue with the migration.


</td></tr></tbody>
</table>2.  Continue with the migration process.


## What to do next

[Prepare base plugins](prepare-base-plugins.md).

