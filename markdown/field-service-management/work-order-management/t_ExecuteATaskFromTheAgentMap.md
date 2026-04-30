---
title: Execute a task from the agent map
description: As an agent, you can accept or reject tasks assigned to you using features in the agent task map, or take on unassigned tasks near you if your schedule permits.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Execute a task from the agent map

As an agent, you can accept or reject tasks assigned to you using features in the agent task map, or take on unassigned tasks near you if your schedule permits.

## Before you begin

The Service Management Geolocation plugin \(com.snc.service\_management.geolocation\) must be enabled and the Google Maps Platform key must be entered into the appropriate [Google Maps property](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Role required: wm\_agent

## About this task

You can optimize task routes in the map to have the system determine the most efficient route. Initial routing shows the sequence established when the dispatcher assigned the tasks. Route optimization uses your location information and creates an ideal schedule based on variables such as location, task duration, travel time, or any [task windows](t_CreateAWorkOrderTask.md). The agent map, which displays color-coded icons for the tasks and your current location, is updated as you complete each task.

## Procedure

1.  Navigate to **Field Service** &gt; **Agent** &gt; **My Map**.

    Tasks that are in one of these states are visible on the map:

    -   **Assigned**
    -   **Accepted**
    -   **Pending Dispatch**
    -   **Work in Progress**

-   **[Agent map symbols](../reference/r_AgentMapSymbols.md)**  
The agent map shows your location, the tasks assigned to you for the current day, tasks that have been accepted, and other tasks that have not yet been assigned.
-   **[Agent location](../concept/c_AgentLocation.md)**  
The Field Service Management application calculates your location from a set of geographical coordinates.
-   **[Manage tasks on the map](../concept/c_ManageTasksOnTheMap.md)**  
The icons in the task map mark the location of tasks assigned to you and any unassigned tasks in your area.
-   **[Pick up an unassigned task](t_PickUpAnUnassignedTask.md)**  
Agents can assign themselves nearby unassigned tasks directly from the agent task map.

**Parent Topic:**[Execute work order tasks](../concept/c_ExecuteWorkOrderTasks.md)

