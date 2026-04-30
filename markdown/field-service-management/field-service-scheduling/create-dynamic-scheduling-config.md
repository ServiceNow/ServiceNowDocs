---
title: Configure dynamic scheduling
description: Dynamic Scheduling enables automatic task assignment to field agents based on predefined rules and configurations. This feature helps streamline task distribution by ensuring the right tasks are assigned to the most suitable agents, optimizing travel time, skill matching, and task priority.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure dynamic scheduling

Dynamic Scheduling enables automatic task assignment to field agents based on predefined rules and configurations. This feature helps streamline task distribution by ensuring the right tasks are assigned to the most suitable agents, optimizing travel time, skill matching, and task priority.

## Before you begin

-   Select dynamic scheduling as the preferred task assignment method. This ensures that tasks are automatically assigned to field agents based on predefined criteria and rules. For more information, see [task assignment method](../../planning-and-policy/task/t_ConfigureFieldService.md#AssignmentOptions).
-   Set up agent schedules so that dynamic scheduling systematically ensures optimal task allocation. For more information, see [Setting up agent schedules for dynamic scheduling](../concept/agent-schedule-dynamic.md).
-   Review the properties and other installed components related to dynamic scheduling. Customize the settings to align with your organization's specific requirements. For more information, see [Review system properties and components for Dynamic Scheduling](../reference/dynamic-sched-system-properties.md).
-   Ensure to configure travel time and distance calculation to determine how the system calculates an agent's estimated travel time and distance to a task location. You can choose between using Google Maps API for real-time travel estimates or straight-line estimates based on the geolocation property settings.
    -   If the `Use Google Maps API for travel time estimates` geolocation property is enabled, choose between using Google Maps API or straight-line estimates.
    -   If the `Use Google Maps API for travel time estimates` geolocation property is disabled, the system considers the Estimated Travel Duration field's value from the work order task.

Role required: admin

## About this task

By default, the `Dynamic Scheduling Config for Work Order` configuration is available with the Dynamic Scheduling plugin. You can modify the configuration as needed or use as a template to create your custom configuration.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  Update an existing work configuration or create a new one.

    This field only appears if you have the plugin installed. For more information, see [Configuring Field Service Work Configurations](../concept/configuring-work-configs.md).

3.  Select the task table that dynamic scheduling will use to assign tasks to agents.

    The default table is `Work Order Task [wm_task]`. Dynamic scheduling can have only one configuration for each task table.

4.  Select the **Un-assignment** check box to let dynamic scheduling unassign a previously assigned task and assign a higher-priority task based on task ordering rules.

    When this option is not selected, the **Un-Assignment Constraints** related list will not be visible in the form.

5.  Select the **Default Agent Work Schedule**.

    Configure the order in which dynamic scheduling determines an agent’s work schedule - agent's specific work schedule, schedule specified on the agent’s user record, the default agent work schedule selected in this configuration, or the default 8-5 weekday schedule.

6.  Set the **Consider Territory Membership** to either consider or ignore the agent's territory membership for assigning tasks.

    This field appears when the Field Service Territory Planning plugin is enabled.

7.  In the **Task Filters** related list, add a task filter or modify an existing task filter or add a new filter.

    Task filters help identify which tasks should be assigned using dynamic scheduling. Within the filter, you can set criteria to match tasks with the most suitable agents. For more information, see [Create a task filter for dynamic scheduling](create-task-filter.md).

8.  In the **Task Ordering Rules** related list, add a new task ordering rule or modify an existing rule.

    Task ordering rules help to determine the order of tasks. For more information, [Create a task ordering rule](create-task-ordering-rule.md).

9.  In the **Un-Assignment Constraints** related list, add or modify criteria for un-assigning tasks.

    This allows the system to free up agents for higher-priority tasks when needed. For more information, see [Create a task unassignment constraint](create-unassignment-constraint.md).

10. Select **Update**.

11. Select **Validate config** to validate the dynamic scheduling configuration.

    An information message appears at the top of the Dynamic Scheduling Configuration form if the configuration is valid.


## Result

Dynamic scheduling automatically assign tasks to field agents based on the defined rules and schedules.

**Related topics**  


[Example - configure dynamic scheduling to assign preferred technicians to tasks](excluded-preferred-agents.md)

[Example - configure dynamic scheduling to ignore excluded technicians](prevent-excluded-agents.md)

[Using dynamic scheduling](../concept/using-dynamic-scheduling.md)

