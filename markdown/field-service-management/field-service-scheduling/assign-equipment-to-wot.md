---
title: Scheduling and assigning equipment to tasks and crews
description: Assigning equipment to a work order task ensures that crews or assigned agents are properly equipped for the task.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Scheduling and assigning equipment to tasks and crews

Assigning equipment to a work order task ensures that crews or assigned agents are properly equipped for the task.

An administrator must install the Field Service Resource Scheduling plugin \(com.snc.resource\_scheduling\). Resource scheduling is then added to the instance, and dispatchers are able to assign equipment to crews.

For information about configuring Field Service Resource Scheduling plugin, see [Configuring Resource Scheduling](configure-equipment-scheduling.md).

Dispatchers can assign equipment and resources to crews or tasks.

-   Assign equipment to planned crews.
-   Assign equipment to task crews.
-   Assign equipment to groups.

Crew leaders can use the Now Mobile agent app to modify their crews or manage their tasks. For more information, see [Crew on Mobile Agent](manage-crew-mobile-agent-app.md).

-   Add, remove, or swap planned crew members.
-   Add or remove equipment and agents according to the resource requirements of the task.

## Interactions with other features

-   **Skills**

    Admins to ensure only skilled, certified, or trained personnel are assigned the equipment. For more information, see [Add skills to an equipment instance](../task/add-skills-eq-instance.md).

-   **Geolocation tracking**

    The latitude and longitude fields \(position\) of equipment will update according to the status and location of the crew leader. If geo-tracking is enabled for the crew leader, the position of the equipment will update based on the positional updates of the crew leader. If geo-tracking is not enabled for the crew leader, the position of the equipment updates to the task location at the start of work. Position is cleared once the equipment is checked in.


-   **[Assign equipment to a planned crew](../task/add-equipment-to-a-planned-crew.md#)**  
Assign equipment to a planned crew to ensure they have tools for their work order tasks. Dispatchers can assign equipment through the ServiceNow AI Platform or Dispatcher Workspace. Crew leaders can assign equipment or modify their crews through the Now Mobile Agent application.
-   **[Assign equipment to a task crew](../task/create-a-task-crew-with-equipment.md)**  
Assign equipment to an ad hoc task crew to ensure they have the necessary tools to complete the work order task.
-   **[Assign an equipment instance to groups](../task/assign-eq-instance-to-groups.md)**  
Assign equipment instances to groups.
-   **[Create a maintenance schedule for an equipment instance](../task/create-maint-sched-for-eq-instance.md)**  
Create a schedule for regular maintenance or downtime for an equipment instance.

**Parent Topic:**[Scheduling and dispatching work order tasks to agents](scheduling-and-dispatching-agents.md)

**Related topics**  


[Configuring Resource Scheduling](configure-equipment-scheduling.md)

