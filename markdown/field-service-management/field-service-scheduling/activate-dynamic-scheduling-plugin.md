---
title: Activate dynamic scheduling
description: Activate the dynamic scheduling feature by activating the Field Service Management plugin \(com.snc.work\_management\).
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Activate dynamic scheduling

Activate the dynamic scheduling feature by activating the Field Service Management plugin \(com.snc.work\_management\).

## Before you begin

Role required: admin

## About this task

The Field Service Management plugin activates the Dynamic Scheduling plugin \(com.snc.dynamic\_scheduling\) and adds the following module to the Field Service menu in the application navigator: **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

The following tables are installed with dynamic scheduling:

<table id="table_udf_cmc_kt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Constraint \[scheduling\_constraint\]

</td><td>

Stores the unassignment constraints for the dynamic scheduling feature.

</td></tr><tr><td>

Dynamic Scheduling Configuration\[dynamic\_scheduling\_config\]

</td><td>

Stores the configurations for the dynamic scheduling feature. Configurations include the selected task table, task filters, task ordering rules, and task unassignment constraints.

</td></tr><tr><td>

Task Filter\[dynamic\_schedule\_task\_filter\]

</td><td>

Stores the task filters for a dynamic scheduling configuration. Filters identify a list of tasks to be assigned using dynamic scheduling.

</td></tr><tr><td>

Task Ordering Rule \[task\_ordering\_rule\]

</td><td>

Stores the task ordering rules for a dynamic scheduling configuration. Ordering rules prioritize the list of tasks identified by the task filters.

</td></tr><tr><td>

Un-Assignment Constraint\[unassignment\_rule\]

</td><td>

Stores the task unassignment constraints for a dynamic scheduling configuration. Constraints prevent a task from being unassigned even if it is of lower importance based on the task ordering rules.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


