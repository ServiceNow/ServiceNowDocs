---
title: Scheduling and assigning equipment to tasks and crews
description: Assigning equipment to a work order task ensures that crews or assigned agents are properly equipped for the task.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scheduling and dispatching, Use, Field Service Management]
---

# Scheduling and assigning equipment to tasks and crews

Assigning equipment to a work order task ensures that crews or assigned agents are properly equipped for the task.

An administrator must install the Field Service Resource Scheduling plugin \(com.snc.resource\_scheduling\). Resource scheduling is then added to the instance, and dispatchers are able to assign equipment to crews.

For information about configuring Field Service Resource Scheduling plugin, see [Configuring Resource Scheduling](configure-equipment-scheduling.md).

Dispatchers can assign equipment and resources to crews or tasks.

-   Assign equipment to planned crews.
-   Assign equipment to task crews.
-   Assign equipment to groups.

Crew leaders can use the Now Mobile agent app to modify their crews or manage their tasks. For more information, see [Crew on ServiceNow Agent](manage-crew-mobile-agent-app.md).

-   Add, remove, or swap planned crew members.
-   Add or remove equipment and agents according to the resource requirements of the task.

## Interactions with other features

-   **Skills**

    Admins to ensure only skilled, certified, or trained personnel are assigned the equipment. For more information, see [Add skills to an equipment instance](../task/add-skills-eq-instance.md).

-   **Geolocation tracking**

    The latitude and longitude fields \(position\) of equipment will update according to the status and location of the crew leader. If geo-tracking is enabled for the crew leader, the position of the equipment will update based on the positional updates of the crew leader. If geo-tracking is not enabled for the crew leader, the position of the equipment updates to the task location at the start of work. Position is cleared once the equipment is checked in.


**Related topics**  


[Configuring Resource Scheduling](configure-equipment-scheduling.md)

