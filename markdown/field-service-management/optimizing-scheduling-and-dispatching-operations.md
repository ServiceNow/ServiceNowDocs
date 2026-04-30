---
title: Optimizing Scheduling and Dispatching operations
description: Explore how dispatchers manage scheduling and dispatching operations to verify tasks are assigned efficiently to field agents, maximizing resource use and customer satisfaction. Discover the mechanisms behind effective task allocation, verifying that the right task goes to the right agent at the right time for smooth service delivery.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Field Service Management]
---

# Optimizing Scheduling and Dispatching operations

Explore how dispatchers manage scheduling and dispatching operations to verify tasks are assigned efficiently to field agents, maximizing resource use and customer satisfaction. Discover the mechanisms behind effective task allocation, verifying that the right task goes to the right agent at the right time for smooth service delivery.

## The Scheduling Challenge

Dispatchers are responsible for determining which field agent should attend to which tasks, and when, during their shift. Their goal is to produce a service schedule, creating an optimal task schedule for all agents in the field.

Given that each task takes two hours to complete and each agent has an eight-hour shift, each field agent can complete up to four tasks during one shift. For four tasks and four resources:

-   All four agents could each take one task.
-   One agent could handle all four tasks.
-   Two agents could split the tasks, each taking two tasks.
-   Three agents could divide the tasks with one agent taking two tasks and the other two taking one task each.

## Overview of Scheduling Methods

The goal of scheduling is to verify that the right task is assigned to the right field agent at the right time, optimizing resource utilization, and customer satisfaction. Understanding the scheduling mechanisms provides a holistic view of task allocation options available to a dispatcher.

-   Manual: Manual scheduling involves the traditional drag-and-drop method, enabling dispatchers to manually assign tasks to field agents. While suitable for smaller teams with limited tasks, manual scheduling can be time-consuming and prone to errors.
-   Interactive: Auto-Assign, Intelligent Task Recommendation, and Route Optimization
    -   Dispatchers can use various interactive tools to find the best assignment, but the dispatcher makes the final decision. Auto-Assign manually triggers dynamic scheduling and finds suitable field agents based on various parameters. The dispatcher chooses to accept. Suitable for high volume of tasks needing quick allocation. For example: a telecom company rolling out a new service across a city.
    -   When Intelligent Task Recommendation is invoked in Dispatcher Workspace, any free time that agents have between tasks and events is displayed as white space in the agent's calendar. It suggests the best available tasks to fill these gaps in the schedule. This feature is available to both dispatchers in the Dispatcher Workspace and to field agents in the ServiceNow Agent Mobile Application.
    -   While Auto-Assign focuses on assigning the task to the most suitable technician, Route Optimization reorders these tasks post-assignment to minimize driving time.
-   Automatic: Automatic scheduling is using Dynamic Scheduling to auto-assign incoming tasks based on predefined conditions like skillset or location. This method utilizes predefined rules to assign tasks and is efficient for medium-scale operations, focusing on immediate, individual task assignments. It’s also ideal for tasks with well-defined requirements, such as routine maintenance tasks for a fleet of rental cars. Automatic scheduling can also be triggered from an event, such as when a tech schedules non-available time, tasks are automatically removed and rescheduled. This may be used during vacations or unexpected sick leaves.
-   Schedule Optimization: Batch Optimization optimizes tasks in batches for multiple field agents, considering all constraints. Use it at the beginning of the day or week. For example, a cleaning service plans its week ahead for multiple clients. Intraday Optimization reoptimizes schedules in real-time based on changing conditions. Useful when tasks are canceled, delayed, or new tasks come in. For example: a cable service provider deals with last-minute cancellations and new installations.

## Automating work order task scheduling

Learn to schedule work order tasks among field agents using automated scheduling methods. With factors like SLAs, task dependencies, and locations in mind, automation streamlines the process for optimal results.

Key Considerations for Scheduling:

-   Service Level Agreements \(SLAs\)
-   Task Windows &amp; Duration
-   Task Dependencies
-   Skills and Parts required
-   Working Time and Overtime
-   Geographical Location
-   Contractor Availability
-   Custom Preferences
-   Task Bundling

The automated scheduling methods consider the key factors and assign tasks to the correct agents. This not only saves time but also enhances the efficiency of the field service operations.

## Efficiently manage technicians and tasks based on location

Field Service Management provides different types of maps. These maps help field service agents, managers, and dispatchers to get tasks done faster.

-   **Agent map**

    Field service agents can view optimized routes for tasks assigned to them on a given day.

    Managers can view optimized routes for tasks assigned to members in their team.

-   **Dispatch map**

    Dispatchers can know where field service technicians are so that the dispatchers can assign and reassign work based on proximity.

    Dispatchers can view all open work tasks so they can understand work distribution and can quickly identify impacted areas.

    Dispatchers can easily assign work tasks, optimize routes, and change assignments directly from the map.

-   **Service level agreement \(SLA\) map**

    The SLA map is color-coded. Dispatchers can prioritize work tasks for technicians based on SLA contractual terms, such as time to breach.


**Related topics**  


[Setting up a Field Service scheduling method](setting-up-scheduling-methods.md)

