---
title: Universal Task data model
description: The Universal Task is a tasking framework that you can append to the ticketing system of any department in your organization. The Universal Task data model explains the tasking framework and its customizations.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Universal Task, Universal Task, Employee Service Management]
---

# Universal Task data model

The Universal Task is a tasking framework that you can append to the ticketing system of any department in your organization. The Universal Task data model explains the tasking framework and its customizations.

You can create Universal Task for any department or service, such as a universal request, an incident, an HR case, or a legal matter. You can also assign multiple universal tasks for a single request.

The following diagram is a high-level overview of the Universal Task data model.

![Universal task data model.](../images/ut-data-model.png)

The Universal Task data model uses a combination of tables to store data:

-   ServiceNow AI Platform tables.
-   Tables that are included with the Universal Task application.

For information on the tables and components that are installed with the Universal Task application, see [Components installed with Universal Task](../reference/installed-with-uni-task.md).

The Universal Task \[sn\_uni\_task\_universal\_task\] table extends the Task \[task\] table to include:

-   The type of task for the current record, for example, Upload document.
-   The catalog item if the task is of type Submit Catalog Item.
-   The generated table that stores the table name that contains the requested catalog items.
-   The generated ID that is the sys\_id of the requested catalog item.

    **Note:** The catalog item, generated table, and generated ID are only applicable for the Submit Catalog item task type.

-   The employee form that is used to request information for the Collect Employee Input task type.
-   The survey instance that stores the instance ID of the employee form for the Collect Employee Input task type.
-   Task template to be used, if any, to auto-fill the Universal Task \[universal-task\] form.

The values for the State and Priority fields in the Task \[task\] table have been modified for Universal Task. The valid states for Universal Task are:

-   1: New \(Draft state\). Tasks at this state are only visible to the agent.
-   2: Work in Progress. Tasks at this state are assigned to and visible to the employee.
-   3: Complete. Tasks transition to the complete state when the employee completes the task.
-   4: Canceled. Tasks at this state can be canceled by agents before the task is completed.

The valid priority values for Universal Task are:

-   1: Critical. Highest priority for urgent or time-sensitive tasks.
-   2: High. Tasks that are important but not urgent.
-   3: Moderate. Tasks that should be completed.
-   4: Low. Optional tasks.

The Universal Task \[sn\_uni\_task\_universal\_task\] table follows data separation.

## Universal Task configuration table

The Universal Task configuration table is configured to identify the following details:

-   The Parent table, or the department-specific table that uses Universal Task. For example, if Universal Task is being used with HR cases, then the HR case table is the parent table. Universal Task can only be created on a table that is an extension of the task table.
-   The task types that are available to the agents to task the requester with. For more details, see [Universal Task types](universal-task-types.md).
-   The **Default Assigned to** field that points to the **requester** field in the parent table. To auto-fill the **Assigned to** field with the assignee while creating a task, configure the **Default Assigned to** field.

For more details, see [Configure Universal Task for your service](../task/config-ut-for-service.md).

Specific task types might have additional configuration tables. For example, for the Submit catalog item task type, the Catalog task configuration \[sn\_uni\_task\_catalog\_task\_config\] table determines which filters to apply to the catalog items that are available to an agent. For more information, see [Configure the catalog items for your service](../task/config-catalog-task.md).

The Universal task configuration \[sn\_uni\_task\_config\] table and the Catalog task configuration \[sn\_uni\_task\_catalog\_task\_config\] table follow process separation.

**Parent Topic:**[Exploring Universal Task](explore-universal-task.md)

