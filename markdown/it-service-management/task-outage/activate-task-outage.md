---
title: Activate Task-Outage Relationship
description: Activate the Task-Outage Relationship plugin \(com.snc.task\_outage\) to track outage duration.
locale: en-US
release: yokohama
product: Task Outage
classification: task-outage
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Task Outage, IT Service Management]
---

# Activate Task-Outage Relationship

Activate the Task-Outage Relationship plugin \(com.snc.task\_outage\) to track outage duration.

## Before you begin

Role required: admin

## About this task

The Task-Outage Relationship plugin creates a many-to-many relationship between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Task-Outage Relationship](../reference/components-instld-with-task-outage.md)**  
The Task Outage table is installed with activation of the Task-Outage Relationship plugin \(com.snc.task\_outage\).

**Parent Topic:**[Task Outage](../concept/task-outage.md)

**Related topics**  


[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

