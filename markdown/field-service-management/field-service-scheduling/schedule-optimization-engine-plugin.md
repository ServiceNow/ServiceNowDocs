---
title: Activate Schedule Optimization
description: Activate the Schedule Optimization plugin \(com.snc\_schedule\_optimization\) for Field Service Management with the administrator role.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Activate Schedule Optimization

Activate the Schedule Optimization plugin \(com.snc\_schedule\_optimization\) for Field Service Management with the administrator role.

## Before you begin

Role required: admin

-   Schedule Optimization requires a separate subscription from the rest of the ServiceNow AI Platform.

    To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a plugin doesn't appear in the instance, submit a request via the Now Support Service Catalog.

-   Schedule Optimization requires the following plugins. Ensure that these plugins are activated before you install Schedule Optimization.
    -   **Predictive Intelligence \(com.glide.platform\_ml\)**

        Provides various capabilities and solution types for training the system to predict, recommend, and drive data outcomes.

    -   **Field Service Management \(com.snc.work\_management\)**

        Adds a number of plugins related to agent scheduling and work order task management.

    -   **Map Integrations for Field Service \(com.snc.app\_fsm\_map\_integr\)**

        Performs intelligent travel time estimates to allocate work order tasks to agents, taking into account both the agent's location and the task's location.


Role required: admin

## About this task

The following items are installed with Schedule Optimization:

<table id="table_dfc_45z_fyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Optimization Scope snc\_schedule\_optim\_optimization\_scope

</td><td>

Defines the qualifiers \(groups or territories\), tasks, and policies to be used during optimization

</td></tr><tr><td>

Scope Qualifier snc\_schedule\_optim\_scope\_m2m\_qualifier

</td><td>

Relates a group or territory to a scope

</td></tr><tr><td>

Optimization Batch snc\_schedule\_optim\_batch

</td><td>

Defines the optimization schedule for one or more scope

</td></tr><tr><td>

Optimization Feature snc\_schedule\_optim\_optimization\_constraints

</td><td>

Defines the objectives and constraints to be used in optimization policies **Note:** table is read only

</td></tr><tr><td>

Policies snc\_schedule\_optim\_policy

</td><td>

Container record for objectives and constraints that are used for optimization

</td></tr><tr><td>

Policy Configurations snc\_schedule\_optim\_policy\_configuration

</td><td>

A related list is table used to add objectives and constraints to a policy

</td></tr><tr><td>

Scheduling Attribute Configuration snc\_schedule\_optim\_sched\_attr\_config

</td><td>

Defines common optimization settings to be used by intraday configurations or optimization batches and scopes

</td></tr><tr><td>

Intraday Configuration snc\_schedule\_optim\_intraday\_config

</td><td>

Defines the default scheduling attribute configuration, the default processing window and flow for intraday optimization

</td></tr><tr><td>

Intraday Qualifier snc\_schedule\_optim\_intraday\_m2m\_qualifier

</td><td>

Relates a group or territory to an intraday configuration

</td></tr><tr><td>

Intraday Attribute Override snc\_schedule\_optim\_intraday\_m2m\_sched\_attr\_config

</td><td>

Overrides the default scheduling attribute configuration or default processing window for a particular group or territory

</td></tr><tr><td>

Intraday Job Qualifier wm\_intraday\_job\_m2m\_qualifier

</td><td>

Relates a group or territory to an intraday job

</td></tr><tr><td>

On-Demand Optimization Applicable Policies snc\_schedule\_optim\_attr\_m2m\_policy

</td><td>

Defines the alternate policies eligible for an on-demand optimization run for a particular scheduling attribute configuration

</td></tr></tbody>
</table>For more information, see [Configuring Schedule Optimization](../concept/schedule-optimization-engine.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Schedule Optimization plugin \(com.snc\_schedule\_optimization\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

[Create a policy for Schedule Optimization](create-policies-schedule-optimization.md)

