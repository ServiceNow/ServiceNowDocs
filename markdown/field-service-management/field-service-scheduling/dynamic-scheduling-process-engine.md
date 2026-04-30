---
title: Learn Dynamic scheduling process engine
description: Dynamic scheduling streamlines the allocation of work orders and tasks to field service agents in real-time. This intricate process ensures that each task is matched with the most appropriate agent at the most suitable moment, thoughtfully considering a range of variables, including agent availability, location, skills, and workload.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Learn Dynamic scheduling process engine

Dynamic scheduling streamlines the allocation of work orders and tasks to field service agents in real-time. This intricate process ensures that each task is matched with the most appropriate agent at the most suitable moment, thoughtfully considering a range of variables, including agent availability, location, skills, and workload.

The following are the key steps involved in the dynamic scheduling process:

-   **Task Identification**

    The process commences by identifying the list of pending tasks awaiting dispatch. These tasks can be from customer requests, service agreements, or maintenance schedules. Key task attributes, such as dependencies, service level agreements, and customer preferences, are pivotal in determining the optimal time for task completion.

    **Note:** Work order tasks that are schedule locked are excluded from the dynamic scheduling process.

-   **Initiate the scheduling process**

    Dynamic scheduling can be triggered either manually by a dispatcher or automatically by the system.

    1.  When manually triggered, dispatchers select multiple tasks in the dispatch queue and use the Auto-Assign feature to initiate the dynamic scheduling process.
    2.  Automatic triggering occurs when the system continuously monitors task and agent statuses. If predefined filter conditions are met or specific intervals are reached, the dynamic scheduling process is automatically initiated.
-   **Agent task assignments**

    Once activated, the system identifies potential work groups capable of executing the tasks. It then intelligently optimizes the assignment of tasks to agents based on factors like agent availability, location, skills, and workload. The aim is to pair each task with the most suitable agent.

-   **Agent Recommendations**

    The system generates agent recommendations for each task, considering attributes such as agent skills, location, and availability. These suggestions are derived from an optimization algorithm designed to match tasks with the most suitable agents. The recommendations are presented to the dispatcher for confirmation. The dispatcher reviews these recommendations and may factor in additional considerations before finalizing the assignments. This step ensures that tasks are assigned to the most fitting agents, thereby optimizing the overall efficiency of the dynamic scheduling process.

-   **Dispatcher confirmation**

    The dispatcher confirms the task assignments based on the recommendations. If auto assignment is disabled, the output of the dynamic scheduling process is usually presented to the dispatcher for confirmation and approval before tasks are assigned. The dispatcher may consider additional factors, specific to the task requirements, urgency, or customer preferences, before confirming the assignments.

-   **Task start times and updates**

    This stage involves scheduling the start times of tasks based on their urgency, dependencies, and other relevant criteria. As tasks progress, the system continuously updates task statuses, agent availability, and real-time data changes.

-   **Unassignment and Reassignment**

    In situations where there are changes in agent availability or task priorities, the system has the capability to unassign or reassign tasks to ensure efficient resource allocation. This becomes especially relevant during an agent's time off or when higher-priority tasks need attention.


## Dynamic Scheduling process flow

The following is the process flow diagram for Dynamic Scheduling.![Dynamic Scheduling process flow.](../image/dynamic-scheduling-process-flow.jpg)

**Related topics**  


[Roles and personas required for Dynamic Scheduling](roles-and-personas-for-dynamic-scheduling.md)

