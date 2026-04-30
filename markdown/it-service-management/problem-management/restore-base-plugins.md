---
title: Restore base plugins
description: Repair the plugins in the specified order to restore the base functionality that is required for the problem state model.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migration job, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Restore base plugins

Repair the plugins in the specified order to restore the base functionality that is required for the problem state model.

## Before you begin

Role required: admin

## About this task

New York Patch 9, or Orlando Patch 3 or later are required before you can see and repair the Problem Management Best Practice – Jakarta \(com.snc.best\_practice.problem.jakarta\) and Problem Management Best Practice — Madrid — State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugins. Before the mentioned patches, these plugins were development plugins.

**Note:** If you do not have the required patch, refer to Blocking modifications for required base functionality in the [KB0819196](https://support.servicenow.com/kb_view.do?sysparm_article=KB0819196) article in the HI Knowledge Base.

## Procedure

1.  Repair the plugins, one at a time.

    1.  Repair the plugin or apply the update set as required.

        **Note:** Certain plugins contain functionality for applications including Problem Management. For those plugins, refer to the specified knowledge article to restore the required problem functionality instead of repairing the plugin.

    2.  Return to the migration job and mark that plugin as repaired.
2.  Click **Run Checks**.


## What to do next

[Resolve blocking and warning modifications](resolve-blocking-warning-modifi.md).

